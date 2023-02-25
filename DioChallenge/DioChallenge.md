# Provas/Desafios JAVA

## **Desafio**

O custo de um carro novo ao consumidor é a soma do custo de fábrica com a porcentagem do distribuidor e dos impostos (aplicados ao custo de fábrica). O gerente de uma loja de carros gostaria de um programa para calcular o preço de um carro novo para os clientes. Você receberá o custo de fábrica e as porcentagens referentes ao distribuidor e os impostos e deverá escrever programa para ler esses valores e imprimir o valor final do carro.

## **Entrada**

Você recebera três valores inteiros que representam o custo de fábrica, as porcentagens do distribuidor e os impostos.

## **Saída**

Como saída, teremos o valor final do preço de um carro novo.

**Exemplo 1**

| Entrada | Saída |
| --- | --- |
| 200002845 | 34600 |

**Exemplo 2**

| Entrada | Saída |
| --- | --- |
| 300001010 | 36000 |

Resposta:

```
package org.example;

import java.util.Scanner;

public class NomeEIDade {
    public static void main(String[] args) {

        Scanner scan = new Scanner(System.in);
        int custoFabrica = scan.nextInt();
        int porcentagemDistribuidor = scan.nextInt();
        int PercentualImpostos = scan.nextInt();

        int custoConsumidor;
        int Distribuidor;
        int ValorImpostos;

        ValorImpostos = (custoFabrica * PercentualImpostos) / 100;
        Distribuidor = (custoFabrica * porcentagemDistribuidor) / 100;
        custoConsumidor = (ValorImpostos + Distribuidor + custoFabrica);

        System.out.println(custoConsumidor);
    }
}
```

## **Desafio**

Leia **6** valores. Em seguida, mostre **quantos** destes valores digitados **foram positivos**. Na próxima linha, deve-se **mostrar a média** de **todos os valores positivos digitados**, com **um** dígito **após** o ponto **decimal**.

## **Entrada**

A entrada contém **6 números** que podem ser valores **inteiros ( int )** ou de **ponto flutuante ( float ou double** ). Pelo menos **um** destes números **será positivo**.

## **Saída**

O **primeiro valor** de saída é a **quantidade de valores positivos**. A próxima linha deve mostrar a **média** dos valores positivos digitados.

| Exemplo de Entrada | Exemplo de Saída |
| --- | --- |
| 7-56-3.44.612 | 4 valores positivos7.4 |

Resposta:

```
package org.example;

import java.util.Scanner;

public class NomeEIDade {
    public static void main(String[] args) {
        Scanner leitor = new Scanner(System.in);
        int cont = 0;
        double media = 0;
        double x;

        //TODO: Implemente as condições adequadas para obter a quantidade
//de valores positivos e a média dos valores positivos:
        for (int i = 0; i < 6; i++) {
            x = leitor.nextFloat();
            if (x > 0) {
                cont++;
                media += x;
            }
        }
        media = media / cont;
        System.out.println(cont + " valores positivos");
        System.out.println(String.format("%.1f", media));
    }
}
```

## **Desafio**

Daenerys é a khaleesi dos Dothraki. Juntamente com Drogon, eles vão atrás do Tyrion, para tentar dominar Westeros. Ela possui, além do seu dragãozinho, um rastreador que mede o nível de energia de qualquer ser vivo. Todos os seres com o nível menor ou igual a 8000, ela considera como se fosse um inseto. Quando passa deste valor, que foi o caso do Drogon, ela se espanta e grita “Mais de 8000”. Baseado nisso, utilize a mesma tecnologia e analise o nível de energia dos seres vivos.

## **Entrada**

A primeira linha contém um número inteiro **C** relativo ao número de casos de teste. Em seguida, haverá **C** linhas, com um número inteiro **N** (100 <= **N** <= 100000) relativo ao nível de energia de um ser vivo.

## **Saída**

Para cada valor lido, imprima o texto correspondente.

| Exemplo de Entrada | Exemplo de Saída |
| --- | --- |
| 38001100200 | Mais de 8000!Inseto!Inseto! |

Resposta:

