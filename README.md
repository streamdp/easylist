## EasyList
Github workflow for automatically update and combine several simple ad blocking lists into one file and prepare it for
use with the [pi-hole](https://github.com/pi-hole) project. 

Last update status: 
* [![updater](https://github.com/streamdp/easylist/actions/workflows/updater.yml/badge.svg)](https://github.com/streamdp/easylist/actions/workflows/updater.yml)

### Usage
Just add [link](https://raw.githubusercontent.com/streamdp/easylist/refs/heads/main/merged.hosts) to the 
`/etc/pihole/adlists.list` or use buil-in [Adlists](http://pi.hole/admin/groups-adlists.php) manager and run gravity update:
```shell
$ echo https://raw.githubusercontent.com/streamdp/easylist/refs/heads/main/merged.hosts > /etc/pihole/adlists.list
$ pihole -g
```
