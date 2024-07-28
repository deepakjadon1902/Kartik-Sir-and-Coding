import java.util.Scanner;
import java.util.Stack;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        
        int Q = scanner.nextInt();  // Number of queries
        Stack<Integer> moduleStack = new Stack<>();
        
        for (int i = 0; i < Q; i++) {
            int queryType = scanner.nextInt();
            
            if (queryType == 1) {  // Student Query
                if (moduleStack.isEmpty()) {
                    System.out.println("No Code");
                } else {
                    System.out.println(moduleStack.pop());
                }
            } else if (queryType == 2) {  // Instructor Query
                int cost = scanner.nextInt();
                moduleStack.push(cost);
            }
        }
        
        scanner.close();
    }
}
