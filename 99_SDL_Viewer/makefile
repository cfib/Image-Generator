# Makefile
CC       = clang
RM       = rm -rf
CFLAGS   = -Wall -Wextra -g `pkg-config sdl2 --cflags` -O3
SRCPATH  = ./src
GENERATOR_DIR ?= ../1_Image-Generator_pthread
SHRPATH  = $(GENERATOR_DIR)/shared/src
INCPATH  = -I./$(GENERATOR_DIR)/shared/include
LIBPATH  =
LIBS     = `pkg-config sdl2 --libs`
SRC      = $(SRCPATH)/image_viewer.c
SRC     += $(wildcard $(SHRPATH)/*.c)
TARGET   = image_viewer
$(TARGET): $(SRC)
	$(CC) -o $(TARGET) $(CFLAGS) $(SRC) $(INCPATH) $(LIBPATH) $(LIBS)

clean:
	$(RM) *~ *.o $(TARGET)

