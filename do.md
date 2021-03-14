# DigitalOcean

    ubuntu-2004: TASK [sysprep : Delete all logrotated log zips] ********************************
    ubuntu-2004: changed: [default]
    ubuntu-2004:
    ubuntu-2004: TASK [sysprep : Remove swapfile] ***********************************************
    ubuntu-2004: skipping: [default] => (item={'path': '/swapfile', 'state': 'absent'})
    ubuntu-2004: skipping: [default] => (item={'path': '/mnt/resource/swapfile', 'state': 'absent'})
    ubuntu-2004:
    ubuntu-2004: TASK [sysprep : Truncate shell history] ****************************************
    ubuntu-2004: ok: [default] => (item={'path': '/root/.bash_history'})
    ubuntu-2004: ok: [default] => (item={'path': '/home/root/.bash_history'})
    ubuntu-2004:
    ubuntu-2004: PLAY RECAP *********************************************************************
    ubuntu-2004: default                    : ok=72   changed=56   unreachable=0    failed=0    skipped=93   rescued=0    ignored=0
    ubuntu-2004:
==> ubuntu-2004: Gracefully shutting down droplet...
==> ubuntu-2004: Creating snapshot: Cluster API Kubernetes v1.18.15 on Ubuntu 20.04
==> ubuntu-2004: Waiting for snapshot to complete...
==> ubuntu-2004: Destroying droplet...
==> ubuntu-2004: Deleting temporary ssh key...
Build 'ubuntu-2004' finished after 19 minutes 13 seconds.

==> Wait completed after 19 minutes 13 seconds

==> Builds finished. The artifacts of successful builds are:
--> ubuntu-2004: A snapshot was created: 'Cluster API Kubernetes v1.18.15 on Ubuntu 20.04' (ID: 80366900) in regions 'nyc1'

