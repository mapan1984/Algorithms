default: run

objects = array.o quick_sort.o test.o

array.o: ../array.c ../array.h
	gcc -c ../array.c -o array.o
quick_sort.o: quick_sort.c quick_sort.h ../array.h
	gcc -c quick_sort.c -o quick_sort.o
test.o: test.c quick_sort.h
	gcc -c test.c -o test.o
test: $(objects)
	gcc -o test $(objects)

run: test
	./test

.PHONY: clean
clean:
	rm -rf test $(objects)
