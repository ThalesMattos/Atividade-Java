# Atividade-Java
Atividade Java 09/03/2023

public class Exec1 {

	public static void main(String[] args) {
	
		MyIO.println("---------- Sistema para correcao de provas -----------");
		String gabarito = MyIO.readString("Insira o gabarito das 8 questoes: ").substring(0, 8);
		int aprovado = 0;
		
		for (int i = 0; i < 10; i++) {
			MyIO.println("");
			int numAluno = MyIO.readInt("Insira o numero do aluno ");
		    String gabaritoAlun = MyIO.readString("Insira o gabarito do aluno: ").substring(0, 8);
		    int acertos = 0;
			int erros = 0;
		    
		    for (int j = 0; j < 8; j++) {
		    		
		    	if (gabarito.charAt(j) == gabaritoAlun.charAt(j))
		    	 acertos ++;
		    	else 
		    	 erros ++;
		    }  
		    
		   MyIO.println("Quantidade de acertos do aluno " +numAluno+ " eh de: " + acertos);
		   MyIO.println("Quantidade de erros do aluno " +numAluno+ " eh de: " + erros);
		   if (acertos >= 5) {
			   MyIO.println("O aluno numero " +numAluno+ " foi aprovado!");
			   aprovado ++;
		   }
		   else
			   MyIO.println("O aluno numero " +numAluno+ " foi reprovado!");
		}
		
		double taxaAprov = 0;	
		taxaAprov = (aprovado * 100)/10;		
		MyIO.println("A taxa de aprovados da turma eh de: " +taxaAprov+ "%");
	}
}

import java.util.Random;

public class Exec2 {

	public static void main(String[] args) {
		
		int[][] matriz = new int[3][4];
		
		Random rand = new Random();
		
		for (int i = 0; i < matriz.length; i++) {
	       for (int j = 0; j < matriz[0].length; j++) {
	    	   matriz[i][i] = rand.nextInt(101);
	          }
	       }
	
		int maior = matriz [0][0];
		int menor = matriz [0][0];
		int linhaMaior = 0, colunaMaior = 0, linhaMenor = 0, colunaMenor = 0;
		for (int i = 0; i < matriz.length; i++) {
			for (int j = 0; j < matriz[0].length; j++) {
				if (matriz[i][j] > maior) {
                    maior = matriz[i][j];
                    linhaMaior = i;
                    colunaMaior = j;
                }
                if (matriz[i][j] < menor) {
                    menor = matriz[i][j];
                    linhaMenor = i;
                    colunaMenor = j;
                }
			}
		}
		
		MyIO.println("Matriz:");
        for (int i = 0; i < matriz.length; i++) {
            for (int j = 0; j < matriz[0].length; j++) {
                System.out.print(matriz[i][j] + " ");
            }
            MyIO.println();
        }
        MyIO.println("O maior elemento da matriz informada eh " + maior);
        MyIO.println("Sua posicao eh: [" + linhaMaior + ", " + colunaMaior + "]");
        MyIO.println("O menor elemento da matriz informada eh " + menor);
        MyIO.println("Sua posica"
        		+ "o eh: [" + linhaMenor + ", " + colunaMenor + "]");
		
		
	}
	}
  
  public class Exec3 {

	public static void main(String[] args) {
      
		String palavra = MyIO.readLine("Insira uma palavra para ser invertida: ");
		MyIO.println("Sua palavra eh: " +palavra);
		int tamanho = palavra.length();
		MyIO.print("A palavra " +palavra+ " criptografada fica: ");
		
		
		for (int i = tamanho - 1; i >= 0; i--) {
		   MyIO.print(palavra.charAt(i));
		}
			
	}

}
  
