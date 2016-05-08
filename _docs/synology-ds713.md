---
title: Synology DS713+ guide
tags: [nas]
---

# Synology DS713+ Guide

## Updating DSM

When DSM is updated, sometimes access to ipkg and optware is lost.

### Access ipkg and optware after DSM update

0. `/opt/bin/nano /etc/profile`
0. Add to the bottom of the file

        PATH=$PATH:/opt/bin:/opt/sbin # Keep bootstrap on update
        PATH=$PATH:/volume1/@appstore/python/bin/ # Add Python binaries to PATH
        export PATH

0. `source /etc/profile`
0. Repeat from step 1 for `/root/.profile`
0. Verify with `ipkg -v`
0. Run `ipkg update` 

> * Preserve your path through DSM updates ([Synology Forum](http://forum.synology.com/enu/viewtopic.php?f=40&t=95756))

### Verify

#### Autostart script

See `/etc/rc.local`

#### pip

    pip install pip --upgrade
    
#### FlexGet

    flexget --version
    pip install flexget --upgrade
    flexget -c /volume1/apps/flexget/config.yml check
    flexget -c /volume1/apps/flexget/config.yml --test execute

#### Subliminal

    subliminal --addic7ed oscarb {ADDIC7ED_PASSWORD} --cache-dir /volume1/apps/subliminal/ download --language en --provider addic7ed --provider podnapisi --provider opensubtitles --provider subscenter --provider thesubdb --provider tvsubtitles  --age 2d /volume1/downloads/tv/
    


    
