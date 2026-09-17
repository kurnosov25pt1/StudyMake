# Усложненный make-file.  Введены переменные для параметров компиляции и исполняемых файлов

.PHONY: all debug release clean

RELEASE_FLAGS = -O2 -Wall -DNDEBUG
DEBUG_FLAGS   = -g -O0 -Wall
RELEASE_EXEC  = hello
DEBUG_EXEC    = hello-dbg
SOURCE        = hello.cpp

all: debug release

debug: $(DEBUG_EXEC)

$(DEBUG_EXEC): hello.cpp
	g++ $(DEBUG_FLAGS) $(SOURCE) -o $(DEBUG_EXEC) #Используем переменную SOURCE 

release: $(RELEASE_EXEC)

$(RELEASE_EXEC): hello.cpp
	g++ $(RELEASE_FLAGS) $(SOURCE) -o $(RELEASE_EXEC) #Используем переменную SOURCE 

clean:
	rm -f $(RELEASE_EXEC) $(DEBUG_EXEC)

