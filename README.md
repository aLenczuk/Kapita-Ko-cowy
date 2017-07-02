# Kapita-Ko-cowy

import java.util.Scanner;

public class KapitałKońcowy
{

	public static void main(String[] args)
	{
		Scanner input= new Scanner(System.in);
		
		System.out.println("Wpisz: \n- \"KP\", aby obliczyć kapitał początkowy, \n- \"KK\", aby obliczyć kapitał koncowy, \n- \"P\", aby     obliczyć oprocentowanie lokat w skali rocznej: ");
		
		String wybór= input.nextLine();
		
		switch(wybór){
		
		case "KP":
			System.out.println("Podaj liczbę lat, na ile była złożona lokata: ");
			double nKP= input.nextDouble();
			System.out.println("Podaj oprocentowanie lokaty w skali rocznej(bez %): ");
			double pKP= input.nextDouble();
			System.out.println("Podaj kapitał końcowy: ");
			double kkKP= input.nextDouble();
			double KP= kkKP/Math.pow((1+(pKP/100)), nKP);
			double odsetkiKP= kkKP-KP;
			System.out.println("Kapitał początkowy lokaty: " + KP + " zł");
			System.out.println("Odsetki: " + odsetkiKP + " zł");
			break; 
		case "KK":
			System.out.println("Podaj liczbę lat, na ile była zlożona lokata: ");
			double nKK= input.nextDouble();
			System.out.println("Podaj oprocentowanie lokaty w skali rocznej(bez %): ");
			double pKK= input.nextDouble();
			System.out.println("Podaj kapitał początkowy: ");
			double kpKK= input.nextDouble();
			double KK= kpKK*(Math.pow(1+(pKK/100), nKK));
			double odsetkiKK= KK-kpKK;
			System.out.println("Kapitał końcowy lokaty: " + KK + " zł");
			System.out.println("Odsetki: " + odsetkiKK + " zł");
			break;
		case "P":
			System.out.println("Podaj liczbę lat, na ile była złożona lokata: ");
			double nP= input.nextDouble();
			System.out.println("Podaj kapitał początkowy: ");
			double kpP= input.nextDouble();
			System.out.println("Podaj kapitał końcowy: ");
			double kkP= input.nextDouble();
			double P= Math.round((Math.pow((kkP/kpP), 1/(double)nP)-1)*100);
			double odsetkiP= kkP-kpP;
			System.out.println("Oprocentowanie w skali rocznej lokaty: " + P + " %");
			System.out.println("Odsetki: " + odsetkiP + " zł");
			break;
		}
		
	}

}
