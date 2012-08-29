sudoku
======
package pack1;

import java.util.Scanner;

import pack2.Editar;
import pack3.Play;
import pack3.Solve;

public class Interfaz {
  
	public void Menu(int[][] mat){
		Scanner sc = new Scanner(System.in);
		Editar ed=new Editar();
		Play pl = new Play();
		Solve sol=new Solve();
		
		
		
	
	System.out.println("1.Ingresar juego");
	System.out.println("2.Jugar");
	System.out.println("3.Solucionar");
	
	System.out.println("\nIngrese la opcion deseada:");
	int opc=sc.nextInt();
	switch(opc){
		case 1:mat=ed.Cargar();//Editar
			   ed.ver(mat);
			   Menu(mat);
			   break;
			   
	    case 2://ed.ver(mat);
	    	   pl.Jugar(mat);//Play.jugar
	           break;
	           
	    case 3:sol.mensaje();//Solve.resolver
	           Menu(mat);
	           break;
	}
	
	}
}
