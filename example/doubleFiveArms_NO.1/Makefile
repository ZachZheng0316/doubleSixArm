TARGET		= doubleFiveArms
OBJS		= doubleFiveArms.o
SRCS		= $(OBJS:.o=.c)
INCLUDEDIRS	+= -I../../include
LIBDIRS		+= -L../../lib
CFLAGS		= $(INCLUDEDIRS) -W -Wall -O2
LDFLAGS		= $(LIBDIRS) -lm -ldxl

#CC			= gcc
CC			= arm-linux-gnueabi-gcc

$(TARGET): $(OBJS)
	$(CC) -o $@ $^ $(LDFLAGS)
	
.c.o:
	$(CC) -c $< $(CFLAGS)
	
clean:
	rm -f $(OBJS) $(TARGET)
	rm -f *~
	@echo "file deleted."

dep:
	gccmakedep $(SRCS)

