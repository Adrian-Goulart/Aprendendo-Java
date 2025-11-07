# Curso 
# Java: aplicando a Orientação a Objetos

---
## 04. Aplicando comportamentos em comum
#### 02. Incluindo comportamentos adicionais -

O uso do `extends` nos códigos deixavam-o muito confusos caso utilizado em excesso, para isso surge a `Interface`. Ele funciona como uma espécie de "contrato" para outras classes, logo cada classe que implementa dela tem de utilizar o método que nela possui. Exemplo:

Criar uma interface:

```Java
public interface Classificavel {
	int getClassificacao();
}
```

Implementar uma interface:

```Java
public class Episodio implements Classificavel{
	// Código
}
```

---

## 03. Classificando episódios e filmes

A interface não pode ser criada como um objeto e sim apenas referenciada.

---

# Curso 
# Java: trabalhando com listas e coleções de dados

---

# Lista de Filmes com ArrayList

O ArrayList é uma lista, sua sintaxe é:

```Java
ArrayList<x> lista = new ArrayList();
```

Onde ***x*** é o tipo da lista.

Para chamar seu tamanho utiliza-se `.size()` e para pegar o valor de um index, utilizamos `.get().metodo()`.