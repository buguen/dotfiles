# Generate tags for system libraries
# Don't forget to add your output file to tags.vim
#
# Author: Casey Link <unnamedrambler(at)gmail(dot)com>

# version of the cpp stl to generate tags for
STL_VER=4.6.1

# path to ctags binary
CTAGS=/usr/bin/ctags


# -------------------

default: all

all: qt4 stl

qt4:
	${CTAGS} -R --sort=foldcase --c++-kinds=+p --fields=+iaS --extra=+q --language-force=C++ -f qt4-tags /usr/include/Qt

boost:
	${CTAGS} -R --sort=foldcase --exclude="*typeof*" --c++-kinds=+p --fields=+iaS --extra=+q -f boost-tags /usr/include/boost

stl:
	${CTAGS} -R --c++-kinds=+p --fields=+iaS --extra=+q -f stdlibcpp-tags /usr/include/c++/${STL_VER}

clean:
	@rm qt4 boost stdlibcpp &> /dev/null

