CC=g++

TARGET=test

CFLAGS= -Wall

SRCS=main.cpp\
../library/glad/src/glad.c\
	

OBJS=$(SRCS:.c=.o)

INCLUDES=-I../library/glfw-3.2.1.bin.WIN64/include\
-I../library/glad/include

LIB_PATHS=-L../library/glfw-3.2.1.bin.WIN64/lib-mingw-w64\

LIBS=-lglfw3 -lglfw3dll -lgdi32 #-lopengl32

#SO=-Wl,-rpath=../library/glfw-3.2.1.bin.WIN32/lib-mingw-w64

$(TARGET):$(OBJS)
	@$(CC) $^ -o $@	$(CFLAGS) $(INCLUDES) $(LIB_PATHS) $(LIBS) $(SO)

%.o : %.c
	echo "$(<:.c=.o)"
	@$(CC) -c $< -o $(<:.c=.o) $(CFLAGS) $(INCLUDES) $(LIB_PATHS) $(LIBS)

clean:
	rm -rf *.out *.o    #清除中间文件及生成文件

.PHONY:clean