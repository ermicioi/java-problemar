# Operații de bază

## Afișarea la ecran și citirea de la tastatură

#### 1. Să se scrie un program care afișează in consola mesajul "Hello World!".
<details>
<summary>Soluție Java:</summary>

```java
public class Main {

    public static void main(String[] args) {
        System.out.println("Hello World");
    }

}
```
</details>
<br />

#### 2. Să se scrie un program care citește de la tastatură o valoare de tip întreg și o afișează in consola. _Adițional experimintează și cu alte tipuri de date._

<details>
<summary>Soluție Java:</summary>

```java
import java.util.Scanner;

public class Main {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Enter value of type integer: ");
        int x = scanner.nextInt();

        System.out.println("The entered value is: " + x);
    }

}
```
</details>
<br />

#### 3. Să se scrie un program care citește de la tastatură două valori de tip real, `x` și `y` și apoi le schimbă valorile și le afișează. Exemplu: se citește de la tastatură `x = 5.3` și `y = 2.1`, după înversare `x = 2.1` și `y = 5.3`.

<details>
<summary>Soluție Java:</summary>

```java
import java.util.Scanner;

public class Main {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Enter x of type float: ");
        float x = scanner.nextFloat();

        System.out.print("Enter y of type float: ");
        float y = scanner.nextFloat();

        float z = x;
        x = y;
        y = z;

        System.out.println("The swapped values are: x = " + x + " and y = " + y);
    }

}
```
</details>
<br />

<!-- ----------------------------------------------------------------------------------------- -->

## Operații aritmetice

**1. Să se scrie un program care citește de la tastatură două valori de tip întreg și afișează la ecran suma lor.** 

_Adițional experimintează cu alte tipuri de date și alte operații aritmetice precum scăderea, înmulțirea și împărțirea._

<details>
<summary>Soluție Java:</summary>

```java
import java.util.Scanner;

public class Main {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Enter x: ");
        int x = scanner.nextInt();

        System.out.print("Enter y: ");
        int y = scanner.nextInt();
        
        int z = x + y;

        System.out.println("The sum is: " + z);
    }

}

```
</details>
<br />

**2. Să se scrie un program care citește de la tastatură o valoare de tip întreg `x`, și efectuează una din operațiile 
următoare, al cărui rezultat este afișat la ecran:**

* `y = (x + 1) * 2`
* `y = x * 4 + 6 / 2`
* `y = 8 / (2 + x)`

<details>
<summary>Soluție Java:</summary>

```java
import java.util.Scanner;

public class Main {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Enter x: ");
        int x = scanner.nextInt();

        int y = (x + 1) * 2;

        System.out.println("The operation result is: " + y);
    }

}

```
</details>
<br />

**3. Să se scrie un program care citește viteza `v` (în kilometri pe oră) de la tastatură și o afișează transformată 
în metri pe secundă. Formula de calcul: `v = v * 1000 / 3600`.**

<details>
<summary>Soluție Java:</summary>

```java
import java.util.Scanner;

public class Main {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Introdu viteza in km/h: ");
        int v = scanner.nextInt();

        v = v * 1000 / 3600;

        System.out.println("Viteza in m/s: " + v);
    }

}
```
</details>
<br />

**4. Să se scrie un program care calculează valoarea expresiei `2.4 + 5 ^ 2` și o afișează la ecran, unde `^` este 
semnul la pătrat. _Adițional experimentează cu alte funcții precum "radical", "absolut", "minim' sau "maxim".**

<details>
<summary>Sugestii Java</summary>
    
<p>Biblioteca Java conține o class-ă numită <code>Math</code>, care conține un set de funcții matimatice precum <code>Math.sqrt()</code>, 
<code>Math.abs()</code>, <code>Math.min()</code> sau <code>Math.max()</code>.</p>

<p>Consideră să implementezi cîteva programe care ar folosi diverse funcții din class-a <code>Math</code>.</p>    
    
</details> 

<details>
<summary>Soluție Java:</summary>

```java
public class Main {

    public static void main(String[] args) {
        double x = 2.4 + Math.pow(5, 2);
        System.out.println("Rezultatul expresiei: " + x);
    }

}

```
</details>
<br />

**5. Să se scrie un program care calculează minimul și maximul a trei numere întregi introduse de la tastatură.**

<details>
<summary>Soluție Java:</summary>

```java
import java.util.Scanner;

public class Main {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Enter x: ");
        int x = scanner.nextInt();

        System.out.print("Enter y: ");
        int y = scanner.nextInt();

        System.out.print("Enter z: ");
        int z = scanner.nextInt();

        int max = Math.max(Math.max(x, y), z);

        System.out.println("The maximum number is: " + max);
    }

}


```
</details>
<br />

