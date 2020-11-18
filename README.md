# poo1-2
aulas
/*
1 - Tendo como dado de entrada a altura, peso e sexo, 
construa um algoritmo que calcule o peso ideal, utilizando as seguintes fórmulas:
Para homens: (72.7*h) - 58 
Para mulheres: (62.1*h) - 44.7 
(h = altura)
Ao final o algoritmo deve mostrar:
- Altura, peso e sexo;
- Peso Ideal;
Mensagem se está acima, abaixo ou no peso ideal; */

import java.util.Scanner;

public class Peso_ideal {

	public static void main(String[] args) {
		
		Scanner entrada = new Scanner(System.in);
		
		char sexo;
		float peso; 
		double h; 			//altura
		double pesoIdealHomem;
		double pesoIdealMulher;
		
		System.out.print("informe o sexo: (m ou h): ");
		sexo = entrada.nextLine().charAt(0);
		
		System.out.print("informe a altura: ");
		h = entrada.nextDouble();
		
		System.out.print("informe o peso: ");
		peso = entrada.nextFloat();
		
		pesoIdealHomem = (peso* h) - 58 ;
		pesoIdealMulher = (peso * h) - 44.7;
		
		if (sexo == 'm' ){
			System.out.println("o peso ideal para esta mulher é: " + pesoIdealMulher);
		}else { 
			
			if (sexo == 'h'){
				System.out.println("o peso ideal para este homem é: " + pesoIdealHomem);
			}
		}

	}

}
