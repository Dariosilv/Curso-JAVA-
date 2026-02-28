# 📘 Cronograma do Curso de Java

**Período total:** 05/02/2026 a 17/04/2026

Este documento organiza os conteúdos do curso de Java por módulos (unidades), com datas, objetivos e um espaço reservado para inclusão de códigos-fonte conforme o aprendizado ao longo do curso.

---

## 🔹 Primeiros Passos

**📅 05/02/2026 a 08/02/2026**

**Conteúdos:**

* Apresentação do curso e da plataforma
* Introdução à lógica de programação
* Instalação e configuração do ambiente Java
* Primeiros conceitos básicos

**📂 Código (a ser adicionado futuramente):**

```java
// Código será inserido após o estudo deste módulo
```

---

## 🔹 Unidade 1 – Introdução aos Fundamentos da Programação

**📅 09/02/2026 a 15/02/2026**

**Conteúdos:**

* O que é programação
* Algoritmos e lógica
* Estrutura básica de um programa em Java
* Primeiro programa: Hello World

**📂 Código (a ser adicionado futuramente):**

```java
// Código de Olá mundo em Java 

public class OlaMundo {
    public static void main(String[] args) {
        System.out.println("Olá, Mundo!");
    
    }
}

```
---

----
## 🔹 Unidade 2 – Sintaxe Básica e Tipos de Dados

**📅 16/02/2026 a 22/02/2026**

**Conteúdos:**

* Sintaxe da linguagem Java

`Ao escrever um programa de computador temos de ter em mente duas dimensões: a sintaxe e a semântica. A sintaxe é como a gramática da linguagem de programação, define as regras de escrita (pontuação, palavras-chave, estrutura das instruções) e é verificada e validade pelo compilador; a semântica refere-se ao significado do que foi escrito (se o programa, mesmo bem escrito, faz o que deveria fazer`

* Tipos de dados primitivos
  
` Quando pensamos em resolver um problema no computador, logo surge a pergunta: onde e como vamos guardar as informações necessárias para esse problema? Em programação, usamos diferentes tipos de dados para armazenar diferentes tipos de valores.
Imagine que o computador é uma grande estante cheia de caixas. Cada caixa tem um rótulo indicando o que pode ser guardado dentro dela: números inteiros, números decimais, uma letra, verdadeiro ou falso. Em Java, essas caixas básicas recebem o nome de tipos primitivos`

* Declaração de variáveis
* Operadores aritméticos e lógicos

**📂 Código (Desafio(opcional) em java ):**

```java

// Código de Desafio opcional em java
public class DesafioEstudo {
    public static void main(String[] args) {
        int HorasPorDia = 2 ;
        int TotalDeSessoesNaSemana = 3;

        // Somando as duas variáveis
        int TotalNaSemana = HorasPorDia * TotalDeSessoesNaSemana;

        //Exibindo o resultado
        System.out.println("***** Rotina de estudos ***** ");
        System.out.println("Horas por dia: " + HorasPorDia + " horas");

        // Detalhamento dos dias
        System.out.println("Segunda-feira (manhã): " + HorasPorDia + " horas");
        System.out.println("Terça-feira (tarde): "+ HorasPorDia + " horas");
        System.out.println("Quinta-feira (noite): " + HorasPorDia + " horas");


        // Exibindo o Calculo Final
        System.out.println("Total na semana " + TotalNaSemana + " horas");

    }
}

```
```Java
//Codigo de relatorio onde ira abordar os tipos primitivos , constantes, Declaração de variáveis.
public class RealatorioRapido {
    public static void main (String[] args) {
        //Valores declarados
        String nomeProduto = "Caderno A4";
        int quantidadeEmEstoque = 12;
        int precoUnitarioCentavos = 350;
        boolean dispoonivelParaVenda = true;
        final int TAXA_ICMS_PERCENTUAL = 18;

        //Cálculos
        int valorbruto = quantidadeEmEstoque * precoUnitarioCentavos;
        int icms = valorbruto * TAXA_ICMS_PERCENTUAL /100;
        int total = valorbruto + icms;

        System.out.println("Produto: " + nomeProduto);
        System.out.println("Quantidade: " + quantidadeEmEstoque);
        System.out.println("Preco (centavos): " + precoUnitarioCentavos);
        System.out.println("Disponivel: " + dispoonivelParaVenda);
        System.out.println("ICMS (centavos): " + icms);
        System.out.println("Total (centavos): " + total);

    }
}
```
---

## 🔹 Unidade 3 – Comandos de Entrada, Saída e Atribuição

**📅 23/02/2026 a 01/03/2026**

**Conteúdos:**

* Entrada de dados (Scanner)
* Saída de dados (System.out)
* Atribuição de valores
* Exercícios práticos

**📂 Código (a ser adicionado futuramente):**

