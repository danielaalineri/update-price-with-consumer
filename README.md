# 💰 Java Price Update with Consumer

Este projeto Java demonstra como utilizar a interface funcional `Consumer<T>` para atualizar preços de produtos em uma lista. 
O programa aplica um aumento de 10% ao preço de cada produto utilizando `forEach`.

---

## 📦 Estrutura do Projeto

### ✅ `Product` (`entities.Product`)
Classe que representa um produto com:
- `name` (nome do produto)
- `price` (preço do produto)

Métodos adicionais:
- `nonStaticPriceUpdate()` e `staticPriceUpdate(Product)` para aumentar o preço em 10% (não usados diretamente no programa).
- `toString()` sobrescrito para exibição formatada.

---

### ✅ `PriceUpdate` (`util.PriceUpdate`)
Classe que implementa `Consumer<Product>`.  
Responsável por aplicar um aumento de **10% no preço** de cada produto:

```java
@Override
public void accept(Product p) {
    p.setPrice(p.getPrice() * 1.1);
}

✅ Program (app.Program)

Classe principal que:

    Cria uma lista com 4 produtos.

    Aplica a lógica de aumento de preço com forEach(new PriceUpdate()).

    Imprime os produtos atualizados no console com System.out::println.


💻 Exemplo de Saída

Tv, 990.00
Mouse, 55.00
Tablet, 385.55
HD Case, 88.99

🚀 Como Executar

    Compile os arquivos:

    javac app/*.java entities/*.java util/*.java

    Execute o programa:
    java app.Program

📚 Conceitos Demonstrados

    Interface funcional Consumer<T>

    Expressões funcionais com forEach

    Encapsulamento com classes Product e PriceUpdate

    Uso de pacotes (app, entities, util)

👩‍💻 Autora

Daniela Alineri
Projeto criado para treinar programação funcional com Consumer e forEach no Java moderno.



    




