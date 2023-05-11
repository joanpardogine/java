# JAVA

## Repositori a on trovareu les solucions penjades

[javaSolucions](https://github.com/joanpardogine/javaSolucions)

## Teoria de **Paquets** (**Packages**)

### [Java Paquets (**Packages**)](./java-paquets.md)

## Teoria de **Enum**

### [Java Tipus d'enumeració (**Enum**)](./java-enum.md)


[Enunciats, activitats i exercicis amb JAVA](https://docs.google.com/document/d/16LS34amjFw8euDG_pULGB0pzCmT_zRGDVfr8QhrSUas)

[Getting Started with Java in VS Code](https://code.visualstudio.com/docs/java/java-tutorial)


# [**A22** - Activitat 22: consum cotxe i preu combustible](./MP03-UF04-A22.md)

# [**A23** - Activitat 23: Sensació segons la temperatura](./MP03-UF04-A23.md)



# Java

**Java** és un llenguatge de programació de **tipus estàtic**. Vol dir que **TOTES** les variables s'han de **declarar** abans del seu ús. És per això que hem de declarar el tipus i el nom de la variable.


## Tipus de dades en Java

Els tipus de dades especifiquen les diferents mides i valors que es poden emmagatzemar a la variable. Hi ha dos tipus de tipus de dades a **Java**:

* **Tipus de dades primitius**: els tipus de dades primitius inclouen ```boolean```, ```char```, ```byte```, ```short```, ```int```, ```long```, ```float``` i ```double```.

* **Tipus de dades no primitius**: els tipus de dades no primitius inclouen ```Classes``` , ```Interfaces``` i ```Vectors```.

### Tipus de dades primitives de Java
En el llenguatge Java, els tipus de dades primitius són els components bàsics de la manipulació de dades. Aquests són els tipus de dades més bàsics disponibles en llenguatge Java .


Hi ha 8 tipus de tipus de dades primitives:

* tipus de dades ```boolean```
* tipus de dades ```byte```
* tipus de dades ```char```
* tipus de dades ```short```
* tipus de dades ```int```
* tipus de dades ```long```
* tipus de dades ```float```
* tipus de dades ```double```

![java-data-types.png](./img/java-data-types.png)

|Tipus de dada|Valor per defecte|Mida|
|:----|:----:|----:|
|```boolean```|false|1 bit|
|```char```|'\u0000'|2 bytes|
|```byte```|0|1 byte|
|```short```|0|2 bytes|
|```int```|0|4 bytes|
|```long```|0L|8 bytes|
|```float```|0.0f|	4 bytes|
|```double```|0.0d|	8 bytes|

## Literal

Un **literal** és la representació del codi font d'un valor fix; els literals es representen directament al vostre codi sense necessitat de càlcul. Com es mostra a continuació, és possible assignar un literal a una variable d'un tipus primitiu:

```java
boolean resultat = true;
char majusculaC = 'C';
byte b = 100;
short s = 10000;
int i = 100000;
```

## Operadors en Java

L'operador en Java és un símbol que s'utilitza per realitzar operacions.
Per exemple: ```+```, ```-```, ```*```, ```/``` etc.

Hi ha molts tipus d'operadors a Java que es donen a continuació:

* Operador **unari**,
* Operador **aritmètic**,
* Operador **shift** (**de canvi**),
* Operador **relacional**,
* Operador **bitwise** (**per bits**),
* Operador **lògic**,
* Operador **ternari** i
* Operador d'**assignació**.

### Precedència de l'operador Java

<table class="alt">
<tbody><tr><th>Tipus d'operador</th><th>Categoria</th><th>Precedència</th></tr>
<tr>
<td rowspan="2">Unari</td><td>postfix</td><td><code><em>expr</em>++ <em>expr</em>--</code></td>
</tr>
<tr>
<td>prefix</td><td headers="precedence"><code>++<em>expr</em> --<em>expr</em> +<em>expr</em> -<em>expr</em> ~ !</code></td>
</tr>
<tr>
<td rowspan="2">Aritmètic</td><td>multiplicatiu</td><td headers="precedence"><code>* / %</code></td>
</tr>
<tr>
<td>additiu</td><td headers="precedence"><code>+ -</code></td>
</tr>
<tr>
<td>Shift (**de canvi**)</td><td>shift</td><td headers="precedence"><code>&lt;&lt; &gt;&gt; &gt;&gt;&gt;</code></td>
</tr>
<tr>
<td rowspan="2">Relacional</td><td>comparació</td><td headers="precedence"><code>&lt; &gt; &lt;= &gt;= **```instanceof```**</code></td>
</tr>
<tr>
<td>igualtat</td><td headers="precedence"><code>== !=</code></td>
</tr>
<tr>
<td rowspan="3">Bitwise</td><td>bitwise AND</td><td headers="precedence"><code>&amp;</code></td>
</tr>
<tr>
<td>bitwise exclusive OR</td><td headers="precedence"><code>^</code></td>
</tr>
<tr>
<td>bitwise inclusive OR</td><td headers="precedence"><code>|</code></td>
</tr>
<tr>
<td rowspan="2">Lòogic</td><td>AND lògic (<code><b>I</b></code> lògic)</td><td headers="precedence"><code>&amp;&amp;</code></td>
</tr>
<tr>
<td>OR lògic (<code><b>O</b></code> lògic)</td><td headers="precedence"><code>||</code></td>
</tr>
<tr>
<td>Ternary</td><td>Ternari</td><td headers="precedence"><code>? :</code></td>
</tr>
<tr>
<td>D'assignació</td><td>assignació</td><td headers="precedence"><code>= += -= *= /= %= &amp;= ^= |= &lt;&lt;= &gt;&gt;= &gt;&gt;&gt;=</code></td>
</tr>
</tbody></table>

## Hola mon!

[Hola mon!](./00-teoria/src/t01Holamon/HolaMon.java)


```java

/**
 * @author Joan Pardo
 *
 */
public class HolaMon {
    /**
     * @param args
     */
    public static void main(String[] args) {
        System.out.println("Hola Món!");
    }

}


```

<!-- ![images](./img/java-data-types.png)


[A_Teoria_02_equals_boolean](./src/teoria/A_Teoria_02_equals_boolean.java) -->