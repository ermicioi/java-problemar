# Operații condiționali
## Operatorul `if`
**1. Să se scrie un program care va citi de la tastatură două numere de tip întreg și va afișa în consolă numărul mai mic**

_Consideră implementarea unui program care va afișa numărul mai mare._

<details>
<summary>Soluție Java:</summary>

```java
import java.util.Scanner;

public class Main {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Enter n: ");
        int n = scanner.nextInt();

        if (n > 0) {
            System.out.println("Test passed");
        }
    }

}

```
</details>
<br />



<!-- -------------------------------------------------------- -->

## Operatorul `else`

<!-- -------------------------------------------------------- -->

## Operație ternară

<!-- -------------------------------------------------------- -->

## Operatorul `switch`

**1. Să se scrie un program care va citi de la tastatură două numere de tip întreg și un operator dintre '+', '-', '\*', '/'. 
Programul va afișa în consolă rezultatul aplicării operatorului asupra numerelor introduse.**

_Exemplu: se introduc numerele întregi 5, 3 și operatorul '+', în consolă se va afișa 8_

<details>
<summary>Soluție Java:</summary>

```java
import java.util.Scanner;

public class Main {

    public static void main(final String[] args) {
        final Scanner scanner = new Scanner(System.in);

        System.out.print("Enter number x: ");
        final int x = scanner.nextInt();

        System.out.print("Enter number y: ");
        final int y = scanner.nextInt();

        System.out.print("Enter operator: ");
        final char op = scanner.next().charAt(0);

        int z = 0;
        switch (op) {
            case '+':
                z = x + y;
                break;

            case '-':
                z = x - y;
                break;

            case '*':
                z = x * y;
                break;

            case '/':
                z = x / y;
                break;

            default:
                System.err.println("Unknown operation " + op);
        }

        System.out.println("Computed value is: " + z);
    }

}

```
</details>
<br />