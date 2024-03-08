# ------ Main class ------
MAIN = Test

# ------ Compiler & Runner ------
CC = javac
RUNNER = java

# ------ Directories ------

SOURCE_DIR = src
CLASSES_DIR = classes

# ------ Lists ------
SRC_LIST = ${wildcard $(SOURCE_DIR)/*}
CLASS_LIST = ${SRC_LIST:$(SOURCE_DIR)/%.java=$(CLASSES_DIR)/%.class}

# ======== Rules ========

.PHONY : all
all : $(CLASS_LIST)


# ------ Compiling ------
classes/%.class : src/%.java
	@$(CC) -d ./$(CLASSES_DIR) -cp ./$(CLASSES_DIR) -sourcepath ./$(SOURCE_DIR) $<

# ------ running ------
.PHONY : run
run :
	$(RUNNER) -cp $(CLASSES_DIR) $(MAIN)

# ------ Workspace initialisation ------
.PHONY : init
init :
	@echo "Creating workspace"
	@mkdir $(SOURCE_DIR);mkdir $(CLASSES_DIR)

# ------ Workspace cleaning (classes) ------

.PHONY : clean
clean :
	@rm $(CLASSES_DIR)/*.class