#include <stdio.h>
#include <stdlib.h>

double * array_new()
{
    printf("\n\nEntrou função new");
    
    double t = 10.0;
    
    double *p = (double*)malloc(t * sizeof(double));

    p[0] = 0.0;
    p[1] = 2.0;
    p[2] = 3.0;
    p[3] = 1.0;
    p[4] = 5.0;
    p[5] = 4.0;
    p[6] = 6.0;
    p[7] = 7.0;
    p[8] = 8.0;
    p[9] = 9.0;

    return p;
}

void array_print(double p[], int tamanho)
{
    printf("\nEntrou função print\n");
   
    for(int i = 0;i <= tamanho; i++){
        printf(" %.2f  ", p[i]);
    }
}

double * array_invert(double p[]){

    printf("\n\nEntrou fução invert");

    double t = 10.0;
    int inicial = 0;
    double *vet_inv = (double*)malloc(t * sizeof(double));

    for (int i = 9; i != 0; i--){
        vet_inv[inicial++] = p[i];
    }
    return vet_inv;
}

void array_copy (double p[], double p_copy[]){

    printf("\n\nEntrou função copy");

    for(int i = 0; i <= 10; i++){
        p_copy[i] = p[i];
    }

    array_print(p_copy, 9);
}

double * array_grow (double p[], int tam){
     
    printf("\n\nEntrou função grow");

    double tamanho = sizeof(p) + 1 + tam;
    double *vet_grow = (double*)malloc(tamanho * sizeof(double));

    for(int i = 0; i <= tamanho; i++){

        if(i <= sizeof(p) + 1 ){
            vet_grow[i] = p[i];
        } else {
            vet_grow[i] = 0.0;
        }
    }

    array_print(vet_grow, tamanho);

    return vet_grow;
}

double * array_sort(double p[], int tam)
{
  double temp;

  printf("\n\nEntrou Função Sort");

  printf("\n ==> Vetor Inicial <==");
  array_print(p, tam);

  for (int i = 0; i < tam; i++)
  {
    for(int j = i + 1; j < tam; j++)
    {
      if (p[i] > p[j])
      {
        temp = p[i];
        p[i]=p[j];
        p[j]=temp;
      }
    }
  }

  printf("\n ==> Vetor Ordenado <==");
  array_print(p, tam);

  return p;
}

void array_statistics(double p[], int tam, int pos){

  printf("\n\nEntrou Função Statistics");

  double *statistics = (double*)malloc(pos * sizeof(double));

  statistics[0] = p[0];
  statistics[1] = p[(tam / 2) + 1];
  statistics[2] = p[tam];

  array_print(statistics, 2);
}

double * array_duplicated(double p[], int tam){
  printf("\n\nEntrou Função Duplicated");

  double *duplicated = (double*)malloc(tam * sizeof(double));

  for(int i = 0; i <= 10; i++){
        duplicated[i] = p[i];
  }

  return duplicated;
}

int array_compare(double p[], int tam, double p2[], int tam2){
    printf("\n\nEntrou Função Compare");

    if(tam != tam2)
        return 0;

    for (int i = 0; i < tam; i++)
    {
        if (p[i] != p2[i]){
            return 0;
        }
    }

    return 1;
}

void array_shuffle(double p[], int tam){
  
    printf("\nEntrou Função Shuffle");

    double *aleatorio = (double*)malloc(tam * sizeof(double));

    for(int i = 0; i < 10; i++){
          int r = rand() % 10;

        int ok = 0;
        while(ok == 0){

        if(aleatorio[r] == 0)        
        {
          aleatorio[r] = p[i];
          ok = 1;
        }

        r = rand() % 10;
        } 
    } 

    array_print(aleatorio, 9);

}

int main(void)
{
    //OBS.: Para os testes, será necessário que sejam comentadas partes das chamadas de código por conta da falta de memória disponível, de acordo com o erro que ocorre, está sendo usado muita alocação de memória, única forma que encontrei para rodar, é ir comentando as chamadas que não serão usadas e liberando a leitura apenas das não usadas pelo código no momento. Neste caso a questão 1 nunca pode ser comentada pois todos os outros usam este mesmo vetor e trabaham com seus valores.

    //Questão 1 - array_new
    double * n1 = array_new();
    array_print(n1, 9);

    //Questão 2 - array_print - Esta sendo chamado por todas as outras funções em meio ao código.

    //Questão 3 - array_invert
    /*double * n3 = array_invert(n1);
    array_print(n3, 9);
*/
    //Questão 4 - array_copy
    /*double *n_copy = (double*)malloc(10 * sizeof(double));
    array_copy(n1, n_copy);
    */

    //Questão 5 - array_grow
    /*int tam = 10;
    double * n5 = array_grow(n1, tam);
    */

    //Questão 6 - array_sort
    /*double * n6 = array_sort(n1, 9); 
    */

    //Questão 7 - array_statistics
    /*array_statistics(array_sort(n1, 9), 9, 2);
    */

    //Questão 8 - array_duplicated
    /*double * n8 = array_duplicated(n1, 9);
    array_print(n8, 9);
    */

    //Questão 9 - array_compare
    /*int n9 = array_compare(n1, 9, n1, 9); //no segundo vetor pode passar o n3 para testar se é diferente 
    printf("\n...Return FALSE = 0 / Return TRUE = 1 : %d", n9);
    */

    //Questão 10 - array_shuffle
    /*array_shuffle(n1, 9);
    */

    return 0;
}
