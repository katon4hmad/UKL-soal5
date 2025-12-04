# UKL-soal5
package latihanukl1;

import java.util.*;

public class soal5 {
    public static void main(String[] args) {

        Scanner input = new Scanner(System.in);
        Random rand = new Random();

        ArrayList<Integer> komputerList = new ArrayList<>();
        ArrayList<Integer> pemainList = new ArrayList<>();

        int skorKomputer = 0;
        int skorPemain = 0;

        while (skorKomputer < 5 && skorPemain < 5) {
            System.out.print("Tekan tombol apapun untuk melempar dadu...");
            input.next();

            int daduKomputer = rand.nextInt(6) + 1;
            int daduPemain = rand.nextInt(6) + 1;

            komputerList.add(daduKomputer);
            pemainList.add(daduPemain);

            System.out.println("Komputer: " + daduKomputer);
            System.out.println("Pemain  : " + daduPemain);

            if (daduKomputer > daduPemain) {
                System.out.println("Komputer menang ronde ini!");
                skorKomputer++;
            } else if (daduPemain > daduKomputer) {
                System.out.println("Pemain menang ronde ini!");
                skorPemain++;
            } else {
                System.out.println("Seri!");
            }

            System.out.println("Skor -> Pemain: " + skorPemain + " | Komputer: " + skorKomputer);
            System.out.println("---------------------------------");
        }

        System.out.println("\n=== PERMAINAN SELESAI ===");
        if (skorPemain > skorKomputer)
            System.out.println("Pemenangnya adalah PEMAIN!");
        else
            System.out.println("Pemenangnya adalah KOMPUTER!");

        System.out.println("\nRiwayat lemparan komputer: " + komputerList);
        System.out.println("Riwayat lemparan pemain  : " + pemainList);

        System.out.println("\nTotal kemenangan Pemain  : " + skorPemain);
        System.out.println("Total kemenangan Komputer: " + skorKomputer);
    }
}
