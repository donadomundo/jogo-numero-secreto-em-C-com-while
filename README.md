# jogo-numero-secreto-em-C-com-while




#include <stdio.h>
#include <stdlib.h>

int main()
{
    printf("-------------------------------------------\n");
    printf("bem vindo ao jogo adivinhe o numero secreto\n");
    printf("-------------------------------------------\n");
    printf("digite um numero que voce acha que eh o numero secreto. voce tem 3 tentativas. boa sorte!\n\n");


    int NumeroSecreto = 42;

    int Chute;

    int ganhou = 0;

    int tentativas =1;
    while (ganhou == 0)
    {
        printf("tentativa %d\n", tentativas);
        printf("qual seu chute?\n");

        scanf("%d", &Chute);
        printf("seu chute foi %d\n\n", Chute);

        if(Chute < 0)
        {
            printf("voce nao pode chutar números negativos\n\n");
            continue; //faz o for continuar.
        }


        int acertou = (Chute == NumeroSecreto);
        int maior = Chute > NumeroSecreto;

         if(acertou)
        {

            printf("parabens, voce acertou o numero secreto\n\n");

            ganhou = 1; //faz o mesmo que o break
        }



        else if(maior)
        {

            printf("o numero escolhido foi mais alto, tente um menor.\n\n");
        }
            else
            {
                printf("o numero escolhido foi menor, tente um  maior.\n\n");
            }
            tentativas = tentativas + 1;
        }
        printf("fim de jogo\n\n");
        printf("voce acertou em %d tentativas", tentativas - 1);
    }



