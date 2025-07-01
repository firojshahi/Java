import java.util.Scanner;
import java.util.Random;

public class RockPaperScissors {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        Random random = new Random();
        String[] options = {"グー", "パー", "チョキ"};

        System.out.println("じゃんけんをしましょう！");
        System.out.println("やめたい時は「exit」と入力してください。\n");

        while (true) {
            System.out.print("あなたの手を入力してください（グー、パー、チョキ）：");
            String userChoice = scanner.nextLine().trim();

            if (userChoice.equalsIgnoreCase("exit")) {
                System.out.println("遊んでくれてありがとう！");
                break;
            }

            userChoice = userChoice.substring(0, 1).toUpperCase() + userChoice.substring(1).toLowerCase();

            if (!userChoice.equals("グー") && !userChoice.equals("パー") && !userChoice.equals("チョキ")) {
                System.out.println("無効な入力です。もう一度入力してください。\n");
                continue;
            }

            String computerChoice = options[random.nextInt(3)];
            System.out.println("コンピューターの手は：" + computerChoice);

            if (userChoice.equals(computerChoice)) {
                System.out.println("あいこです！\n");
            } else if (
                (userChoice.equals("グー") && computerChoice.equals("チョキ")) ||
                (userChoice.equals("パー") && computerChoice.equals("グー")) ||
                (userChoice.equals("チョキ") && computerChoice.equals("パー"))
            ) {
                System.out.println("あなたの勝ちです！\n");
            } else {
                System.out.println("あなたの負けです！\n");
            }
        }

        scanner.close();
    }
}
