import java.util.Scanner;

public class Notas {

    static void main() {
        Scanner scanner = new Scanner(System.in);
        double A1, A2, media;

        System.out.println("Digite a nota da A1: ");
        A1 = scanner.nextDouble();

        System.out.println("Digite a nota da A2: ");
        A2 = scanner.nextDouble();

        media = (A1 + A2);

        if (media >= 5.75 && media < 6) {
            media = 6;
        }

        if (media >= 6){
            System.out.println("Aluno aprovado com " + media);
        } else if (media < 0.75) {
            System.out.println("Aluno reprovado direto");
        } else {
            System.out.println("Aluno de recuperação");

            System.out.println("Digite a nota da avaliação final: ");
            double finalProva = scanner.nextDouble();

            if (A1 < A2){
                A1 = finalProva;
            } else {
                A2 = finalProva;
            }

            media = (A1 + A2);

            if (media >= 5.75 && media < 6) {
                media = 6;
            }

            if (media >= 6){
                System.out.println("Aluno aprovado na avaliação final " + media);
            } else {
                System.out.println("Aluno reprovado");
            }

        }

        scanner.close();
    }


}
