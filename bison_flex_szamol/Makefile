all: szamol

szamol.tab.c szamol.tab.h:	szamol.y
	bison -t -v -d szamol.y

lex.yy.c: szamol.l szamol.tab.h
	flex szamol.l

szamol: lex.yy.c szamol.tab.c szamol.tab.h
	gcc -o szamol szamol.tab.c lex.yy.c -lm

clean:
	rm szamol szamol.tab.c lex.yy.c szamol.tab.h szamol.output
