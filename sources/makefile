target: main_pp.cpp main_asm.s main_obj.o andrew_pp.cpp andrew_asm.s andrew_obj.o omar_pp.cpp omar_asm.s omar_obj.o main_exe.exe 

main_pp.cpp: main.cpp 
	g++ -E -I ../headers main.cpp -o main_pp.cpp 

main_asm.s: main_pp.cpp 
	g++ -S main_pp.cpp -o main_asm.s

main_obj.o: main_asm.s 
	g++ -c main_asm.s -o main_obj.o 



andrew_pp.cpp: andrew.cpp 
	g++ -E -I ../headers andrew.cpp -o andrew_pp.cpp 

andrew_asm.s: andrew_pp.cpp 
	g++ -S andrew_pp.cpp -o andrew_asm.s

andrew_obj.o: andrew_asm.s 
	g++ -c andrew_asm.s -o andrew_obj.o 

omar_pp.cpp: omar.cpp 
	g++ -E -I ../headers omar.cpp -o omar_pp.cpp 

omar_asm.s: omar_pp.cpp 
	g++ -S omar_pp.cpp -o omar_asm.s

omar_obj.o: omar_asm.s 
	g++ -c omar_asm.s -o omar_obj.o 

main_exe.exe: main_obj.o 
	g++ main_obj.o andrew_obj.o omar_obj.o -o main_exe.exe 

run: 
	./main_exe.exe 

clean: 
	rm main_pp.cpp main_asm.s main_obj.o andrew_pp.cpp andrew_asm.s andrew_obj.o omar_pp.cpp omar_asm.s omar_obj.o main_exe.exe 