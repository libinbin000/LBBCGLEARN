CC=g++

TARGET=test

CFLAGS= -Wall

SRCS=main.cpp\
	

OBJS=$(SRCS:.c=.o)

INCLUDES=-I../library/glfw-3.2.1.bin.WIN32/include\
-I../library/glad/include

LIB_PATHS=-L../library/glfw-3.2.1.bin.WIN32/lib-mingw\

LIBS=-lglfw3 -lglfw3dll -lgdi32 #-lopengl32

#在gcc末尾加入以下代码

SO=-Wl,-rpath=../library/glfw-3.2.1.bin.WIN32/lib-mingw

$(TARGET):$(OBJS)
	$(CC) $^ -o $@	$(CFLAGS) $(INCLUDES) $(LIB_PATHS) $(LIBS) $(SO)

%.o : %.c
	$(info >>>>>>>>>>>>>>>>>>>>>>>%.o)
	$(CC) -c $< $(CFLAGS) $(INCLUDES) $(LIB_PATHS) $(LIBS)

clean:
	rm -rf *.out *.o    #清除中间文件及生成文件

.PHONY:clean