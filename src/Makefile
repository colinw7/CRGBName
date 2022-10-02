CPP_CC = g++

AR = ar
RM = rm

CDEBUG = -g

INC_DIR = ../include
OBJ_DIR = ../obj
LIB_DIR = ../lib
BIN_DIR = ../bin

all: $(LIB_DIR)/libCRGBName.a

CPP_SRC = \
CRGBName.cpp \

CPP_OBJS = $(patsubst %.cpp,$(OBJ_DIR)/%.o,$(CPP_SRC))

CFLAGS = \
-std=c++17 \
$(CDEBUG) \
-I$(INC_DIR) \
-I. \
-I../../CStrUtil/include \
-I../../CMath/include \
-I../../COS/include \
-I../../CUtil/include \

clean:
	$(RM) -f $(OBJ_DIR)/*.o
	$(RM) -f $(LIB_DIR)/libCRGBName.a

.SUFFIXES: .cpp

$(CPP_OBJS): $(OBJ_DIR)/%.o: %.cpp
	$(CPP_CC) -c $< -o $(OBJ_DIR)/$*.o $(CFLAGS)

$(LIB_DIR)/libCRGBName.a: $(CPP_OBJS)
	$(AR) crv $(LIB_DIR)/libCRGBName.a $(CPP_OBJS)
