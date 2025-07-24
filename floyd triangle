import java.util.ArrayList;
import java.util.List;
import java.util.Scanner;

public class ExpenseTracker {
    private static List<Expense> expenses = new ArrayList<>();

    static class Expense {
        String description;
        double amount;
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        while (true) {
            System.out.println("\n** Expense Tracker **");
            System.out.println("1. Add Expense");
            System.out.println("2. View Expenses");
            System.out.println("3. Calculate Total");
            System.out.println("4. Exit");
            System.out.print("Choose an option: ");
            int choice = scanner.nextInt();

            switch (choice) {
                case 1:
                    System.out.print("Enter description: ");
                    scanner.nextLine();  // Clears the buffer
                    String desc = scanner.nextLine();
                    System.out.print("Enter amount ($): ");
                    double amount = scanner.nextDouble();
                    addExpense(desc, amount);
                    break;
                case 2:
                    viewExpenses();
                    break;
                case 3:
                    calculateTotal();
                    break;
                case 4:
                    System.out.println("Exiting...");
                    scanner.close();
                    return;
                default:
                    System.out.println("Invalid option!");
            }
        }
    }

    private static void addExpense(String desc, double amount) {
        Expense expense = new Expense();
        expense.description = desc;
        expense.amount = amount;
        expenses.add(expense);
        System.out.println("✅ Expense added!");
    }

    private static void viewExpenses() {
        if (expenses.isEmpty()) {
            System.out.println("No expenses yet!");
            return;
        }
        System.out.println("\n--- All Expenses ---");
        for (Expense expense : expenses) {
            System.out.println("- " + expense.description + ": $" + expense.amount);
        }
    }

    private static void calculateTotal() {
        double total = 0;
        for (Expense expense : expenses) {
            total += expense.amount;
        }
        System.out.println("💰 Total Expenses: $" + total);
    }
}
