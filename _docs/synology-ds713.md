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
        ```
        PATH=$PATH:/opt/bin:/opt/sbin # Keep bootstrap on update
        PATH=$PATH:/volume1/@appstore/python/bin/ # Add Python binaries to PATH
        export PATH
        ```
0. `source /etc/profile`
0. Repeat from step 1 for `/root/.profile`
0. Verify with `ipkg -v`
0. Run `ipkg update` 
