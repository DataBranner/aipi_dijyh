Because my ISP frequently changes my IP address at home without notifying me, I run a cron job every 15 minutes to store the current IP address and, if it has changed, push it to a remote Git repository where I can see it.

The script is in `script.sh` and should have its mode made executable. The cron job is as below; note that the `SHELL` and `PATH` values should reflect the values on the platform where the script is being run.

```
SHELL=/bin/bash
PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games
 
0 * * * *  <PATH TO REPO>/aipi_dihjyy/script.sh
15 * * * * <PATH TO REPO>/aipi_dihjyy/script.sh
30 * * * * <PATH TO REPO>/aipi_dihjyy/script.sh
45 * * * * <PATH TO REPO>/aipi_dihjyy/script.sh
```

The current IP address is saved in a file `aipi_dihjyy`.

[end]
