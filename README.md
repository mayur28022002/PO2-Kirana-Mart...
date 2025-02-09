public class Kirana {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int choice;
        double total = 0;

        System.out.println("Welcome to PO2 Kirana Mart..!");
        System.out.println("1. Rice - Rs. 50/kg");
        System.out.println("2. Sugar - Rs. 40/kg");
        System.out.println("3. Wheat - Rs. 30/kg");
        System.out.println("4. Tea - Rs. 100/pack");
        System.out.println("5. Exit");

        while (true) {
            System.out.print("Enter your choice: ");
            choice = scanner.nextInt();
            
            if (choice == 5) {
                System.out.println("Thank you for shopping! Your total bill is Rs. " + total);
                break;
            }
            
            System.out.print("Enter quantity (kg or pack): ");
            int quantity = scanner.nextInt();
            
            switch (choice) {
                case 1:
                    total += quantity * 50;
                    System.out.println(quantity + " kg Rice added to cart.");
                    break;
                case 2:
                    total += quantity * 40;
                    System.out.println(quantity + " kg Sugar added to cart.");
                    break;
                case 3:
                    total += quantity * 30;
                    System.out.println(quantity + " kg Wheat added to cart.");
                    break;
                case 4:
                    total += quantity * 100;
                    System.out.println(quantity + " pack(s) Tea added to cart.");
                    break;
                default:
                    System.out.println("Invalid choice. Please try again.");
            }
        }
        
        scanner.close();
    }
}
