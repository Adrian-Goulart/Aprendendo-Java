# Aprendendo-Java

[***Curso Maratona Virado no Jiraya***](https://www.youtube.com/playlist?list=PL62G310vn6nFIsOCC0H-C2infYgwm8SWW)

Estou escrevendo o que estou aprendendo nas aulas do [DevDojo](https://www.youtube.com/@DevDojoBrasil). Aulas não citadas significam que já tenho conhecimento do conteúdo apresentado.

---
#### 02 - Como Java Funciona

O Java possui a vantagem de escrever apenas uma vez e rodar em qualquer lugar, o arquivo em que escrevemos é um arquivo .java, para rodar em outros sistemas o arquivo passa por uma compilação (javac) onde passa a ser um arquivo .class (Bytecode), no qual a partir do JVM (Java Virtual Machine) consegue se comunicar com os outros sistemas, sendo que cada Sistema Operacional tem sua JVM. Para desenvolver aplicações em Java é utilizado o JDK (Java Development Kit) em que possui uma JVM, compilador e ferramentas que servem de ajuda ao desenvolvedor.

---
#### 15 - Operadores pt 01 - Relacionais

Não é possível executar uma operação após concatenar a expressão com uma String.

---
### 16 - Operadores pt 02 - Relacionais

Símbolos de operações básicas como adição, subtração, divisão, multiplicação e resto recebem o nome de **Operações Aritméticas**, enquanto as **Operações Relacionais** são comparações de valores (retornam *true* ou *false*). Padrão de nomenclatura para tipos booleanos começam com **is**.

---
### 19 - Operadores pt 05 - Atribuição

Os operadores (++) e (--) são chamados de operadores unários, por exemplo:

```Java
int contador = 0;
contador++;
```

A ordem de colocação dos sinais tem interferência no modo como é executado, enquanto for posicionado depois, será adicionado um valor somente se algo for feito em relação a variável, já quando posicionado antes será adicionado um valor sem a necessidade da variável passar por uma ação.

---
### 20 - Estruturas Condicionais pt 01 - IF

O operador de negação (!), tem a mesma função que a comparação para um valor false, exemplo:

```java
boolean bool = true;  
if (bool == false) {  
    System.out.println("Não executado");  
}
```

É a mesma coisa que:

```java
boolean bool = true;  
if (!bool) {  
    System.out.println("Não executado");  
}
```

---
### 25 - Estruturas Condicionais pt 06 - Switch

O Switch suporta somente os tipos char, int, byte, short, enum e String.

---
### 26 - Estruturas Condicionais pt 07 - Switch exercício

Por meio dos comentários aprendi que a partir do Java 14 tem o switch expression, uma maneira mais fácil e bonita da antiga maneira de tirar vantagem de uma funcionalidade do switch no qual na ausência de um ```break;``` ele continua executando. 

---
### 27 - Estruturas de Repetição pt 01 - Laços de repetição while, do while, for

O ```do while``` mesmo se a condição for falsa ela é executada ao menos uma vez , caso verdadeira continuará a ser executada até cumprir sua condição.

---
### 31 - Estruturas de Repetição pt 05 - Continue

O `continue` é o contrário do `break`, ele volta ao início da repetição e continua executando dentro do loop, quando condição estiver satisfeita, executa o resto do loop.

---
### 32 - Arrays pt 01

Arrays são sempre do tipo *reference* (e somente tipos de referência podem ser inicializados com valor nulo). Por terem mais de um valor sua nomenclatura é sempre no plural. Arrays são declaradas da seguinte forma:

```java
int[] numbers = new int [x];
```

O ***x*** representa o número de itens comportados pela lista. (Não é possível utilizar o `new` diretamente em tipos primitivos).

---
### 33 - Arrays pt 02

Valores padrões do tipos:
* byte, short, long, double, int, float = 0
* char = '\u0000' --> (Espaço em branco no Unicode)
* boolean = false
* String = null

---
### 34 - Arrays pt 03

O tamanho do array não pode ser alterado dinamicamente, contudo ele é um *objeto* e logo possui métodos.

Caso eu chame novamente uma lista, o espaço da referência antiga é perdida.

---

### 35 - Arrays pt 04 - Foreach

Um array também pode ser inicializado desta forma:

```Java
char[] letters = {'A', 'D', 'R', 'I', 'A', 'N'};
```

Ou

```Java
char[] letters = new char[]{'A', 'D', 'R', 'I', 'A', 'N'};
```

Dessa maneira já informando os valores e tamanho da lista.

O `foreach` funciona do seguinte modo para percorrer uma lista:

```Java
for (String character : letters) {
	System.out.println(num);
}
```

---

### 36 - Arrays Multidimensionais pt 01

Os arrays multidimensionais são como arrays de arrays. Para criar arrays multidimensionais basta adicionar mais colchetes (pode-se ter várias):

```Java
int[][] num = new int[3][3];
```

O primeiro valor nos colchetes a direita equivale ao tamanho do array **base**, os demais são as posições dentro deste array base e assim por diante.

Logo para percorrer esta lista fazemos:

```Java
for (int i = 0; i < num.length; i++) {
	for (int x = 0; x < num[0].length; x++) {
		System.out.println(num[i][x]);
	}
}
```

---

### 38 - Arrays Multidimensionais pt 03 - Inicialização

Para inicializar um array multidimensional precisamos fazer:

```Java
int[][] arrayInt = new int[3][];

arrayInt[0] = new int[3];
arrayInt[1] = new int[6];
arrayInt[2] = new int[9];
```

E para entender ficar melhor visualizando, o que pode-se ser feito com o seguinte código:

```Java
for (int[] arrayBase : arrayInt) {
	System.out.println("\n------");
	for (int num : arrayBase){
		System.out.print(num + " ");
	}
}
```

Também pode-se ser inicializada desta forma, já informando os valores:

```Java
arrayInt[0] = new int[]{1, 2, 3};
arrayInt[1] = new int[]{1, 2, 3, 4, 5, 6};

// Ou assim

int array = {1, 2, 3, 4, 5, 6, 7, 8, 9}

arrayInt[2] = array;
```

E para inicializar de maneira direta, faremos:

```Java
int[][] arrayInt2 = {{1, 2, 3}, {1, 2, 3, 4, 5, 6}}
```

---
