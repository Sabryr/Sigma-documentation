# Job Types on Betzy

Betzy is designed to run highly parallelized jobs.  If you need to run medium-sized jobs, than Fram is a better choice, while for serial jobs you shall use Saga.

For a preprocessing or postprocessing job which only needs one or max 32 CPU cores, use a *preproc* job.

For development or testing use the  *devel* queue which is limited to small and short jobs. 

Here is a more detailed description of the different job types on Betzy:

## Normal

- __Allocation units__: whole nodes
- __Job Limits__:
    - minimum 8 nodes
    - maximum 256 nodes
- __Maximum walltime__: 4 days
- __Priority__: normal
- __Available resources__: 1340 nodes with 128 CPU cores and 256 GiB RAM

This is the default job type. In _normal_ jobs, the queue system hands out complete nodes.


## Preproc

- __Allocation units__: shared node between users
- __Job Limits__:
    - minimum 1 CPU core per user
    - maximum 32 CPU cores per user
- __Maximum walltime__: 1 day
- __Priority__: normal
- __Available resources__: *preproc* jobs run on a dedicated node with 32 CPU
	cores and 256 GiB RAM

*preproc* jobs are meant for small preprocessing or postprocessing tasks.  Typically, such jobs don't use many CPUs, so requiring them to use 8 nodes would be wasting of resources.

## Devel

- __Allocation units__: whole nodes
- __Job Limits__:
    - minimum 1 nodes, maximum 4 nodes per job
    - maximum 1 job per user
    - maximum 20 jobs per *devel* queue
- __Maximum walltime__: 20 minutes
- __Priority__: high
- __Available resources__: 4 nodes with 128 CPU cores and 256 GiB RAM

This is meant for small, short development or test jobs.  *Devel* jobs have access to a set of dedicated nodes.

If you have _temporary_ development needs that cannot be fulfilled by the _devel_ job type, please contact us at
<support@metacenter.no>.