**6. Să se scrie un program care calculează câtul și restul împărțirii la 7 a unui număr întreg `n` citit de la 
tastatură.**

<details>
<summary>Soluție Java:</summary>

```java
import java.util.Scanner;

public class Main {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Enter integer number: ");
        int n = scanner.nextInt();

        int x = n / 7;
        int y = n % 7;

        System.out.println("The extent of the division is: " + x);
        System.out.println("The rest of the division is: " + y);
    }

}

```
</details>
<br />

**7. Să se scrie un program care calculează suma cifrelor unui număr întreg dat `n` din 3 cifre.**

<details>
<summary>Soluție Java:</summary>

```java
import java.util.Scanner;

public class Main {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Enter an integer number between 100 and 999: ");
        int n = scanner.nextInt();

        int x = n % 10;
        x = x + n / 10 % 10;
        x = x + n / 100 % 10;

        System.out.println("The sum is: " + x);
    }

}

```
</details>
<br />

**8. Să se scrie un program care citește de la tastatură un număr `n`, unde `0 < n < 10000` și să se afișeze la ecran 
următoarele:**

1. Ultima cifră al numărului introdus
2. Penultima cifră al numărului introdus
3. Câtul și restul împărțirii la 9 

<details>
<summary>Soluție Java:</summary>

```java
import java.util.Scanner;

public class Main {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Enter an integer number between 0 and 10000: ");
        int n = scanner.nextInt();

        System.out.println("The last digit is: " + n % 10);
        System.out.println("The second last digit is: " + n / 10 % 10);
        System.out.println("The remains of devision to 9 is: " + n % 9);
        System.out.println("The devision to 9 is: " + n / 9);
    }
}
```
</details>
<br />

**9. Să se scrie un program care citește de la tastatură un număr `n`, unde `0 < n < 10000` și să se afișeze la ecran 
următoarele:**

1. Partea întreagă a lui `n`
2. Partea fracționară a lui `n`
3. Rotungirea lui `n` la întreg

<details>
<summary>Soluție Java:</summary>

```java
import java.util.Scanner;

public class Main {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Enter n between 0 and 10000: ");
        float n = scanner.nextFloat();

        System.out.println("The whole number is: " + (int) n);
        System.out.println("The fractional side of number is: " + (n - (int) n));
        System.out.println("The rounded number is: " + Math.round(n));
    }
}
```
</details>
<br />

**10. Să se scrie un program care citește de la tastatură un număr întreg `n`, unde `100 <= n <= 999` și afișează 
răsturnatul numărului.**

Exemplu: De la tastatură este introdus numărul `123`, la ecran va fi afișat `321`.

<details>
<summary>Soluție Java:</summary>

```java
import java.util.Scanner;

public class Main {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Enter n between 100 and 999: ");
        int n = scanner.nextInt();

        int x = n % 10 * 100 + n / 10 % 10 * 10 + n / 100;
        System.out.println("Inverted number is: " + x);

    }

}
```
</details>
<br />

**11. Să se scrie un program care citeste de la tastatură un număr întreg `n`, unde 65 <= n <= 90 și afișează în consolă litera
a cărui număr de ordine în tabelul de semne ASCII este `n`.**

<details>
<summary>Soluție Java:</summary>

```java
import java.util.Scanner;

public class Main {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Enter n between 65 and 90: ");
        int n = scanner.nextInt();

        System.out.println("The letter is: " + (char) n);

    }

}
```
</details>
<br />

**12. Să se scrie un program care citește de la tastatură un caracter ce reprezintă o literă din alfabetul latin în 
registrul mare (de la A la Z) și să se afișeze în consolă numărul de ordine al acestei litere in tabelul de semne ASCII.**

<details>
<summary>Soluție Java:</summary>

```java
import java.util.Scanner;

public class Main {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        
        System.out.print("Enter one character between A and Z: ");
        final char c = scanner.nextLine().charAt(0);

        System.out.println("The ASCII position is: " + (int) c);

    }

}
```
</details>
<br />

**13. Să se scrie un program care citește de la tastatură un număr `n` care reprezintă o sumă de lei. Să se scrie un
program care va afișa în consolă list de bancnote care va reprezenta suma introdusă astfel ca numărul de bancnote să 
fie minim. Să se consider că bancnote possible sunt în valoare de 1000, 500, 200, 100, 50, 20, 10, 5, 1 lei.**

