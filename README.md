# Cafeteria API - Backend em C#

## Objetivos
A Cafeteria API foi projetada para:
- Gerenciar pedidos;
- Gerenciar estoque;
- Acompanhar vendas.

## Estrutura do Projeto
O projeto utiliza o padrão **MVC (Model-View-Controller)**, com os seguintes componentes:

### 1. **Views**
As *Views* representam a interface onde os usuários interagem. Todas as solicitações realizadas nesta camada são direcionadas aos *Controllers*.

#### Telas disponíveis:
- **Home**: Tela inicial.
- **Order**: Tela de pedidos.
- **Product**: Tela de estoque.

### 2. **Controllers**
Os *Controllers* são responsáveis por requisitar ações ou dados dos *Models* e retornar os resultados para as *Views*.

#### Controladores disponíveis:
- **Home**: Gerencia a tela inicial.
- **Order**: Implementa o CRUD de pedidos.
- **Product**: Implementa o CRUD de produtos.

### 3. **Models**
Os *Models* interagem com o banco de dados, realizando consultas e inserções. Eles enviam os resultados para os *Controllers*.

#### Classes disponíveis:
- **Order**: Representa os pedidos registrados.
- **Product**: Representa os produtos registrados.
- **ProductCategory**: Representa as categorias dos produtos.

## Diagrama de Classes
```mermaid
classDiagram
    Order <|-- Product
    class Product {
        +int Id
        +string Name
        +int Quantity
        +string Category
        +decimal Price
    }
    class Order {
        +int Id
        +string Name
        +int Quantity
    }
