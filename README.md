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
for (char character : letters) {
	System.out.println(character);
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
# 47 - Orientação Objetos - Métodos pt 04 - Retorno pt 02

O `return` pode-se ser utilizado como um `break` para métodos do tipo void.

---
# 48 - Orientação Objetos - Métodos pt 05 - Parâmetros tipo primitivo

Quando se passa variáveis de tipo primitivo dentro de classes, a variável original nunca será alterada, independentemente do que aconteça dentro do método. O que acontece é que cria-se uma cópia e passa para uma nova variável de referência que está sendo criada dentro do método.

---

# 52 - Orientação Objetos - Métodos pt 09 - Varargs

O VarArgs é indicado com `int...`, ele funciona de maneira similar a um array, sua diferença está na hora da chamada, por exemplo em uma função de somar os números de uma lista:

Com array:
```Java
public class Calculator {  
    public void SumList(int[] list) {  
        int sum = 0;  
        for ( int num : list) {  
            sum += num;  
        }  
        System.out.println(sum);  
    }  
}
```

Chamada:
```Java
public class Main {  
    public static void main(String[] args) {  
        Calculator calculadora = new Calculadora();  
        calculator.SumList(new int[] {1, 2, 3, 4, 5, 6});  
    }  
}

// Resultado 21
```

Já com VarArgs:
```Java
public class Calculadora {  
    public void SumList(int... list) {  
        int sum = 0;  
        for ( int num : list) {  
            sum += num;  
        }  
        System.out.println(sum);  
    }  
}
```

Chamada:
```Java
public class Main {  
    public static void main(String[] args) {  
        Calculadora calculadora = new Calculadora();  
        calculadora.SumList(1,2,3,4,5,6);
    }
}

// Resultado 21
```

Vale ressaltar que nada pode-se ser colocado após o VarArgs, porque ele não identifica aonde seria o fim da lista, contudo é possível coloca-lo antes.

---

# 56 - Orientação Objetos - Modificador de acesso private, get e set pt 03

Não é recomendado a chamadas dos métodos `get` dentro do próprio atributo e sim usar o `this.`, afinal ele retornará o valor em memória.

---

# 57 - Orientação Objetos - Sobrecarga de métodos

A sobrecarga de métodos são métodos com o mesmo nome e a quantidade **OU** o tipo dos parâmetros diferentes. Também é demonstrada a utilização de um método que funciona de maneira similar (para não falar idêntico) a um construtor.

---

# 59 - Orientação Objetos - Construtores pt 02 - Sobrecarga

É possível também utilizar a sobrecarga em construtores, mas para se referir a um outro construtor é utilizado o `this();` e se necessário, argumentos. Vale ressaltar que isto funciona somente para construtores

---

# 60 - Orientação Objetos - Blocos de inicialização

A execução dos objetos começam antes mesmo da execução dos construtores e os blocos de inicialização também. Os blocos de inicialização também são chamados de instância e são executados sempre na criação de um objeto, Também aprendi que há diferentes usos dos construtores, ou seja, posso ter duas maneiras ou mais de "inicializar" com construtores.

---

# 61 - Orientação Objetos - Modificador static

O modificador de acesso `static` vai fazer com que o atributo pertença a classe, logo todos os objetos iram compartilhar seu valor. Importante citar que não é recomendado o uso do `this` para acessar um atributo estático e sim a utilização do próprio objeto, exemplo:

```Java
public class Episodio {
	private String nome;
	private int episodios;
	public static int epLimite = 24;
	private int temporadas;
	
	public void imprime() {
		System.out.println("Episódios: " + this.episodios);
		System.out.println("Temporadas: " + this.temporadas);
		System.out.println("Episódios Limite: " + Episodio.epLimite);
	}
	
	// Outros códigos
}
```

---

# 62 - Orientação Objetos - Métodos estáticos

Não pode-se adicionar nenhuma variável estática a um método não estático, mas o contrário é possível. É recomendado utilizar métodos estáticos quando o método não acessa uma variável.

---

# 63 - Orientação Objetos - Bloco de inicialização estático

Blocos de inicialização podem ser estáticas, com isso ela é executada apenas uma vez quando a classe é executada pela JVM, dessa forma economizando processamento. Caso haja mais de um bloco de inicialização estático eles são executados em ordem.

Acho importante trazer uma anotação da aula:

0. Bloco de inicialização é executado quando a JVM carrega a classe
1. Alocado espaço em memória pro objeto
2. Cada atributo da classe é criado e inicializado com valores default ou que for atribuído
3. Bloco de inicialização é executado
4. Construtor é executado

---

# 65 - Orientação Objetos - Associação pt 02 - Associação unidirecional um para muitos

A associação unidirecional é algo que referencia a outro em que este outro não referencia ao algo, simplificando, um objeto chamado *Integrante* referencia a outro objeto chamado *Guilda*, mas *Guilda* não referencia a *Integrante*.

---
