OBJ_DIR = ../../../obj/
BIN_DIR = ../../../bin/
UTILITIES_DIR = ../../utils/
# -------------------
# define our includes
# -------------------
INCLUDES =  -I$(UTILITIES_DIR)/general/ \
			-I$(UTILITIES_DIR)/fileType/ \
			-I$(UTILITIES_DIR)/FileRecordTools/ \
           -I$(UTILITIES_DIR)/FileRecordTools/FileReaders/ \
           -I$(UTILITIES_DIR)/FileRecordTools/Records/ \
			-I$(UTILITIES_DIR)/KeyListOps/ \
			-I$(UTILITIES_DIR)/GenomeFile/ \
 			-I$(UTILITIES_DIR)/BamTools/include \
			-I$(UTILITIES_DIR)/BamTools/src/ \
			-I$(UTILITIES_DIR)/version/
			

# ----------------------------------
# define our source and object files
# ----------------------------------
SOURCES= ContextBase.cpp ContextBase.h ContextIntersect.cpp ContextIntersect.h ContextFisher.cpp ContextFisher.h ContextMap.cpp \
	ContextMap.h ContextSample.cpp ContextSpacing.cpp ContextSample.h ContextSpacing.h ContextMerge.h ContextMerge.cpp ContextJaccard.h ContextJaccard.cpp \
	ContextClosest.cpp ContextClosest.h
OBJECTS= ContextBase.o ContextIntersect.o ContextFisher.o ContextMap.o ContextSample.o ContextSpacing.o ContextMerge.o ContextJaccard.o ContextClosest.o
_EXT_OBJECTS=ParseTools.o QuickString.o
EXT_OBJECTS=$(patsubst %,$(OBJ_DIR)/%,$(_EXT_OBJECTS))
BUILT_OBJECTS= $(patsubst %,$(OBJ_DIR)/%,$(OBJECTS))

all: $(BUILT_OBJECTS)

.PHONY: all

$(BUILT_OBJECTS): $(SOURCES)
	@echo "  * compiling" $(*F).cpp
	@$(CXX) -c -o $@ $(*F).cpp $(LDFLAGS) $(CXXFLAGS) $(INCLUDES)

clean:
	@echo "Cleaning up."
	@rm -f $(OBJ_DIR)/ContextBase.o \
	       $(OBJ_DIR)/ContextIntersect.o \
	       $(OBJ_DIR)/ContextFisher.o \
	       $(OBJ_DIR)/ContextMap.o \
	       $(OBJ_DIR)/ContextSample.o \
	       $(OBJ_DIR)/ContextSpacing.o \
	       $(OBJ_DIR)/ContextMerge.o \
	       $(OBJ_DIR)/ContextJaccard.o \
	       $(OBJ_DIR)/ContextClosest.o \

.PHONY: clean
