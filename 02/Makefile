# You can use a Makefile to automate useful commands
# Try:
# - make diff
# - make distribute

all: fakefile.txt

fakefile.txt:
	rm -f fakefile.txt
	echo "fake" > fakefile.txt

clean:
	rm -f fakefile.txt dist.tgz

diff:
	$(info The status of the repository, and the volume of per-file changes:)
	@git status
	@git diff --stat

distribute: clean
	tar zcvf dist.tgz *
