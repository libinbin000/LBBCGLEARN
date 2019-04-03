CC=g++

TARGET=test

CFLAGS= -Wall

SRCS=main.cpp\
../library/glad/src/glad.c

	

OBJS=$(SRCS:.c=.o)

INCLUDES=-I../library/glfw-3.2.1.bin.WIN32/include\
-I../library/glad/include\
-I../library/glew-2.1.0-win32/glew-2.1.0/include\

LIB_PATHS=-L../library/glfw-3.2.1.bin.WIN32/lib-mingw\
-L../library/glew-2.1.0-win32/glew-2.1.0/lib/Release/Win32

LIBS=-lglfw3 -lglfw3dll -lgdi32 #-lopengl32

#在gcc末尾加入以下代码

SO=-Wl,-rpath=../library/glfw-3.2.1.bin.WIN32/lib-mingw

$(TARGET):$(OBJS)
	$(CC) $^ -o $@	$(CFLAGS) $(INCLUDES) $(LIB_PATHS) $(LIBS) $(SO)

%.o : %.c
	$(CC) -c $< -o $(<:.c=.o) $(CFLAGS) $(INCLUDES) $(LIB_PATHS) $(LIBS) -g

clean:
	rm -rf *.out *.o    #清除中间文件及生成文件

.PHONY:clean