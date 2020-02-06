TOP=../..

include $(TOP)/configure/CONFIG
#----------------------------------------
#  ADD MACRO DEFINITIONS AFTER THIS LINE
#=============================

#=============================
# Build the IOC application

PROD_IOC = sbtest-mk-ioc
# sbtest-mk-ioc.dbd will be created and installed
DBD += sbtest-mk-ioc.dbd

# sbtest-mk-ioc.dbd will be made up from these files:
sbtest-mk-ioc_DBD += base.dbd
sbtest-mk-ioc_DBD += iocAdmin.dbd
sbtest-mk-ioc_DBD += geminiRecords.dbd
sbtest-mk-ioc_DBD += aSubRecord.dbd
sbtest-mk-ioc_DBD += timelib.dbd
sbtest-mk-ioc_DBD += slalib.dbd
#sbtest-mk-ioc_DBD += menuScan.dbd
sbtest-mk-ioc_DBD += initTrace.dbd
sbtest-mk-ioc_DBD += sbtest.dbd

# Include dbd files from all support modules:
#sbtest-mk-ioc_DBD += xxx.dbd

# Add all the support libraries used by this IOC
sbtest-mk-ioc_LIBS_RTEMS += bancomm 

sbtest-mk-ioc_LIBS += devIocStats
sbtest-mk-ioc_LIBS += geminiRecords
sbtest-mk-ioc_LIBS += timelib
sbtest-mk-ioc_LIBS += slalib
sbtest-mk-ioc_LIBS += seq pv

sbtest-mk-ioc_SRCS += initTrace.c
sbtest-mk-ioc_SRCS += sbtest.c
# sbtest-mk-ioc_registerRecordDeviceDriver.cpp derives from sbtest-mk-ioc.dbd
sbtest-mk-ioc_SRCS += sbtest-mk-ioc_registerRecordDeviceDriver.cpp

# Build the main IOC entry point on workstation OSs.
sbtest-mk-ioc_SRCS_DEFAULT += sbtest-mk-iocMain.cpp

# Finally link to the EPICS Base libraries
sbtest-mk-ioc_LIBS += $(EPICS_BASE_IOC_LIBS)

#===========================

include $(TOP)/configure/RULES
#----------------------------------------
#  ADD RULES AFTER THIS LINE

