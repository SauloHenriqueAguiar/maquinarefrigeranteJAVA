# maquinarefrigeranteJAVA


package com.mycompany.maquinarefrigerante;

import java.util.Scanner;


public class LojadeConveniencia {
    public static void main(String args[]){
        Scanner teclado = new Scanner(System.in);
        MaquinadeRefri m = new MaquinadeRefri();
        int opcao,res;
        float valor;
        
        do{
        
            
        System.out.println(m.mostraInfo());
        System.out.println("Digite 99 para inserir crédito");
        System.out.println("Digite -1 para sair");
        System.out.println("Ou digite o numero do refri para comprar (0-4)");

        opcao = teclado.nextInt();        
         switch(opcao){
             case 0:
             case 1:
             case 2:
             case 3:
             case 4:
                  res =  m.comprar(opcao);
            switch (res) {
                case 0:
                    System.out.println("ENJOY!");
                    break;
                case -1:
                    System.out.println("Saldo insuficiente!");
                    break;
                default:
                    System.out.println("desculpe regrifegante em falta!");
                    break;
            }
                  

             case 99:
             System.out.println("Digite um valor: ");
             valor = teclado.nextFloat();
             m.inserirCredito(valor);
             break;
             case -1:
                 System.out.println("Obrigado por utilizar a maquina");
                 System.out.println("receba o troco" + m.solicitarTroco());
                 break;
             default:
                 System.out.println("Opção invalida!");
                 break;
         }   
        
        } while(opcao != -1);
        
        }
}
        
