Test Environment
===
We test this software on a MSI laptop equipped with SGX CPU, the CPU model is Intel(R) Core(TM) i7-6820HK CPU @ 2.70GHz. The OS is Ubuntu 16.04.3 LTS. We use the Intel SGX SDK at the below link to build the software (lastst commit on Nov 30, 2017)

https://github.com/01org/linux-sgx/

![](https://github.com/anonysubmit/LPAD/blob/master/env.png "Test Environment")

How to build and run
===

To enable LPAD protocol, edit the following line in the Makefile

```
LSM_VERIFY ?= 1
```

To build the project, just run

```
make
```

Running db_bench for LPAD is the same as running original db_bench, for example, the below command runs sequential write with one million records.

```  
./app --benchmarks=fillseq --num=1000000
```

![](https://github.com/anonysubmit/LPAD/blob/master/run.png "Running a workload")