```
package org.example;

import java.util.Scanner;

public class PoderDeCombate {
    public static void main(String[] args) {
        int casos, poderDeLuta;

        Scanner ler = new Scanner(System.in);

        casos = ler.nextInt();

        for(int i = 0; i < casos; i++){
            poderDeLuta = ler.nextInt();

            if( poderDeLuta > 8000){
                System.out.println("Mais de 8000!");
            } else {
                System.out.println("Inseto!");
            }
        }
    }
}
```

## **Desafio**

A seguinte sequência de números 0 1 1 2 3 5 8 13 21... é conhecida como série de Fibonacci. Nessa sequência, cada número, depois dos 2 primeiros, é igual à soma dos 2 anteriores. Escreva um algoritmo que leia um inteiro N (N < 46) e mostre os N primeiros números dessa série.

## **Entrada**

O arquivo de entrada contém um valor inteiro N (0 < N < 46).

## **Saída**

Os valores devem ser mostrados na mesma linha, separados por um espaço em branco. Não deve haver espaço após o último valor.

| Exemplo de Entrada | Exemplo de Saída |
| --- | --- |
| 5 | 0 1 1 2 3 |

Agradecimentos a Cássio F.

Resposta:

```
package org.example;

import java.util.Scanner;

public class Fibonacci {
    public static void main(String[] args) {
        Scanner leitor = new Scanner(System.in);
        int N = leitor.nextInt();
        int proximo, anterior = 0, atual = 1;
        for (int i = 1; i <= N; i++) {
            if (i == N) System.out.println(anterior);

                //TODO: Implemente a condição ideal para que possamos obter os valores solicitados:

else System.out.print(anterior + " ");
            proximo = anterior + atual;
            anterior = atual;
            atual = proximo;
        }
    }
}
```

## **Desafio**

Neste desafio, faça um programa que calcule o valor de H com N termos.

Sendo, H = 1 + 1/2 + 1/3 + 1/4 + ... + 1/N.

## **Entrada**

A entrada consiste em um número inteiro positivo.

## **Saída**

Na saída será impresso o valor que representa a soma dos termos.

| Entrada | Saída |
| --- | --- |
| 4 | 2 |
| 8 | 3 |
| 3 | 2 |

Resposta:

```
package org.example;

import java.util.Scanner;

public class Desafio2 {
    public static void main(String[] Args) {

        double h = 0;
        Scanner sc = new Scanner(System.in);
        double n = sc.nextDouble();

        for (int i = 1; i <= n; i++) {
            h += 1 / (double)i;
        }
        System.out.println((String.format(String.valueOf((Math.round(h))))));
    }
}
```

## **DESAFIO ANIMAL**

Neste problema, você deverá ler 3 palavras que definem o tipo de animal possível segundo o esquema abaixo, da esquerda para a direita.  Em seguida conclua qual dos animais seguintes foi escolhido, através das três palavras fornecidas.

