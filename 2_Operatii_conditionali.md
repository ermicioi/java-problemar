# Operații condiționali
## Operatorul `if`
######  Să se scrie un program care va citi de la tastatură valoare de tip întreg `n` și va afișa la ecran mesajul "Test passed" în cazul în care `n` este mai mare ca `0`.

_Consideră implementarea programelor care întrunesc și următoarele condiții:_
* `n` este mai mic ca `0`
* `n` este egal cu `0`
* `n` este mai mare egal cu `0`
* `n` este mai mic egal cu `0` 

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

---

<details>
<summary>Support teoretic & ajutor:</summary>
<p>Contactează autorul la email-ul <a href="mailto:andrei.ermicioi@gmail.com">andrei.ermicioi@gmail.com</a> pentru support toeretic sau ajutor.</p>
<p>Serviciu contra plată, 10 euro pentru 30 min de online call.</p>
</details>
<br />