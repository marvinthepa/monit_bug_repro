This is a minimal reproduction of https://bitbucket.org/tildeslash/monit/issues/1028/.
The bug is now fixed, see there for details.

Run:

```
  /path/to/monit -Iv -c monitrc
```

In a separate terminal, run

```
  /path/to/monit start all
```

Observe:
With monit 5.26.0, the output of `/path/to/monit summary` contains:

```
foo                             │ OK                         │ Process
```

With monit >= 5.27.0

```
foo                             │ Not monitored              │ Process
```
