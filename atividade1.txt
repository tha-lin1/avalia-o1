/*
Welcome to JDoodle!

You can execute code here in 88 languages. Right now you’re in the Java IDE.

  1. Click the orange Execute button ▶ to execute the sample code below and see how it works.

  2. Want help writing or debugging code? Type a query into JDroid on the right hand side ---------------->

  3.Try the menu buttons on the left. Save your file, share code with friends and open saved projects.

Want to change languages? Try the search bar up the top.
*/
public class SistemaEscolar {

    public static void main(String[] args) {
        // Notas fornecidas
        double[] notas = {9, 7, 10, 10, 9, 8, 7, 10};

        // Calculando médias bimestrais
        double[] mediasBimestrais = new double[4];
        for (int i = 0; i < 4; i++) {
            mediasBimestrais[i] = (notas[i * 2] + notas[i * 2 + 1]) / 2.0;
        }

        // Calculando médias semestrais
        double[] mediasSemestrais = new double[2];
        mediasSemestrais[0] = (mediasBimestrais[0] + mediasBimestrais[1]) / 2.0;
        mediasSemestrais[1] = (mediasBimestrais[2] + mediasBimestrais[3]) / 2.0;

        // Média final
        double mediaFinal = (mediasSemestrais[0] + mediasSemestrais[1]) / 2.0;

        // Exibindo resultados
        System.out.println("=== MÉDIAS BIMESTRAIS ===");
        for (int i = 0; i < mediasBimestrais.length; i++) {
            System.out.printf("Bimestre %d: %.2f%n", i + 1, mediasBimestrais[i]);
        }

        System.out.println("\n=== MÉDIAS SEMESTRAIS ===");
        for (int i = 0; i < mediasSemestrais.length; i++) {
            System.out.printf("Semestre %d: %.2f%n", i + 1, mediasSemestrais[i]);
        }

        System.out.println("\n=== MÉDIA FINAL ===");
        System.out.printf("Média Final: %.2f%n", mediaFinal);
    }
}
