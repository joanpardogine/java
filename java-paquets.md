# Java Paquets **Packages**

## Paquets Java i API

S'utilitza un paquet en **Java** per agrupar **classes relacionades**. Penseu en això com una **carpeta en un directori** de fitxers. Utilitzem paquets per evitar conflictes de noms i per escriure un codi que sigui molt més fàcil de mantenir. Els paquets es divideixen en dues categories:

**1.** [Paquets integrats](./java-paquets.md#1-paquets-integrats) (paquets de l'API de Java)
**1.** [Paquets definits per l'usuari](./java-paquets.md#2-paquets-definits-per-lusuari) (creeu els vostres propis paquets)

## **1.** Paquets integrats

L'**```API```** de **Java** és una **biblioteca de classes** escrites prèviament, d'ús gratuït, inclosa a l'entorn de desenvolupament de Java.

La biblioteca conté components per gestionar l'entrada, la programació de bases de dades i molt més. La llista completa es pot trobar al lloc web d'**Oracle**: [https://docs.oracle.com/javase/8/docs/api/](https://docs.oracle.com/javase/8/docs/api/).

La biblioteca està dividida en paquets i classes. És a dir, es pot importar una sola classe (juntament amb els seus mètodes i atributs) o un paquet sencer que contingui totes les classes que pertanyen al paquet especificat.

Per utilitzar una classe o un paquet de la biblioteca, heu d'utilitzar la **paraula clau** **```import```**:

> **Sintaxi**
> ```java
> import paquet.nom.Class;   // Importa només una classe
> import package.nom.*;   // Importa un paquet sencer
> ```

### Importa una classe

Si trobeu una classe que voleu utilitzar, per exemple, la classe **```Scanner```**, que s'utilitza per obtenir l'entrada de l'usuari, escriviu el codi següent:

> **Exemple**
> ```java
> import java.util.Scanner;
> ```

A l'exemple anterior, **```java.util```** és un paquet, mentre que **```Scanner```** és una classe del paquet **```java.util```**.

Per utilitzar la classe **```Scanner```**, cal crear un objecte de la classe i utilitzar qualsevol dels mètodes disponibles que es troben a la documentació de la classe **```Scanner```**. En el nostre exemple, utilitzarem el mètode **```nextLine()```**, que s'utilitza per llegir una línia completa:

> **Exemple**
> Utilitzant la Scannerclasse per obtenir l'entrada de l'usuari:
> ```java
> import java.util.Scanner;
> 
> class LaMevaClasse {
>   public static void main(String[] args) {
>     Scanner teclat = new Scanner(System.in);
>     System.out.print("Entra el teu nom: ");
> 
>     String nomUsuari = teclat.nextLine();
>     System.out.println("El teu nom és: " + nomUsuari);
>   }
> }
>```

### Importa un paquet

Hi ha molts paquets per triar. A l'exemple anterior, hem utilitzat la classe **```Scanner```** del paquet **```java.util```**. Aquest paquet també conté funcions de data i hora, generador de nombres aleatoris i altres classes d'utilitat.

Per importar un paquet sencer, acabeu la frase amb un asterisc (**```*```**). L'exemple següent importarà **TOTES** les classes del paquet **```java.util```**:

> **Exemple**
>```java
> import java.util.*;
>``` 

## **2.** Paquets definits per l'usuari

Per crear el vostre propi paquet, cal entendre que Java utilitza un directori del sistema de fitxers per emmagatzemar-los. Igual que les carpetes del vostre ordinador:

```
└── root
  └── el_meu_paquet
    └── ElMeuPaquetClasse.java
```

Per crear un paquet, utilitzeu la paraula clau **```package```**:

> Contingut del fitxer **```ElMeuPaquetClasse.java```**
> ```java
> package el_meu_paquet;
> class ElMeuPaquetClasse {
>   public static void main(String[] args) {
>     System.out.println("Aquest és el meu paquet!");
>   }
> }
> ```

Gaurdeu el fitxer com a **```ElMeuPaquetClasse.java```** i compileu-lo:

```
javac ElMeuPaquetClasse.java
```

A continuació, compileu el paquet:

```
javac -d . ElMeuPaquetClasse.java
```

> Això obliga al compilador a crear el paquet "**```el_meu_paquet```**".
> 
> La paraula clau **```-d```** especifica la destinació d'on desar el fitxer de classe. Podeu utilitzar qualsevol nom de directori, com ara ```c:\user``` (windows), o, si voleu mantenir el paquet dins del mateix directori, podeu utilitzar el signe de punt "**```.```**", com a l'exemple anterior.
> 
> **Nota**: El nom del paquet s'ha d'escriure en minúscules per evitar conflictes amb els noms de classe.

Quan vam compilar el paquet de l'exemple anterior, es va crear una carpeta nova, anomenada **```el_meu_paquet```**.

Per executar el fitxer **```ElMeuPaquetClasse.java```**, escriviu el següent:
```java
java el_meu_paquet.ElMeuPaquetClasse
```
La sortida serà:

```
Aquest és el meu paquet!
```

### Passem a veure-ho amb un exemple complert

```
└── root
  |   AppMenus.java
  └── menu_joan
    └── GestioDeMenus.java
```

## Contingut del fitxer **```GestioDeMenus.java```**

```java
package menu_joan; // indiquem que es troba a una carpeta anomenada menu_joanpackage utils_joan; // indiquem que es troba a una carpeta anomenada utils_joan

import java.util.InputMismatchException;
import java.util.Scanner;
/**
 * @author: Joan Pardo
 */
public class GestioDeMenus {
    
    // Atributs   --> No en té!
    
    // Constructor
    private GestioDeMenus(){
        // Una IllegalStateException és una excepció en
        // temps d'execució a Java que es llança per indicar
        // que s'ha invocat un mètode en el moment equivocat.
        // Aquesta excepció s'utilitza per indicar que es
        // crida un mètode en un moment il·legal o inadequat.
        throw new IllegalStateException("Utility class");
    }
    
    // Setters i Getters    --> No en té ja que no té atributs!!
    // Mètodes
    /**
     * @author Joan Pardo
     * @param  vectorOpcions  Es tracta d'un vector que conté totes les opcions a mostrar.
     * @param  titol Cadena que s'imprimirà just abans del llistat del menú,
     *           com si fos el títol del menú.
     * @param  missatge Cadena que s'imprimirà després del llistat del menú,
     *           i just abans de les opcions.
     * @return  <pre>int</pre>
     *          Es tracta del valor que ha introduït l'usuari, en funció
     *              de la posició del menú que ha escollit.
     */
    public static int entraOpcioMenu(String[] vectorOpcions, String titol, String missatge) {
        Scanner teclat = new Scanner(System.in);
        int max = vectorOpcions.length;
        int min = 1;
        int opcioEscollida;
        opcioEscollida = -1;
        boolean esCorrecte;
        do {
            System.out.println(titol);
            mostraMenu(vectorOpcions);
            try {
                esCorrecte = true;
                System.out.print(missatge + " (1.." + max + "): ");
                opcioEscollida = teclat.nextInt();
                // if( (min<=opcioEscollida) && (opcioEscollida<=max)) {
                if ((min > opcioEscollida) || (opcioEscollida > max)) {
                    System.out.println("Error!! Cal que entris una de les opcions diponibles!");
                    esCorrecte = false;
                }
            } catch (InputMismatchException esUnaLletra) {
                System.out.println("Error!! Cal que entris un nombre enter!");
                esCorrecte = false;
            } finally {
                teclat = new Scanner(System.in); // Per "netejar" el "teclat"!
            }
        } while (!esCorrecte);
        teclat.close();
        return opcioEscollida;
    }

    private static void mostraMenu(String[] vectorOpcions) {
        for (int i = 0; i < vectorOpcions.length; i++) {
            System.out.println((i + 1) + " - " + vectorOpcions[i]);
        }
    }
}
```

## Contingut del fitxer **```AppMenus.java```**

```java
import menu_joan.GestioDeMenus; // Importem de la carpeta menu_joan, la Classe 

public class AppMenus {
    public static void main(String[] args) {
        String[] nomMesos = {
            "gener","febrer","març",
            "abril","maig","juny",
            "juliol","agost","setembre",
            "octubre","novembre","desembre"
        };

        int opcioEntrada;

        opcioEntrada = GestioDeMenus.entraOpcioMenu(nomMesos,"ESCULL UN MES","Entra una de les següents opcions");

        System.out.println("Has entrat l'opció " + opcioEntrada + " és a dir " + nomMesos[opcioEntrada-1]);
    }
}
```