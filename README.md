# Polimorfismo
## Exercício de polimorfismo

Fazer um programa para ler os dados de N
produtos (N fornecido pelo usuário). Ao final,
mostrar a etiqueta de preço de cada produto na
mesma ordem em que foram digitados.
Todo produto possui nome e preço. Produtos
importados possuem uma taxa de alfândega, e
produtos usados possuem data de fabricação.
Estes dados específicos devem ser
acrescentados na etiqueta de preço conforme
exemplo (próxima página). Para produtos
importados, a taxa e alfândega deve ser
acrescentada ao preço final do produto.

```mermaid
classDiagram
    class Product {
        -name : String
        -price : Double
        +priceTag() : String
    }

    class ImportedProduct {
        -customsFee : Double
        +priceTag() : String
        +totalPrice() : Double
    }

    class UsedProduct {
        -manufactureDate : Date
        +priceTag() : String
    }

    Product <|-- ImportedProduct
    Product <|-- UsedProduct
```
