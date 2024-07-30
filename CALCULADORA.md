#include <stdio.h>
#include <stdlib.h>
#include <math.h>
#include <locale.h>
#define POTENCIA 2
int main()
{
    //const int POTENCIA = 2;
    //esto es un comentario de una linea
    /*
        comentario de
        más de una línea
        */
    setlocale(LC_ALL, "spanish");
    int ca=0;
    int co=0;
    float hi, sup, per = 0;

    printf("INGRESE EL VALOR DEL CATETO ADYACENTE: ");
    scanf("%i",&ca);
    if(ca < 0){
        printf("EL CATETO NO PUEDE SER NEGATIVO\n");
        return -1;
    }else{
        if(ca == 0){
            printf("EL CATERO NO PUEDE SER CERO \n");
            return -1;
        }
    }
    printf("INGRESE EL VALOR DEL CATETO OPUESTO: ");
    scanf("%i",&co);
    if(co <= 0){
        printf("EL CATETO NO PUEDE SER NEGATIVO\n");
        return -1;
    }else{
        if(co == 0){
            printf("EL CATERO NO PUEDE SER CERO \n");
            return -1;
        }
    }

    hi = (float) sqrt((float) pow(ca,POTENCIA)+ (float) pow(co,POTENCIA));
    sup = (float) (ca*co)/2;
    per = (float) ca + (float) co + hi;

    printf("EL VALOR DEL CATETO ADYACENTE ES: %i cm\n",ca);
    printf("EL VALOR DEL CATETO OPUESTO ES: %i cm\n",co);
    printf("EL VALOR DE LA HIPOTENUSA ES: %f cm\n",hi);
    printf("EL VALOR DE LA SUPERFICIE ES: %f cm*2 \n", sup);
    printf("EL VALOR DEL PERÍMETRO ES: %f cm \n", per);
    system("pause");
    return 0;
}
