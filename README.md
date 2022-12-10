# Programacao-de-Solucoes-Computacionais-Ex06-Lista05
Faça um programa que converta da notação de 24 horas para a notação de 12 horas. Por exemplo, o programa deve converter 14:25 em 2:25 P.M. A entrada é dada em dois inteiros.
import java.util.Scanner;

public class Ex06 {
    public static void main(String[] args) throws Exception {
        Scanner sc = new Scanner(System.in);
        while (true) {
            System.out.println("Informe apenas as horas no formato 24 horas: ");

            int hours = sc.nextInt();

            System.out.println("Agora informe apenas os minutos: ");
            int minutes = sc.nextInt();

            int HoursConverted = convert(hours);
            saida(hours, minutes, HoursConverted);

            System.out.println("Deseja continuar convertendo outros horários? [S/N]");
            String resp = sc.next();
            if (resp.equalsIgnoreCase("N")) {
                break;
            }
        }
        sc.close();
    }

    public static int convert(int hours) {
        if (hours > 12) {
            hours -= 12;
            return hours;
        } else {
            return hours;
        }
    }

    public static void saida(int hours, int minutes, int HoursConverted) {
        String M = "A.M";
        String N = "P.M";

        if (hours > 12) {
            System.out.println("Horas convertidas: " + HoursConverted + ":" + minutes + " " + N);

        } else {
            System.out.println(hours + ":" + minutes + " " + M);
        }
    }
}
