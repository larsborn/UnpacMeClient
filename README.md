# UnpacMe API Client
Python-based Client for the [unpac.me] service.  

## Installation

Requires at least Python 3.7 and the package `requests` to be installed. Fully compatible with being run in a virtual
environment. It is recommended to set the environment variable `UNPACME_API_KEY` to the API key you can get from 
https://www.unpac.me/account.

## Example Usage
After aliasing the script `unpac-me.py` to `unpac` and setting the environment variable `UNPACME_API_KEY` a typical 
session may look like the following:
 
```Batch
> unpac --debug upload 3d9f7ec30e9da132aca7cdd2c34f765cca1b5a24b66a5eccad6d470dd77eefb1
[DEBUG] Using User-Agent string: UnpacMeClient/1.0.0 (python-requests 2.22.0) Windows (8.1)
[DEBUG] Tasking "3d9f7ec30e9da132aca7cdd2c34f765cca1b5a24b66a5eccad6d470dd77eefb1"...
[DEBUG] Pooling Status of Upload ID: polling status of submission id "0dfd97cd-df01-4ea6-9ca5-7597cf03dbbb"...
...
[INFO] Unpacking finished: <UnpacMeResults status=UnpacMeStatus.COMPLETE>

> unpac status 0dfd97cd-df01-4ea6-9ca5-7597cf03dbbb --list
[INFO] Task completed
SHA256: 3d9f7ec30e9da132aca7cdd2c34f765cca1b5a24b66a5eccad6d470dd77eefb1

Unpacked Files
---
3d9f7ec30e9da132aca7cdd2c34f765cca1b5a24b66a5eccad6d470dd77eefb1
8338f8f988a574ca90f2723ea178a4cbc8ea34d9bb79c1d0e0ebc2ce516c4b0d (win_nanocore_w0)
61e9d5c0727665e9ef3f328141397be47c65ed11ab621c644b5bbf1d67138403
01e3b18bd63981decb384f558f0321346c3334bb6e6f97c31c6c95c4ab2fe354
f9b8c3f31375e9a1ec105f930f751869a804110d29d6b38e7298622eb74b2bec

> unpac download 8338f8f988a574ca90f2723ea178a4cbc8ea34d9bb79c1d0e0ebc2ce516c4b0d

> file 8338f8f988a574ca90f2723ea178a4cbc8ea34d9bb79c1d0e0ebc2ce516c4b0d
8338f8f988a574ca90f2723ea178a4cbc8ea34d9bb79c1d0e0ebc2ce516c4b0d: PE32 executable (GUI) Intel 80386 Mono/.Net ...
```





[unpac.me]: https://www.unpac.me/
