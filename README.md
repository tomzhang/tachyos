# Tachyos
A Mesos Framework for Tachyon, a memory-centric distributed file system.
## Word of Warning

_This is not production-ready version. Still Under development._

## Prerequisites

- A Mesos cluster
- Java JDK

## Usage

```bash
$ java -cp tachyos-0.1.0-uber.jar com.apache.mesos.tachyos.Main
```
 `mesosMaster` and other configuration parameters must be specified in "SchedulerConf.java"

## Design

### Tachyon-Mesos Scheduler

The scheduler:

- registers as a framework with a Mesos master, naturally
- links against the tachyon library and starts a Tachyon Master
  in the same process.
- launches Tachyon worker processes on Mesos slaves

