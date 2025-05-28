import java.util.Random;
import java.util.Scanner;

public class ZgadywanieLiczby {
    public static void main(String[] args) {
        Random random = new Random();
        int wylosowanaLiczba = random.nextInt(100) + 1; // liczba od 1 do 100
        Scanner scanner = new Scanner(System.in);
        int proba;

        System.out.println("Zgadnij liczbę od 1 do 100:");

        while (true) {
            System.out.print("Wpisz swoją liczbę: ");
            proba = scanner.nextInt();

            if (proba < wylosowanaLiczba) {
                System.out.println("Za mała liczba.");
            } else if (proba > wylosowanaLiczba) {
                System.out.println("Za duża liczba.");
            } else {
                System.out.println("Gratulacje! Poprawna liczba.");
                break;
            }
        }

        scanner.close();
    }
}
