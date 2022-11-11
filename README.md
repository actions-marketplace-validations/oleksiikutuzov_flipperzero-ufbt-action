# flipperzero-ufbt-action

## Usage example
> **Note**
> You should checkout your repository to some directory, so that ufbt is not in your repo root

```yml
name: Build FAP

on: [push]

jobs:
  build:
    runs-on: ubuntu-latest

    steps:
    - name: Checkout
      uses: actions/checkout@v3
      with:
        path: flipperzero-lightmeter
        submodules: 'true'
        
    - name: Build
      uses: oleksiikutuzov/flipperzero-ufbt-action@v1
      with:
        fap-dir: flipperzero-lightmeter
        channel: rc
```
