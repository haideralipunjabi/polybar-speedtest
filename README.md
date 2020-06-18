# polybar-speedtest

[speedtest.net](https://speedtest.net) module for [Polybar](https://github.com/jaagr/polybar)

![screenshot](screenshot.png)

## Dependencies

* [python3](https://www.python.org)
* [speedtest-cli](https://github.com/sivel/speedtest-cli/)

## Usage

Make sure the `polybar-speedtest` is executable

``` bash
chmod +x polybar-speedtest
```

Use it in your polybar `config` as

``` yaml
[module/speedtest]  
type = custom/script  
exec-if = hash speedtest
exec = "/path/to/polybar-speedtest"  
interval = 90
```

By default, the module will show Download Speed in bits/sec. Add `--upload` flag in `exec` to show upload speed, and `--bytes` to use bytes/sec. You can also modify the `interval` parameter (in seconds) to change the refresh delay.  

*Note: The module might not be visible from the start as it takes sometime to do the speedtest*

## Also See
[KDEConnect Module for Polybar](https://github.com/HackeSta/polybar-kdeconnect)  
[qBittorrent Module for Polybar](https://github.com/HackeSta/polybar-qbittorrent)
