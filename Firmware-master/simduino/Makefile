# Based on code from simavr (https://github.com/buserror/simavr)

target=	simduino
board = ${OBJ}/${target}.elf
# simavr = ../../

# IPATH = .
# IPATH += ../parts
# IPATH += ${simavr}/include
# IPATH += ${simavr}/simavr/sim

# VPATH = .
# VPATH += ../parts

LDFLAGS += -lpthread -lutil

# include ../Makefile.opengl

all: obj ${target}

include Makefile.common

${board} : ${OBJ}/uart_pty.o
${board} : ${OBJ}/${target}.o

${target}: ${board}
	cp ${board} ${target}

clean: clean-${OBJ}
	rm -rf *.a *.axf ${target} *.vcd *.hex
