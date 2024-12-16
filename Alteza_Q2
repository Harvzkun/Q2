import java.util.Scanner;

public class CreaturePower {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int[] powerLevels = new int[10];

        // Input the power levels
        System.out.println("Enter 10 power levels of creatures:");
        for (int i = 0; i < 10; i++) {
            powerLevels[i] = scanner.nextInt();
        }

        // Bubble Sort in ascending order
        bubbleSortAscending(powerLevels);
        System.out.println("\nBubble Sort (Ascending):");
        displayArray(powerLevels);

        // Selection Sort in descending order
        selectionSortDescending(powerLevels);
        System.out.println("\nSelection Sort (Descending):");
        displayArray(powerLevels);

        // Calculate and display analysis
        calculateAndDisplayAnalysis(powerLevels);
    }

    // Bubble Sort in ascending order
    public static void bubbleSortAscending(int[] arr) {
        int n = arr.length;
        for (int i = 0; i < n - 1; i++) {
            for (int j = 0; j < n - i - 1; j++) {
                if (arr[j] > arr[j + 1]) {
                    // Swap arr[j] and arr[j + 1]
                    int temp = arr[j];
                    arr[j] = arr[j + 1];
                    arr[j + 1] = temp;
                }
            }
        }
    }

    // Selection Sort in descending order
    public static void selectionSortDescending(int[] arr) {
        int n = arr.length;
        for (int i = 0; i < n - 1; i++) {
            int maxIndex = i;
            for (int j = i + 1; j < n; j++) {
                if (arr[j] > arr[maxIndex]) {
                    maxIndex = j;
                }
            }
            // Swap arr[maxIndex] and arr[i]
            int temp = arr[maxIndex];
            arr[maxIndex] = arr[i];
            arr[i] = temp;
        }
    }

    // Display the array
    public static void displayArray(int[] arr) {
        for (int num : arr) {
            System.out.print(num + " ");
        }
        System.out.println();
    }

    // Calculate and display analysis
    public static void calculateAndDisplayAnalysis(int[] arr) {
        int sumEven = 0;
        int sumOdd = 0;
        int min = arr[0];
        int max = arr[0];

        for (int num : arr) {
            if (num % 2 == 0) {
                sumEven += num;
            } else {
                sumOdd += num;
            }
            if (num < min) {
                min = num;
            }
            if (num > max) {
                max = num;
            }
        }

        System.out.println("\nAnalysis:");
        System.out.println("Sum of Even Numbers: " + sumEven);
        System.out.println("Sum of Odd Numbers: " + sumOdd);
        System.out.println("Min Power Level: " + min);
        System.out.println("Max Power Level: " + max);
    }
}
