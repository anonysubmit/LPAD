Test Environment
===
We test this software on a MSI laptop equipped with SGX CPU, the CPU model is Intel(R) Core(TM) i7-6820HK CPU @ 2.70GHz. The OS is Ubuntu 16.04.3 LTS. We use the Intel SGX SDK at the below link to build the software (lastst commit on Nov 30, 2017)

https://github.com/01org/linux-sgx/

![alt text](https://github.com/anonysubmit/LPAD/blob/master/env.jpg "Test Environment")

How to build and run
===

To enable LPAD protocol, edit the following line in the Makefile

```
LSM_VERIFY ?= 1
```

make

./app
