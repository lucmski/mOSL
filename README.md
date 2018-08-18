# macOS Lockdown (mOSL)
[![Build Status](https://travis-ci.org/0xmachos/mOSL.svg?branch=master)](https://travis-ci.org/0xmachos/mOSL) [![GitHub Release](https://github-basic-badges.herokuapp.com/release/0xmachos/mOSL.svg)](https://github.com/0xmachos/mOSL/releases/latest)

Bash script to audit and fix macOS High Sierra (`10.13.x`) security settings

## Warnings
- This script will **only ever** support the _latest_ macOS release  
- This script requires your **password** to invoke some commands with `sudo`  

## Verification

The executable `Lockdown` file can be verified with [Minisign](https://jedisct1.github.io/minisign/):
```
minisign -Vm Lockdown -P RWTiYbJbLl7q6uQ70l1XCvGExizUgEBNDPH0m/1yMimcsfgh542+RDPU
```
Install via [brew](https://brew.sh/): `brew install minisign`

## Usage

```
$ ./Lockdown 

  Audit or Fix macOS security settings🔒🍎

  Usage: ./Lockdown [list | audit {setting_index} | fix {setting_index}]

    list         - List settings that can be audited/ fixed
    audit        - Audit the status of all or chosen setting(s) (Does NOT change settings)
    fix          - Attempt to fix all or chosen setting(s) (Does change settings)

    fix-force    - Same as 'fix' however bypasses user confirmation prompt
                   (Can be used to invoke Lockdown from other scripts)
```

## Settings

Settings that can be audited/ fixed:
```
  [0] enable automatic updates
  [1] enable gatekeeper
  [2] enable firewall
  [3] enable admin password preferences
  [4] enable terminal secure entry
  [5] enable sip
  [6] disable firewall builin software
  [7] disable firewall downloaded signed
  [8] disable ipv6
  [9] disable mail remote content
  [10] disable remote apple events
  [11] disable remote login
  [12] set airdrop contacts only
  [13] set appstore update check daily
  [14] check kext loading consent
  [15] check efi integrity
  [16] check filevault
  [17] check firmware password set
```
