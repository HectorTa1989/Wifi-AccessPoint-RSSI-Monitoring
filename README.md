# Wifi-AccessPoint-RSSI-Monitoring
Python script to monitor wifi access point signal strength. It collects RSSI information about wifi access points around you and draws graphics showing RSSI activity.

## Goal
The idea was to provide a commandline way to collect RSSI data on the platforms where it's only possible through NetworkManager
and there is no robust and simple console utility.

## Dependencies

```
matplotlib
python-tk
```

## Usage

```
usage: list_rssi.py [-h] [-i] [-n [NETWORKS [NETWORKS ...]]]

optional arguments:
  -h, --help            show this help message and exit
  -i, --interactive     start polling RSSI from the networks
  -n [NETWORKS [NETWORKS ...]], --networks [NETWORKS [NETWORKS ...]]
                        networks to collect data from
```

After start you recieve an RSSI data for all access points around you.
If you didn't enable interactive mode, this is the only usecase, good
for platforms without UI.

In the interactive mode those commands are available:
After that you will be prompted for a command.
    plot
        draw an RSSI activity graphic for this moment since program start
    stop
        stop the program
    print
        print actual rssi data one more time

### Example
    ./list_rssi.py -i -n "WifiHome" "WifiBuddy" "Dlink200"
    ... walking around the apartment for some time with opened laptop to confuse everybody
    plot
    ...watching your graphic
    stop
