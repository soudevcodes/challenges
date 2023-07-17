### Desafio: Calculadora de Média

Escreva um programa que solicite ao usuário que insira uma lista de números (separados por vírgula) e calcule a média dos números fornecidos. O programa deve exibir o resultado da média na tela.

Regras:

- Os números podem ser inteiros ou decimais.
- Os números podem ser positivos ou negativos.
- O programa deve lidar com uma lista de qualquer tamanho.


Exemplo de entrada 1:
```
Insira a lista de números: 5, 8, 12, 3, 6
````

Exemplo de saída 1:
```
A média é: 6.8
```

Exemplo de entrada 2:
```
Insira a lista de números: 10, -5, 2.5, 9, -3.5
```

Exemplo de saída 2:
```
A média é: 2.2
```

Você pode escolher a linguagem de programação que preferir e implementar a solução para este desafio. 

-----

### Respostas

#### Python

```python
def calcular_media():
    numeros = input("Insira a lista de números (separados por vírgula): ")
    lista = [float(num) for num in numeros.split(",")]

    soma = sum(lista)
    media = soma / len(lista)
    print(f"A média é: {media:.2f}")

calcular_media()
```

#### JavaScript

```javascript
function calcularMedia() {
  const numeros = prompt("Insira a lista de números (separados por vírgula):");
  const lista = numeros.split(",").map(Number);

  const soma = lista.reduce((acc, num) => acc + num, 0);
  const media = soma / lista.length;
  console.log(`A média é: ${media.toFixed(2)}`);
}

calcularMedia();
```


#### C#
```csharp
using System;

class Program
{
    static void Main()
    {
        CalcularMedia();
    }

    static void CalcularMedia()
    {
        Console.Write("Insira a lista de números (separados por vírgula): ");
        string numerosInput = Console.ReadLine();

        double[] numeros = Array.ConvertAll(numerosInput.Split(','), double.Parse);

        double soma = 0;
        foreach (double num in numeros)
        {
            soma += num;
        }

        double media = soma / numeros.Length;
        Console.WriteLine($"A média é: {media:F2}");
    }
}

```


#### Java
```java
import java.util.Scanner;
import java.util.Arrays;

public class Main {
    public static void main(String[] args) {
        calcularMedia();
    }

    public static void calcularMedia() {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Insira a lista de números (separados por vírgula): ");
        String numerosInput = scanner.nextLine();

        double[] numeros = Arrays.stream(numerosInput.split(","))
                                 .mapToDouble(Double::parseDouble)
                                 .toArray();

        double soma = Arrays.stream(numeros).sum();
        double media = soma / numeros.length;
        System.out.printf("A média é: %.2f%n", media);

        scanner.close();
    }
}
```



