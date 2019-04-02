CC=gcc

TARGET=test

CFLAGS= -Wall

SRCS=main.c\

OBJS=$(SRCS:.c=.o)

INCLUDES=-I../library/glfw-3.2.1.bin.WIN32/include\

LIB_PATHS=-L../library/glfw-3.2.1.bin.WIN64/lib-mingw-w64
LIBS=-lglfw3\

#在gcc末尾加入以下代码

#SO=-Wl,-rpath=../library/glfw-3.2.1.bin.WIN64/lib-mingw

$(TARGET):$(OBJS)
	$(CC) $^ -o $@	$(CFLAGS) $(INCLUDES) $(LIB_PATHS) $(LIBS) $(SO)

%.o : %.c
	$(info >>>>>>>>>>>>>>>>>>>>>>>%.o)
	$(CC) -c $< $(CFLAGS) $(INCLUDES) $(LIB_PATHS) $(LIBS)

clean:
	rm -rf *.out *.o    #清除中间文件及生成文件

.PHONY:clean