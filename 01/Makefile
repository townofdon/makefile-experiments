# variables, work a lot like bash vars
MY_TEXT="my dude"

# top-level rule always runs by default if you just run `make` -> equivalent to `make all`
all: output.txt

output.txt: a.o b.o
# use `@` to not print the command being run
	@echo ">> creating output.txt"
	rm -f output.txt
	cat a.o > output.txt
	cat b.o >> output.txt

b.o: b.c
	@echo ">> creating b.o"
	rm -f b.o
	cat b.c > b.o
	echo "stuff" >> b.o

# % = wildcard
# $@ = target file
# $^ = dep file
%.o: %.c
	@echo ">> creating $@"
	rm -f $@
	cat $^ > $@

a.c: src.txt
	@echo ">> creating a.c"
	rm -f a.c
	cat src.txt > a.c

b.c: src.txt
	@echo ">> creating b.c"
	rm -f b.c
	echo $(MY_TEXT) > b.c

clean:
	@echo ">> cleaning up!"
	rm -f output.txt a.o b.o a.c b.c