<details>
<summary>Soluție Java:</summary>

```java
import java.util.Scanner;

public class Main {

    public static void main(final String[] args) {
        final Scanner scanner = new Scanner(System.in);

        System.out.print("Enter sum: ");
        int sum = scanner.nextInt();

        System.out.println("1000: " + sum / 1000);
        sum -= sum / 1000 * 1000;

        System.out.println(" 500: " + sum / 500);
        sum -= sum / 500 * 500;

        System.out.println(" 200: " + sum / 200);
        sum -= sum / 200 * 200;

        System.out.println(" 100: " + sum / 100);
        sum -= sum / 100 * 100;

        System.out.println("  50: " + sum / 50);
        sum -= sum / 50 * 50;

        System.out.println("  20: " + sum / 20);
        sum -= sum / 20 * 20;

        System.out.println("  10: " + sum / 10);
        sum -= sum / 10 * 10;

        System.out.println("   5: " + sum / 5);
        sum -= sum / 5 * 5;

        System.out.println("   1: " + sum);
    }

}
```
</details>
<br />

<!-- ----------------------------------------------------------------------------------------- -->

## Operații pe biți

**1. Să se scrie un program care citește de la tastatură un număr întreg `n` și afișează la ecran rezultatul mișcării 
la dreapta cu un bit.**

<details>
<summary>Soluție Java:</summary>

```java
import java.util.Scanner;

public class Main {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Enter n: ");
        int n = scanner.nextInt();

        int x = n >> 1;

        System.out.println("The shifted number is: " + x);
    }

}

```
</details>
<br />

_Observă că mișcare cu un bit la dreapta coincide cu operația de împărțire la 2. Experimentează cu operația de mișcare la stânga cu un bit și observă cu ce operație aritmetică coincide._

<details>
<summary>Explicație:</summary>

Să luăm ca exemplu cifra `5` al cărei reprezentare binară este `101`. Atunci cănd mișcăm valoare cu un bit la dreapta, rezultatul obținut este `010` care coincide cu cifra `2` (mișcare la stânga cu un bit va fi rezulta în valoare `1010` care corespunde cu valoare `10` în sistemul zecimal).
</details>
<br />

**2. Să se scrie un program care va citi de la tastatură un număr întreg cu valoarea între `0` și `3`, ce va 
reprezentare starea a două întrerupătoare `A` și `B` (`0` - întrerupătoarele sunt deconectate, `1` - întrerupătorul 
`A` este conectat și `B` deconectat, `2` - întrerupătorul `A` este deconectat și `B` conectat, `3` - ambele 
întrerupătoare sunt conectate) și un număr întreg cu valoarea `1` sau `2` care va reprezenta starea conectată a 
întrerupătorului `A` sau `B`. Programul va afișa `1` dacă întrerupătorul respectiv este conectat și `0` contrar.**

_Exemplu:_ Prima valoare introdusă este `2` (reprezentarea binară `10`) și a doua valoare introdusă `1` (valoare binară `01`) atunci programul va afișa `0`.

<details>
<summary>Soluție Java:</summary>

```java
import java.util.Scanner;

public class Main {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Enter switch state (0 - 3): ");
        int x = scanner.nextInt();

        System.out.print("Enter query state 1 or 2: ");
        int y = scanner.nextInt();

        System.out.println("The state: " + (x & y));
    }

}
```
</details>

<br />

<details>
<summary>Explicație:</summary>

Ficare bit al primei cifre introduse reprezintă starea întrerupătorului `A` sau `B`, spre exemplu bitul de pe poziția 
`0` ar reprezinta starea întrerupătorului `A` și bitul de pe poziția `1` ar reprezenta starea întrerupătorului `B` 
(spre exemplu cifra `2`, reprezentarea binară `10`, are reprezenta starea întrerupătorul `A` deconectat și `B` conectat). 

Atunci cînd se execută și binar ficare bit de pe poziții corespunzătoare se verifică astfel că:

* `1 & 1 = 1` (operație sau: `1 | 1 = 1`)
* `0 & 1 = 0` (operație sau: `0 | 1 = 1`)
* `1 & 0 = 0` (operație sau: `1 | 0 = 1`)
* `0 & 0 = 0` (operație sau: `0 | 0 = 0`)

Astfel cînd `10 & 01 = 00` (zecimal `0`), iar `10 & 10 = 10` (zecimal `1`).

Această tehnică este bine cunoscută în programare cînd se vrea păstrarea unei stări binare a mai multor elemente. 

</details>
