TARGET = libxxx.so #编译生成的动态库
PRIV_CFLAGS += 
PRIV_LDFLAGS += -shared -fPIC
SRCS=libxxx.c	#生成动态库的源文件
TEST_SRCS=xxx.c	#带main函数的.c
TEST_BIN=xxx	#生成main函数的可执行文件

all:
	$(CC) -o  $(TARGET) $(SRCS)  $(PRIV_CFLAGS) $(PRIV_LDFLAGS)
	$(CC) -o  $(TEST_BIN) $(TEST_SRCS) -lxxx -L. -Wl,-rpath=. #xxx为动态库去掉lib和.so后的名字
clean:
	rm -rf *.o *.so $(TARGET) $(TEST_BIN)
