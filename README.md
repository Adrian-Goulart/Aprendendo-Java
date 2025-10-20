# Aprendendo-Java

[***Curso Maratona Virado no Jiraya***](https://www.youtube.com/playlist?list=PL62G310vn6nFIsOCC0H-C2infYgwm8SWW)

Estou escrevendo o que estou aprendendo nas aulas do [DevDojo](https://www.youtube.com/@DevDojoBrasil). Aulas não citadas significam que já tenho conhecimento do conteúdo apresentado.
#### 02 - Como Java Funciona

O Java possui a vantagem de escrever apenas uma vez e rodar em qualquer lugar, o arquivo em que escrevemos é um arquivo .java, para rodar em outros sistemas o arquivo passa por uma compilação (javac) onde passa a ser um arquivo .class (Bytecode), no qual a partir do JVM (Java Virtual Machine) consegue se comunicar com os outros sistemas, sendo que cada Sistema Operacional tem sua JVM. Para desenvolver aplicações em Java é utilizado o JDK (Java Development Kit) em que possui uma JVM, compilador e ferramentas que servem de ajuda ao desenvolvedor.
#### 15 - Operadores pt 01 - Relacionais

Não é possível executar uma operação após concatenar a expressão com uma String.

### 16 - Operadores pt 02 - Relacionais

Símbolos de operações básicas como adição, subtração, divisão, multiplicação e resto recebem o nome de **Operações Aritméticas**, enquanto as **Operações Relacionais** são comparações de valores (retornam *true* ou *false*). Padrão de nomenclatura para tipos booleanos começam com **is**.

### 19 - Operadores pt 05 - Atribuição

Os operadores (++) e (--) são chamados de operadores unários, por exemplo:

```Java
int contador = 0;
contador++;
```

A ordem de colocação dos sinais tem interferência no modo como é executado, enquanto for posicionado depois, será adicionado um valor somente se algo for feito em relação a variável, já quando posicionado antes será adicionado um valor sem a necessidade da variável passar por uma ação.

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