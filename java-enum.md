# Java Tipus d'enumeració (**Enum**)

Un **tipus d'enumeració** és un **tipus de dades especial** que permet que una variable sigui un conjunt de constants predefinides. La variable ha de ser igual a un dels valors que s'hi hagin predefinit. Els exemples habituals inclouen les direccions de la brúixola (valors de **```NORD```**, **```SUD```**, **```EST```** i **```OEST```**) i els dies de la setmana.

Com que són constants, els noms dels camps d'un tipus d'**```enum```** estan en majúscules.

Al llenguatge de programació Java, definiu un tipus d'**```enum```** mitjançant la paraula clau **```enum```**. Per exemple, especificaríeu un tipus d'enumeració de dies de la setmana com:

```java
public enum Dia {
     DIUMENGE, DILLUNS, DIMARTS, DIMECRES,
     DIJOUS, DIVENDRES, DISSABTE
}
```

