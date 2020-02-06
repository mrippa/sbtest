TOP=../..
include $(TOP)/configure/CONFIG

#----------------------------------------
#  ADD MACRO DEFINITIONS AFTER THIS LINE

# Search for .db files in $SYS_DB_PATHS, the list 
# of paths output by "convertGemRelease.pl dbPaths"
vpath %.db $(SYS_DB_PATHS)

#----------------------------------------------------
# Create and install (or just install) into <top>/db
# databases, templates, substitutions like this
# DB += xxx.db
DB += iocAdminRTEMS.db
DB += asubRX.db
DB += asubTX.db
DB += userHost.substitutions
#DB += asub2.db
#DB += userHost2.substitutions
#DB += userHost3.substitutions
#DB += userHost4.substitutions
#DB += tcs.substitutions
#DB += mcs.substitutions

include $(TOP)/configure/RULES
#----------------------------------------
#  ADD RULES AFTER THIS LINE
$(COMMON_DIR)/%.db: %.db
	cp $< $@

clean::
	$(RM) *.dat *.bak
