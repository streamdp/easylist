## EasyList
Github workflow for automatically update and combine several simple ad blocking lists into one file and prepare it for
use with the [pi-hole](https://github.com/pi-hole) project. 

Last update status: 
* [![updater](https://github.com/streamdp/easylist/actions/workflows/updater.yml/badge.svg)](https://github.com/streamdp/easylist/actions/workflows/updater.yml)

### Usage
Just add [link](https://raw.githubusercontent.com/streamdp/easylist/refs/heads/main/easy-lists-merged.hosts) to the 
`gravity.db` or use buil-in [Adlists](http://pi.hole/admin/groups-adlists.php) manager and run gravity update:
```shell
$ sqlite3 /etc/pihole/gravity.db  "insert into adlist (address) values('https://raw.githubusercontent.com/streamdp/easylist/refs/heads/main/easy-lists-merged.hosts')"
$ pihole -g
```
