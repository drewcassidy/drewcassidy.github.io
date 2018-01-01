---
title: Raspbian Time-Zones and ntpd
tags: Raspberry-pi linux
---
Setting the time zone in raspbian using `raspi-config` has strange results
```
Current default time zone: 'US/Pacific-New'
Local time is now:      Mon Jan  1 08:02:07 PST 2018.
Universal Time is now:  Mon Jan  1 16:02:07 UTC 2018.
```

setting the time zone to GMT-8 manually is even weirder
```
Current default time zone: 'Etc/GMT-8'
Local time is now:      Tue Jan  2 00:02:46 +08 2018.
Universal Time is now:  Mon Jan  1 16:02:46 UTC 2018.
```

The solution is to shut down ntpd while changing the time zone
``` shell
sudo /etc/init.d/ntp stop
sudo raspi-config #set time zone
sudo date -s "1 Jan 2018 00:09:00"
sudo /etc/init.d/ntp start
```

And yes, I did spend New Years debugging time zones in Linux, among other things.
