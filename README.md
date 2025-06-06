#include<stdio.h>
int main (){

    int numeroGrenal[447], golsInter[447], golsGremio[447];
    int inter=0, gremio=0, empate=0;
    int grenal = 0;
    int novoGrenal;
    int menu, buscarGrenal[447];
    int i=0, x=0;


                    for(i = 0; i < 447; i++){
                        printf("Novo Grenal (1.Sim 2.Nao)?");
                        scanf("%i", &novoGrenal);

                            if(novoGrenal == 1){
                                printf("\nDigite o numero do grenal: ");
                                scanf("%i", &numeroGrenal[i]);
                                printf("Digite o numero de gols do Internacional: ");
                                scanf("%i", &golsInter[i]);
                                printf("Digite o numero de gols do Gremio: ");
                                scanf("%i", &golsGremio[i]);

                                if(golsInter[i] > golsGremio[i]){
                                    printf("Internacinal ganhou o grenal %i \n\n", numeroGrenal[i]);
                                    inter++;
                                }
                                else if(golsGremio[i] > golsInter[i]){
                                    printf("O Gremio ganhou o grenal %i \n\n", numeroGrenal[i]);
                                    gremio++;
                                }
                                else if(golsInter[i] == golsGremio[i]){
                                    printf("O grenal %i terminou empatado \n\n", numeroGrenal[i]);
                                    empate++;
                                }
                                grenal++;

                    }
                            else if(novoGrenal == 2){
                                printf("\n\tMenu de opcoes: \n");
                                printf("(1)Listar todos os Grenais \n");
                                printf("(2)Listar o resultado de um Grenal \n");
                                printf("(3)Visualizar Estatisticas \n");
                                printf("(4)Sair \n");
                                scanf("%i", &menu);


                                if(menu == 1){
                                    for(i=0; i < grenal; i++){
                                        printf("Grenal %i: Interncioanl %i x %i Gremio \n", numeroGrenal[i], golsInter[i], golsGremio[i]);
                                    }
                                    return 1;
                                }
                                else if(menu == 2){
                                    printf("Digite o numero do grenal que deseja buscar: ");
                                    scanf("%i", &buscarGrenal[x]);

                                    i=x;

                                    printf("Grenal %i: \nInternacional %i x %i Gremio", numeroGrenal[i], golsInter[i], golsGremio[i]);
                                    return 1;
                                }
                                else if(menu == 3) {
                                    printf("Estatisticas gerais:\nVitorias Internacional: %i / Gols Interncioanl: %i\nVitorias Gremio: %i / Gols Gremio: %i\nEmpates: %i", inter, golsInter, gremio, golsGremio, empate);
                                    return 1;
                                }
                                else if(menu == 4){
                                    printf("Programa Encerrado");
                                    return 1;
                                }
                        }
                    }





return 0;
}
