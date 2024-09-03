# Atividade-48

#include <stdio.h>
#include <stdlib.h>

#define MAX_FLOORS 10

typedef struct {
    int currentFloor;
} Elevator;

void moveFloor(Elevator *elevator, int floor) {
	
  if (floor >= 0 && floor < MAX_FLOORS) {
  	
    printf("O Elevador esta se movendo do andar %d para o andar %d\n", elevator->currentFloor, floor);
    elevator->currentFloor = floor;
    
  } else {
  	
    printf("o Andar Digitado e invalido... \n Digite outro andar!");
  }
}
int main() {
	
  Elevator elevator = {0}; 
  
  int floor;
  
  while (1) {
  	
  	printf("\n \nVoce esta no Elevador! \n");
    printf("Digite o andar que voce deseja ir entre (0-%d)", MAX_FLOORS - 1);
    printf("\nCaso queira sair digite -1 \n");
    scanf("%d", &floor);
    
    
    system("cls");
    
    if (floor == -1) {
      break;
    }
    moveFloor(&elevator, floor);
  }
  
  return 0;
}
