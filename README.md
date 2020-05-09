# pilas
package javaapplication25;

import java.util.Scanner;

/**
 *
 * @author Asus-lap
 */
public class JavaApplication25 {    /**
     * @param args the command line arguments
     */
    @SuppressWarnings("empty-statement")
    public static void main(String[] args) {

        Scanner Leer = new Scanner(System.in);
        int opt, tope = 0, tam = 0, A = 0, B = 0,C,j=0;
        System.out.println("tamaño del vector A");
        int[] pilaA = new int[A = Leer.nextInt()];
        System.out.println("tamaño del vector B");
        int[] pilaB = new int[B=A];
        System.out.println("  " + B);
        System.out.println("tamaño del vector C");
        int[] pilaC = new int[C = A + B];
        
        System.out.println("  " + C);

        System.out.println("elija una opcion");
        do {

            System.out.println("1-llenar \n");
            System.out.println("2-mostrar \n");
            System.out.println("3-ordenar \n");
            System.out.println("5-vaciar\n");
            System.out.println("6-Salir\n");

            switch (opt = Leer.nextInt()) {

                case 1:
                    System.out.println(" datos DE PILA A ingresado: ");

                    for (int i = 0; i < A; i++) {
                        pilaA[tope] = (int) (Math.random() * -200 + 200);
                        tope++;
                    }
                    System.out.println(" datos DE PILA B ingresado: ");
                    for (int i = 0; i < B; i++) {
                        pilaB[tam] = (int) (Math.random() * -200 + 200);

                        tam++;

                    }

                    break;
                case 2:
                    System.out.println("LOS DATOS DE PILA A SON: ");
                    for (int i = tope - 1; i >= 0; i--) {
                        System.out.println("POCISION " + i
                                + " TIENE EL DATO " + pilaA[i]);
                    }
                    System.out.println("LOS DATOS DE PILA B SON: ");
                    for (int i = tam - 1; i >= 0; i--) {
                        System.out.println("POCISION " + i
                                + " TIENE EL DATO " + pilaB[i]);
                    }
                     for (int i =0; i <A; i++){
                      pilaC[j]=pilaA[i];
                              j++;
                   }
                           for  (int i =0; i<B; i++){     
                       pilaC[j]=pilaB[i];
                       j++;
                   }
                   System.out.println("LOS DATOS DELA PILA C SON");
                   for(int i=0;i<C;i++){
                       System.out.println("POCISION " + i
                                + " TIENE EL DATO " + pilaC[i]);  
                   }
                    break;
                case 3:
                    int aux;
                  System.out.println("ORDENAR: ");
                 
                   for(int x=0; x<C; x++) {
                      for  (int i=0; i<C-1; i++){ 
                           if(pilaC[i]>pilaC[i+1]){
                               aux=pilaC[i];
                               pilaC[i]=pilaC[i+1];
                               pilaC[i+1]=aux;
                               
                           }
                           
                       }   
                }
                   int k=0;
                   System.out.println("ordenar");
                   while(k<C)
                   for(int i=0;i<C;i++){
                       System.out.println(pilaC[k]+" ");
                       k++;
                   }
                
                    break;
            }
        } while (opt != 6);
    }
}

