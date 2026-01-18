all:	wozmon.mon wozmon-serial.mon wozmon-apple1.mon wozmon-apple2.mon wozmon-pet.mon

wozmon.mon: wozmon.bin
	bintomon -v `./getaddress wozmon.map` wozmon.bin >wozmon.mon

wozmon.bin: wozmon.o
	ld65 -C /usr/local/share/cc65/cfg/none.cfg -vm -m wozmon.map -o wozmon.bin wozmon.o

wozmon.o: wozmon.s
	ca65 -g -l wozmon.lst wozmon.s

wozmon-serial.mon: wozmon-serial.bin
	bintomon -v `./getaddress wozmon-serial.map` wozmon-serial.bin >wozmon-serial.mon

wozmon-serial.bin: wozmon-serial.o
	ld65 -C /usr/local/share/cc65/cfg/none.cfg -vm -m wozmon-serial.map -o wozmon-serial.bin wozmon-serial.o

wozmon-serial.o: wozmon-serial.s
	ca65 -g -l wozmon-serial.lst wozmon-serial.s

wozmon-apple1.mon: wozmon-apple1.bin
	bintomon -v `./getaddress wozmon-apple1.map` wozmon-apple1.bin >wozmon-apple1.mon

wozmon-apple1.bin: wozmon-apple1.o
	ld65 -C /usr/share/cc65/cfg/none.cfg -vm -m wozmon-apple1.map -o wozmon-apple1.bin wozmon-apple1.o

wozmon-apple1.o: wozmon-apple1.s
	ca65 -g -l wozmon-apple1.lst wozmon-apple1.s

wozmon-apple2.mon: wozmon-apple2.bin
	bintomon -v `./getaddress wozmon-apple2.map` wozmon-apple2.bin >wozmon-apple2.mon

wozmon-apple2.bin: wozmon-apple2.o
	ld65 -C /usr/share/cc65/cfg/none.cfg -vm -m wozmon-apple2.map -o wozmon-apple2.bin wozmon-apple2.o

wozmon-apple2.o: wozmon-apple2.s
	ca65 -g -l wozmon-apple2.lst wozmon-apple2.s

wozmon-pet.mon: wozmon-pet.bin
	bintomon -v `./getaddress wozmon-pet.map` wozmon-pet.bin >wozmon-pet.mon

wozmon-pet.bin: wozmon-pet.o
	ld65 -C /usr/share/cc65/cfg/none.cfg -vm -m wozmon-pet.map -o wozmon-pet.bin wozmon-pet.o

wozmon-pet.o: wozmon-pet.s
	ca65 -g -l wozmon-pet.lst wozmon-pet.s

clean:
	$(RM) *.o *.lst *.map *.bin

distclean: clean
	$(RM) *.mon