![https://resources.urionlinejudge.com.br/gallery/images/problems/UOJ_1049_b.png](https://resources.urionlinejudge.com.br/gallery/images/problems/UOJ_1049_b.png)

## **Entrada**

A entrada contém 3 palavras, uma em cada linha, necessárias para identificar o animal segundo a figura acima, com todas as letras minúsculas.

## **Saída**

Imprima o nome do animal correspondente à entrada fornecida.

| Exemplos de Entrada | Exemplos de Saída |
| --- | --- |
| vertebradomamiferoonivoro | homem |

| Exemplos de Entrada | Exemplos de Saída |
| --- | --- |
| vertebradoavecarnivoro | aguia |

| Exemplos de Entrada | Exemplos de Saída |
| --- | --- |
| invertebradoanelideoonivoro | minhoca |

Resposta:

```
package org.example;

import java.util.Scanner;

public class DesafioAnimal {

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        String AN1, AN2, AN3;

        AN1 = sc.nextLine();
        AN2 = sc.nextLine();
        AN3 = sc.nextLine();

        switch (AN1) {
            case "vertebrado":
                if (AN2.equals("ave") && AN3.equals("carnivoro")) {
                    System.out.println("aguia");
                } else if (AN2.equals("ave") && AN3.equals("onivoro")) {
                    System.out.println("pomba");
                } else if (AN2.equals("mamifero") && AN3.equals("onivoro")) {
                    System.out.println("homem");
                } else if (AN2.equals("mamifero") && AN3.equals("herbivoro")) {
                    System.out.println("vaca");
                }
            case "invertebrado":
                if (AN2.equals("inseto") && AN3.equals("hematofago")) {
                    System.out.println("pulga");
                } else if (AN2.equals("inseto") && AN3.equals("herbivoro")) {
                    System.out.println("lagarta");
                } else if (AN2.equals("anelideo") && AN3.equals("hematofago")) {
                    System.out.println("sanguessuga");
                } else if (AN2.equals("anelideo") && AN3.equals("onivoro")) {
                    System.out.println("minhoca");
                }
        }
    }
}
```

## **Desafio**

Seu Zé está vendendo frutas com a seguinte tabela de preços:

**Exemplo 1**

|  | Até 5 Kg | Acima de 5 Kg |
| --- | --- | --- |
| Morango | R$ 2,50 por Kg | R$ 2,20 por Kg |
| Maçã | R$ 1,80 por Kg | R$ 1,50 por Kg |

Se o cliente comprar mais de 8 Kg em frutas ou o valor total da compra ultrapassar R$ 25,00, receberá ainda um desconto de 10% sobre este total. Escreva um algoritmo para ler a quantidade (em Kg) de morangos e a quantidade (em Kg) de maças adquiridas e escreva o valor a ser pago pelo cliente.

## **Entrada**

Como entrada, você recebera a quantidade em kg de morangos e a quantidade em kg de maçãs.

## **Saída**

Será o valor a ser pago pelo cliente, conforme a tabela de preços da quintanda do seu Zé.

**Exemplo 1**

| Entrada | Saída |
| --- | --- |
| 32 | 11.1 |

**Exemplo 2**

| Entrada | Saída |
| --- | --- |
| 11 | 4.3 |

**Exemplo 3**

| Entrada | Saída |
| --- | --- |
| 55 | 19.35 |

Resposta:

```
package org.example;

import java.util.Scanner;

public class BancaDoZe {
    public static void main(String[] args) {

        Scanner input = new Scanner(System.in);
        int morangos = input.nextInt();
        int macas = input.nextInt();
        double precoMorangos;
        double precoMacas;
        double precoTotal;

        if (morangos <= 5) {
            precoMorangos = morangos * 2.50;
        } else {
            precoMorangos = morangos * 2.20;
        }
        if (macas <= 5) {
            precoMacas = macas * 1.80;
        } else {
            precoMacas = macas * 1.50;
        }

        precoTotal = precoMorangos + precoMacas;

        if ((morangos + macas > 8) || (precoTotal > 25.00)) {
            System.out.println(precoTotal - (precoTotal * 0.1));
        } else {
            System.out.println(precoTotal);
        }
    }
}
```

## **Desafio**

Leia 3 valores reais (A, B e C) e verifique se eles formam ou não um triângulo. Em caso positivo, calcule o perímetro do triângulo (soma de todos os lados) e apresente a mensagem:**Perimetro = XX.X**Em caso negativo, calcule a área do trapézio que tem A e B como base e C como altura, mostrando a mensagem:**Area = XX.X**

*Fórmula da área de um trapézio: AREA = ((A + B) x C) / 2*

## **Entrada**

A entrada contém três valores reais.

## **Saída**

O resultado deve ser apresentado com uma casa decimal.

| Exemplo de Entrada | Exemplo de Saída |
| --- | --- |
| 6.0 4.0 2.0 | Area = 10.0 |

| 6.0 4.0 2.1 | Perimetro = 12.1 |
| --- | --- |

Resposta:

```
package org.example;

import java.util.Scanner;

public class AreaPerimetro {
    public static void main(String[] args) {
        Scanner leitor = new Scanner(System.in);
        double A = leitor.nextDouble();
        double B = leitor.nextDouble();
        double C = leitor.nextDouble();
        double perimetroTriangulo;
        double areaTrapezio;
        boolean triangulo;

        if ((B - C) < A && A < (B + C)) {
            triangulo = true;
        } else if ((A - C) < B && B < (A + C)) {
            triangulo = true;
        } else if ((A - B) < C && C < (A + B)) {
            triangulo = true;
        } else triangulo = false;

        if (triangulo) {
            perimetroTriangulo = A + B + C;
            System.out.println("Perimetro = " + String.format("%.1f", perimetroTriangulo));
        } else {
            areaTrapezio = (((A + B) * C) / 2);
            System.out.println("Area = " + String.format("%.1f", areaTrapezio));
        }
    }
}
```

## **Desafio**

Jorginho é professor do primário de uma determinada escola. Ele tem 100000 alunos e precisa criar um programa que verifica quantos espaços em branco e quantas vogais existem em uma determinada string de entrada que os alunos entregaram na avaliação final. Ajude-o a realizar essa tarefa antes que o tempo para entrega-la no fim do semestre acabe!

## **Entrada**

A entrada será uma frase no formato de string.

## **Saída**

A saída deverá retornar quantos espaços em branco e quantas vogais existem na determinada string, conforme exemplo abaixo:

| EXEMPLO DE ENTRADA | EXEMPLO DE SAÍDA |
| --- | --- |
| “Amo a DIO” | Espacos em branco: 2 Vogais: 5 |
| “Esse desafio foi facil” | Espacos em branco: 3 Vogais: 10 |
| “Navegar nas aguas do teu mar” | Espacos em branco: 5 Vogais: 11 |

Resposta:

```
package org.example;

import java.util.Scanner;

public class EspacosEmBranco {

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String str = sc.nextLine();
        String[] strSplit = str.split(" ");
        char[] arrVogais = {'a', 'e', 'i', 'o', 'u'};
        int espacosEmBranco = strSplit.length - 1, quantVogais = 0;

        for (String item : strSplit) {
            for (char vogais : arrVogais) {
                if (item.toLowerCase().contains(String.valueOf(vogais))) {
                    quantVogais++;
                }
            }
        }
        System.out.println("Espacos em branco: " + espacosEmBranco + " Vogais: " + quantVogais);
    }
}
```

## **Desafio**

Há um país denominado Lolipad, todos os habitantes ficam felizes em pagar seus impostos, pois sabem que nele não existem políticos corruptos e os recursos arrecadados são utilizados em benefício da população, sem qualquer desvio. A moeda deste país é o Loli, cujo símbolo é o R$.

Você terá o desafio de ler um valor com duas casas decimais, equivalente ao salário de uma pessoa de Loli. Em seguida, calcule e mostre o valor que esta pessoa deve pagar de Imposto de Renda, segundo a tabela abaixo.

![https://resources.urionlinejudge.com.br/gallery/images/problems/UOJ_1051_pt.png](https://resources.urionlinejudge.com.br/gallery/images/problems/UOJ_1051_pt.png)

Lembre que, se o salário for R$ 3002.00, a taxa que incide é de 8% apenas sobre R$ 1000.00, pois a faixa de salário que fica de R$ 0.00 até R$ 2000.00 é isenta de Imposto de Renda. No exemplo fornecido (abaixo), a taxa é de 8% sobre R$ 1000.00 + 18% sobre R$ 2.00, o que resulta em R$ 80.36 no total. O valor deve ser impresso com duas casas decimais.

## **Entrada**

A entrada contém apenas um valor de ponto flutuante, com duas casas decimais.

## **Saída**

Imprima o texto "R$" seguido de um espaço e do valor total devido de Imposto de Renda, com duas casas após o ponto. Se o valor de entrada for menor ou igual a 2000, deverá ser impressa a mensagem "Isento".

| Exemplos de Entrada | Exemplos de Saída |
| --- | --- |
| 3002.00 | R$ 80.36 |

| 1701.12 | Isento |
| --- | --- |

| 4520.00 | R$ 355.60 |
| --- | --- |

Resposta: