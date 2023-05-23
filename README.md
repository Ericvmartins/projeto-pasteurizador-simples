# Projeto Pasteurizador Simples 
Código feito em C


#include <stdio.h>
#include <stdlib.h>
#include <locale.h>

#define vermelho "\x1b[31m"
#define verde "\x1b[32m"
#define ciano "\x1b[36m"
#define reset "\x1b[0m"

int main () {
	
	setlocale(LC_ALL, "Portuguese");
    
	int tanque, vazao, resposta, pressao;
	float quente, frio;
	
	system ("cls");
	printf ("-------Pasteurizador-------\n");
	printf ("\nSeu tanque está cheio?\n");
	printf (verde "\n1 - Sim" reset);
	printf (vermelho "\n0 - Não" reset);
	printf ("\n\nResposta: "); 
	scanf ("%d", &resposta);
	
	if (resposta == 0) {
		printf ( ciano "\nAguardando o enchimento do tanque.\n\n" reset);
		system ("pause");
	}
	
	system ("cls");
	printf (ciano "A bomba está ligada.\n" reset);
	
	printf ("\nA vazão está correta?\n");
	printf (verde "\n1 - Sim" reset);
	printf (vermelho "\n0 - Não" reset);	
	printf ("\n\nResposta: ");
	scanf ("%d", &resposta);
	
	if (resposta == 0) {
		printf (ciano "\nVazão sendo ajustada...\n\n" reset);
		system ("pause");
	}
	
	system ("cls");
	
	printf ("\nA pressão está correta?\n");
	printf (verde "\n1 - Sim" reset);
	printf (vermelho "\n0 - Não\n" reset);	
	printf ("\nResposta: ");
	scanf ("%d", &resposta);
	
	if (resposta == 0) {
		printf (ciano "\nPressão sendo ajustada...\n\n" reset);
		system ("pause");
	}
	
	system ("cls");
	
	printf ("\nInsira o valor da temperatura do tanque de aquecimento: ");
	printf ("\n\nResposta: ");
	scanf ("%f",&quente);
	
	if (quente >= 75) {
		printf(ciano "\nDesligar o aquecedor\n\n" reset);
		system ("pause");
	} else {
		printf(ciano "\nLigar o aquecedor\n\n" reset);
		system ("pause");
	}
	system ("cls");
	
	printf ("\nInsira o valor da temperatura do tanque de resfriamento: ");
	printf ("\n\nResposta: ");
	scanf ("%f",&frio);
	
	if (frio <= -4) {
		printf(ciano "\nDesligar o resfriador\n\n" reset);
		system ("pause");
	} else { 
		printf(ciano "\nLigar o resfriador\n\n" reset);
		system ("pause");
	}
	
	system ("cls");
	
	printf ("Deseja encerrar o processo de pasteurização?\n\n");
	printf (verde "\n1 - Sim" reset);
	printf (vermelho "\n0 - Não" reset);
	printf ("\n\nResposta: "); 
	scanf ("%d", &resposta);
	
	if (resposta == 0) { 
		main ();
	} else {
		printf(vermelho "\nProcesso encerrado!" reset);
		return 0;
	}
	
}
