# mage-smartmontools
Ansible role to install smartmontools. Inspired by https://github.com/LibreIT/ansible-smartd

Role variables:

```
smartd_short_test_month: '..'     # month to start short test (two decimal digits: 01 - 12)
smartd_short_test_dom: '..'       # day of the month to start short test (two decimal digits: 01 - 31)
smartd_short_test_dow: '.'        # day of the week to start short test (one decimal digit: 1 - 7)
smartd_short_test_hour: 'random'  # hour of the day to start short test (two decimal digits: 00 - 23)

smartd_long_test_month: '..'      # month to start long test (two decimal digits: 01 - 12)
smartd_long_test_dom: '..'        # day of the month to start long test (two decimal digits: 01 - 31)
smartd_long_test_dow: 'random'    # day of the week to start long test (one decimal digit: 1 - 7)
smartd_long_test_hour: 'random'   # hour of the day to start long test (two decimal digits: 00 - 23)
```

A randomization of scheduled time (hour,dow) is enabled to avoid to test many disks in the same time.
**NOTE:** "." (dot) are like "?" wildcard in smartd config. Example: `smartd_short_test_month` with `'..'` value is executed every month.