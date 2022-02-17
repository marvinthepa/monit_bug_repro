Run:

```
  /path/to/monit -Iv -c monitrc
```

In a separate terminal, run

```
  /path/to/monit -c monitrc start all
```

Observe:
With monit 5.26.0, the output of `/path/to/monit -c monitrc` contains:

```
foo                             │ OK                         │ Process
```

With monit >= 5.27.0

```
foo                             │ Not monitored              │ Process
```
