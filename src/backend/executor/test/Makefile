subdir=src/backend/executor
top_builddir=../../../..
include $(top_builddir)/src/Makefile.global

TARGETS=nodeSubplan nodeShareInputScan

include $(top_builddir)/src/backend/mock.mk

nodeSubplan.t: \
	$(MOCK_DIR)/backend/cdb/dispatcher/cdbdisp_mock.o \
	$(MOCK_DIR)/backend/cdb/dispatcher/cdbdisp_query_mock.o \
	$(MOCK_DIR)/backend/commands/explain_mock.o \
	$(MOCK_DIR)/backend/cdb/cdbtm_mock.o \
	$(MOCK_DIR)/backend/cdb/motion/ic_common_mock.o \
	$(MOCK_DIR)/backend/tcop/pquery_mock.o

nodeShareInputScan.t: \
	$(MOCK_DIR)/backend/executor/execUtils_mock.o \
	$(MOCK_DIR)/backend/utils/sort/tuplestorenew_mock.o
