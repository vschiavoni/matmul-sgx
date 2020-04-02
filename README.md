------------------------
Purpose of matmul-sgx
------------------------
This project consists of a parallel and secure version of the multiplication multiplication problem. I performes the multiplication of two matrices (A and B) into a third one (C). Parallelization is achived using OmpSs Programming Model and security is assured by means of Intel SGX.

------------------------------------
How to Build/Execute
------------------------------------
1. Install OmpSs
2. Install Intel(R) SGX SDK for Linux* OS
3. Make sure your environment is set:
    $ export TARGET=$HOME/ompss
    $ source ${sgx-sdk-install-path}/environment
4. Build the project with the prepared Makefile:
    a. Hardware Mode, Debug build:
        $ make
    b. Hardware Mode, Pre-release build:
        $ make SGX_PRERELEASE=1 SGX_DEBUG=0
    c. Hardware Mode, Release build:
        $ make SGX_DEBUG=0
    d. Simulation Mode, Debug build:
        $ make SGX_MODE=SIM
    e. Simulation Mode, Pre-release build:
        $ make SGX_MODE=SIM SGX_PRERELEASE=1 SGX_DEBUG=0
    f. Simulation Mode, Release build:
        $ make SGX_MODE=SIM SGX_DEBUG=0
5. Execute the binary directly:
    $ ./app
6. Remember to "make clean" before switching build mode
