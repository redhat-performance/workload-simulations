# workload-simulations
Workload simulations using fio, uperf, vdbench, etc.  Contact [Robert Krawitz](mailto:rlk@redhat.com) for more information.

The purpose of this repository is to serve as a library of job files
for simulating workloads, rather than everyone creating their own
jobs.  The job files should be used as starting points; some things
(such as pathnames, DNS hostnames, IP addresses) and such can't be
constant.  Going forward, we may add tools to instantiate job files
from templates.

## Structure

At least initially, the repo will be structured as

```
.
|-- fio
|   |-- transaction-processing.job
|	|-- analytics.job
|	|-- linpack.job
|-- uperf
|   |-- pingpong.job
|   |-- client-server.job
|-- ...
```

In the future, we may reorganize this.

The top level README.md will contain an inventory of job files,
grouped by workload type rather than by tool.

## Inventory

### Basic Operations

- **fio/basic-operations-with-fdatasync.job**: perform basic
  read()/write() testing with use of fdatasync.
  
### RDBMS

### HPTC
