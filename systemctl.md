## Service Management

### Starting and Stopping Services

Starting

```bash
> sudo systemctl start application.service
```

or simply

```bash
> sudo systemctl start application
```

Stopping

```bash
> sudo systemctl stop application.service
```

### Restarting and Reloading

```bash
> sudo systemctl restart application.service
```

If the application in question is able to reload its configuration files (without restarting), you can issue the reload command to initiate that process:

```bash
> sudo systemctl reload application.service
```

## Enabling and Disabling Services

The above commands are useful for starting or stopping commands during the current session.

```bash
> sudo systemctl enable application.service
> sudo systemctl disable application.service
> systemctl daemon-reload
> systemctl reset-failed
```

### Checking the Status of Services

```bash
> systemctl status application.service
> systemctl is-active application.service
> systemctl is-enabled application.service
> systemctl is-failed application.service
```

## Verify a service file

```bash
> sudo systemd-analyze verify application.service
```

## Following the logs dor those services

```bash
# Filter with service
> sudo journalctl -u application.service
# To list boots
> journalctl --list-boots
# From Last boot
> journalctl -b -1
# Since last hour
> journalctl --since "1 hour ago"
# Since yesterday and until now
> journalctl ---since yesterday --until now
# Reverse order and last 50 logs
> journalctl -u application.service -r -n 50
# Output formats -jsonwill,verbose,cat,short-monotonic,json-pretty
> journalctl -o json-pretty

```

## Setting the System Time

```bash
# Listing time zones
> timedatectl list-timezones
# Show current status
> timedatectl status
# Set timezone
> sudo timedatectl set-timezone zone
```

Sources:

* [using-journalctl] (<https://www.loggly.com/ultimate-guide/using-journalctl/)>
* [how-to-use-journalctl-to-view-and-manipulate-systemd-logs] (<https://www.digitalocean.com/community/tutorials/how-to-use-journalctl-to-view-and-manipulate-systemd-logs)>
* [cheat-sheets/journalctl] (<https://www.cheatography.com/airlove/cheat-sheets/journalctl/)>
* [managing-logging-systemd] (https://blog.selectel.com/managing-logging-systemd/)