```java
// Atividade em Grupo (TRIO)
import java.util.Locale;
import java.util.Scanner;

public class RelatorioOrcamento_2 {
    public static void main(String[] args) {
        Locale.setDefault(new Locale("pt", "BR"));
        Scanner sc = new Scanner(System.in).useLocale(Locale.US);

        // Entradas
        System.out.print("Nome: ");
        String nome = sc.nextLine();

        System.out.print("Rendimento mensal: ");
        double rendimento = sc.nextDouble();

        System.out.print("Moradia: ");
        double moradia = sc.nextDouble();

        System.out.print("Alimentação: ");
        double alimentacao = sc.nextDouble();

        System.out.print("Transporte: ");
        double transporte = sc.nextDouble();

        // Cálculos
        double totalDespesas = moradia + alimentacao + transporte;
        double saldo = rendimento - totalDespesas;
        double percentual = (totalDespesas / rendimento) * 100;


        System.out.println("\n******** RELATÓRIO DO ORÇAMENTO ********");
        System.out.println("Nome: " + nome);
        System.out.printf("Rendimento mensal: R$ %.2f%n", rendimento);

        System.out.println("\nDespesas:");
        System.out.printf("- Moradia: R$ %.2f%n", moradia);
        System.out.printf("- Alimentação: R$ %.2f%n", alimentacao);
        System.out.printf("- Transporte: R$ %.2f%n", transporte);

        System.out.printf("\nTotal de despesas: R$ %.2f%n", totalDespesas);
        System.out.printf("Saldo do mês: R$ %.2f%n", saldo);
        System.out.printf("Percentual gasto: %.2f%%%n", percentual);
        System.out.println("****************************************");

        sc.close();
    }
}
```


```java
// Desafio do modulo 3
package UNIDADE_3;
import java.util.Scanner;
import java.util.Locale;

public class exercicio3 {
    public static void main(String[] args) {
        Locale.setDefault(new Locale("pt", "BR"));
        Scanner entrada = new Scanner(System.in).useLocale(Locale.US);

        System.out.println("Digite o seu nome:");
        String nome = entrada.nextLine();

        // Notas das provas
        System.out.println("----- Notas das Provas ----");
        System.out.print("Digite a nota da prova 1: ");
        double prova1 = entrada.nextDouble();

        System.out.print("Digite a nota da prova 2: ");
        double prova2 = entrada.nextDouble();

        // Notas dos Trabalhos
        System.out.println("----- Notas dos Trabalhos ----");
        System.out.print("Digite a nota do trabalho 1: ");
        double trabalho1 = entrada.nextDouble();

        System.out.print("Digite a nota do trabalho 2: ");
        double trabalho2 = entrada.nextDouble();

        System.out.print("Digite a nota do trabalho 3: ");
        double trabalho3 = entrada.nextDouble();

        System.out.print("Digite a nota do Trabalho Final: ");
        double trabalhoFinal = entrada.nextDouble();

        // Calculando a média
        double mediaProvas = (prova1 + prova2) / 2;
        double mediaTrabalhos = (trabalho1 + trabalho2 + trabalho3) / 3;
        double notaFinal = (mediaProvas * 0.60) + (mediaTrabalhos * 0.20) + (trabalhoFinal * 0.20);

        // Resultado final
        System.out.println("\n--- Relatório de Desempenho do Aluno ---");
        System.out.printf("Aluno: %s%n", nome);
        System.out.printf("Média das provas: %.2f%n", mediaProvas);
        System.out.printf("Média dos trabalhos práticos: %.2f%n", mediaTrabalhos);
        System.out.printf("Nota final: %.2f%n", notaFinal);

        entrada.close();  // FECHAR O SCANNER
    }
}

```
---

## 🔹 Unidade 4 – Estruturas Condicionais

**📅 02/03/2026 a 08/03/2026**

**Conteúdos:**

* Estrutura if, else e else if
* Estrutura switch-case
* Tomada de decisão no programa

**📂 Código (a ser adicionado futuramente):**

```java
// Código será inserido após o estudo deste módulo
```

---

## 🔹 Unidade 5 – Estruturas de Repetição

**📅 09/03/2026 a 15/03/2026**

**Conteúdos:**

* Laços for, while e do-while
* Controle de repetição
* Exercícios com loops

**📂 Código (a ser adicionado futuramente):**

```java
// Código será inserido após o estudo deste módulo
```

---

## 🔹 Unidade 6 – Funções e Manipulação de Dados

**📅 16/03/2026 a 22/03/2026**

**Conteúdos:**

* Métodos em Java
* Parâmetros e retorno
* Organização do código

**📂 Código (a ser adicionado futuramente):**

```java
// Código será inserido após o estudo deste módulo
```

---

## 🔹 Unidade 7 – Criação de Métodos

**📅 23/03/2026 a 29/03/2026**

**Conteúdos:**

* Métodos com e sem retorno
* Métodos estáticos
* Boas práticas

**📂 Código (a ser adicionado futuramente):**

```java
// Código será inserido após o estudo deste módulo
```

---

## 🔹 Unidade 8 – Coleções Simples

**📅 30/03/2026 a 05/04/2026**

**Conteúdos:**

* Arrays unidimensionais
* Arrays bidimensionais
* Manipulação de listas simples

**📂 Código (a ser adicionado futuramente):**

```java
// Código será inserido após o estudo deste módulo
```

---

## 🔹 Unidade 9 – Manipulação de Arquivos

**📅 06/04/2026 a 12/04/2026**

**Conteúdos:**

* Leitura de arquivos
* Escrita de arquivos
* Persistência de dados

**📂 Código (a ser adicionado futuramente):**

```java
// Código será inserido após o estudo deste módulo
```

---

## 📝 Avaliação Final

**📅 13/04/2026 a 17/04/2026**

* Revisão geral dos conteúdos
* Aplicação prática dos conceitos estudados
* Consolidação do aprendizado

---

✍️ **Autor:** Dário Silva
