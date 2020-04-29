target: main_pp.cpp main_asm.s main_obj.o main_exe.exe

main_pp.cpp: main.cpp sources/omar.cpp sources/andrew.cpp
	g++ -E -I headers main.cpp sources/omar.cpp sources/andrew.cpp -o main_pp.cpp 

main_asm.s: main_pp.cpp 
	g++ -S main_pp.cpp -o main_asm.s

main_obj.o: main_asm.s 
	g++ -c main_asm.s -o main_obj.o 

main_exe.exe: main_obj.o 
	g++ main_obj.o -o main_exe.exe 

run: 
	./main_exe.exe 

clean: 
	rm main_pp.cpp main_asm.s main_obj.o main_exe.exe