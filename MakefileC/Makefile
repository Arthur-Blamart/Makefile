# ======= Target =======
TARGET = prog

# ------Compiler------
CC = gcc

# -----Compilation Flags-----
WARNING_FLAGS = -W -Wall
OPTIMIZATION_FLAGS = -O0
HEADER_FLAG = -I $(HEADER_DIR)


CFLAGS = -c $(WARNING_FLAGS) $(OPTIMIZATION_FLAGS) $(HEADER_FLAG)

# -----locations-----
SOURCE_DIR = src
HEADER_DIR = header
BUILD_DIR = build
BIN_DIR = bin

# ------Lists------
SRC_LIST = ${wildcard src/*}
OBJ_LIST = ${SRC_LIST:src/%.c=$(BUILD_DIR)/%.o}


.PHONY : all
all : $(BIN_DIR)/$(TARGET)

# ========= Target Rule =========
$(BIN_DIR)/$(TARGET) : ./build/hello.o ./build/main.o
	@echo "========= Link time ========="
	@$(CC) $(OBJ_LIST) -o $(BIN_DIR)/$(TARGET)
	@echo "========= Link time Finished ========="

# ========= Object Rule =========
$(BUILD_DIR)/%.o : $(SOURCE_DIR)/%.c $(HEADER_DIR)/%.h
	@echo "========= Building $@ ========="
	@$(CC) $(CFLAGS) $< -o $@
	@echo "========= $@ Finished  ========="

# ========= initialize directories =========
.PHONY : init
init : 
	@echo "Creating workspace"
	@echo "Don't forget :"
	@echo "1 header.h for 1 source.c file"
	@mkdir bin build src header

# ======= Cleaner =======
.PHONY : clean
clean : cleanBin cleanBuild

.PHONY : cleanBin
cleanBin : 
	@rm $(BIN_DIR)/*

.PHONY : cleanBuild
cleanBuild : 
	@rm $(BUILD_DIR)/*.o
