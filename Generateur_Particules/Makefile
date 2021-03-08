CC = g++
EXEC = Particules
FLAGS = -Wall -pedantic
LIBS = -lsfml-graphics -lsfml-window -lsfml-system
STD = -std=c++17
S = src
O = obj
B = bin

all: $(O) $(B) $(O)/main.o
	$(CC) $(O)/*.o -o $(B)/$(EXEC) $(LIBS)

$(O)/main.o: $(O)/Engine.o
	$(CC) $(S)/main.cpp -c -o $(O)/main.o $(STD) $(FLAGS)

$(O)/Engine.o: $(O)/Ball.o $(O)/BallTest.o $(O)/ParticuleGenerator.o
	$(CC) $(S)/Engine.cpp -c -o $(O)/Engine.o $(STD) $(FLAGS)

$(O)/ParticuleGenerator.o: $(O)/Particule.o $(O)/Ball.o 
	$(CC) $(S)/ParticuleGenerator.cpp -c -o $(O)/ParticuleGenerator.o $(STD) $(FLAGS)

$(O)/Ball.o:
	$(CC) $(S)/Ball.cpp -c -o $(O)/Ball.o $(STD) $(FLAGS)

$(O)/BallTest.o:
	$(CC) $(S)/BallTest.cpp -c -o $(O)/BallTest.o $(STD) $(FLAGS)

$(O)/Particule.o:
	$(CC) $(S)/Particule.cpp -c -o $(O)/Particule.o $(STD) $(FLAGS)

clean: $(O) $(B)
	rm -r $(O)
	rm -r $(B)

$(O):
	mkdir $(O)

$(B):
	mkdir $(B)
