1、wildcard : 扩展通配符 </br>
2、notdir ： 去除路径 </br>
3、patsubst ：替换通配符</br>

i.e.
src=$(wildcard *.c ./sub/*.c) </br>
dir=$(notdir $(src)) </br>
obj=$(patsubst %.c,%.o,$(dir) ) </br>

For the first line, it will print
````
a.c b.c ./sub/sa.c ./sub/sb.c
````
That means, wildcard expends the target files in the directory ./ and ./sub

For the second line, it will print
````
a.c b.c sa.c sb.c
````
Because notdir removes the directory information frome expanded files.

For the third line, print
````
a.o b.o sa.o sb.o
````
Because patsubst changes the files with suffix .c which in the directory $(dir)  to .o.
