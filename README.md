
import java.util.Scanner;
public class Suma {
	
	 public static final char RESPOSTA_CORRECTA = 'b';
	 public static void main (String[] args) {
		 Scanner lector = new Scanner(System.in);
		 int intents=0;
		 boolean correcte=false;
		 
		 System.out.println("Endevina la pregunta. Tens 3 intents");
		 System.out.println("Quin dels següents no és un tipus primitiu? ");
		 System.out.println("a) Enter");
		 System.out.println("b) Scanner");
		 System.out.println("c) Caràcter");
		 System.out.println("d) Booleà");
		 System.out.print("La teva resposta és l'opció: ");
		
		do { 
			 String paraula = lector.nextLine(); //Es llegeix la cadena de text.
			 if (paraula.length() == 1) { //És una paraula d'un únic caràcter?
				 char car = paraula.charAt(0); //S'extreu el caràcter.
				
				 if ((car >= 'a')&&(car <= 'd')) { //És un caràcter vàlid a-d?
					 
					 if (car == RESPOSTA_CORRECTA) { //Resposta correcta?
						 System.out.println("Correcte, la resposta era '" + RESPOSTA_CORRECTA + "'.");
						 correcte=true;					 
					 } else{
						 System.out.println("La resposta '" + car + "' és incorrecta.");
						 intents++;
					 }
					 
				 } else System.out.println("'" + car + "' és una opció incorrecta.");
			 } else { //No era un unic caracter.
				 System.out.println("\"" + paraula + "\" no és un caràcter individual.");
			 }
		 }while (intents<3 && !correcte);
		if (intents==3) System.out.println("No et queden més intents"); 
	 }
	 
	}


