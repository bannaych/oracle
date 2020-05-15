# Install Oracle on ASM

- Install the OEL Linux OS ( I will not go into the install process )
- Update Linux packages
- create all the disk required for ASM, DATA FRA REDO
- Download the Oracle pre-install packages - pick the version you want to install
```
yum search oracle
yum search oracle
Loaded plugins: langpacks, ulninfo
=========================================================================== N/S matched: oracle ===========================================================================
kmod-oracleasm.x86_64 : oracleasm kernel module(s)
oracle-database-preinstall-18c.x86_64 : Sets the system for Oracle Database single instance and Real Application Cluster install for Oracle Linux 7
oracle-database-preinstall-19c.x86_64 : "Sets the system for Oracle Database single instance and Real Application Cluster 19c install for Oracle Linux .el7"
```
- Install oracle 19c
```
yum install oracle-database-preinstall-19c.x86_64
```
- install the Oracle ASM packages
```
yum search oracleasm
[root@ora2 ~]# yum search oracleasm
Loaded plugins: langpacks, ulninfo
========================================================================= N/S matched: oracleasm ==========================================================================
kmod-oracleasm.x86_64 : oracleasm kernel module(s)
oracleasm-support.x86_64 : The Oracle Automatic Storage Management support programs.
oracleasmlib.x86_64 : The Oracle Automatic Storage Management library userspace code.
```
```
yum install oracleasm-support.x86_64
```
NOTE: **You do not need to install kmod from 7.4 onwards, Its included in the kernal**
