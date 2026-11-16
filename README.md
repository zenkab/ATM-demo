import java.util.Scanner;

/**
 * demo enos ATM trapezas
 * emfanizoume menou epilogwn gia analipsi kai katathesi
 * kai to programma ilopoiei tin epilogi kai dinei kai feedback ston xristi
 *
 */
public class AtmApp {
    public static void main(String[] args) {

        Scanner input = new Scanner(System.in);

        int ballance = 0;
        int choise = 0;
        int amount = 0;

        while (true) {
            System.out.println("\n------ATM MENU-----");
            System.out.println("1. Αναλυψη");
            System.out.println("2.Καταθεση");
            System.out.println("3.Εξοδος");
            System.out.println("Επιλογη");

            choise = input.nextInt();

            if (choise == 3) {
                System.out.println("Εξοδος");
                System.out.println("Ευχαριστουμε για την συναλαγη");
                break;
            }
            switch (choise) {
                case 1:
                    System.out.println("Εισαγετε ποσο αναληψης");
                    amount = input.nextInt();

                    if (amount <= 0) {
                        System.out.println("Το ποσο πρεπει να ειναι θετικο");
                        continue;
                    }

                    if (amount > ballance) {
                        System.out.println("Ανεπαρκες υπολοιπο");
                        continue;
                    }

                    ballance -= amount;
                    System.out.println("Το νεο υπολοιπο ειναι : " + ballance);
                    break;

                case 2:
                    System.out.println("Εισαγετε ποσο καταθεσης");
                    amount = input.nextInt();

                    if (amount <= 0) {
                        System.out.println("Το ποσο πρεπει να ειναι θετικο");
                        continue;
                    }

                    ballance += amount;
                    System.out.println("Το νεο υπολοιπο ειναι \n" + ballance);
                    break;
            }
        }
    }

}# ATM-demo
