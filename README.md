
package jsjc;

import java.util.Scanner;

public class JSJC {

    public static void main(String[] args) {
        Scanner entrada = new Scanner(System.in);
        Scanner tipojuros = new Scanner(System.in);
        Scanner valores = new Scanner(System.in);
        String teclado, rep;
        double C, i, j, M;
        int t;

        System.out.println("Digite Y para calcular ou N para sair ");
        rep = entrada.nextLine();

        while (rep.equals("Y")) {

            System.out.println("Digite JS para Juros Simples, e JC para calcular Juros Compostos: ");
            teclado = tipojuros.nextLine();

            if (teclado.equals("JS")) {

                System.out.println("Digite o capital inicial: ");
                C = valores.nextDouble();

                System.out.println("Digite a taxa de juros: ");
                i = valores.nextDouble();

                System.out.println("Digite o tempo em meses: ");
                t = valores.nextInt();

                j = C * i * t;
                M = C + j;

                System.out.println("O montante após " + t + " meses vai ser de " + M);
            } else if (teclado.equals("JC")) {

                System.out.println("Digite o capital inicial: ");
                C = valores.nextDouble();

                System.out.println("Digite a taxa de juros: ");
                i = valores.nextDouble();

                System.out.println("Digite o tempo em meses: ");
                t = valores.nextInt();

                M = C * (Math.pow((1 + i), t));

                System.out.println("O montante após " + t + " meses vai ser de " + M);

            }

            System.out.println("Digite Y para calcular ou N para sair ");
            rep = entrada.nextLine();
        }
    }
}
    

