# 📊 Persistência de Dados: JPA, Hibernate e Padrão DAO

## Domínio de Modelagem e Acesso a Dados para Aplicações Backend

Este projeto é um portfólio prático que demonstra a implementação de uma camada robusta de **Persistência de Dados** em Java. O foco está na utilização do **Java Persistence API (JPA)** e **Hibernate** para mapeamento Objeto-Relacional (ORM) e na aplicação do padrão **DAO (Data Access Object)**.

---

## 🚀 Conceitos e Habilidades Demonstradas

Este repositório é a prova do domínio dos seguintes pilares do Backend Java:

### 1. Modelagem de Dados e POO

* **Entidades JPA (`@Entity`):** Mapeamento de classes de domínio, como `Cliente`, `Produto`, `Categoria` e `ItemPedido`.
* **Relacionamentos:** Implementação de cardinalidades entre entidades, incluindo **`@ManyToOne`** (ex: `ItemPedido` para `Pedido` e `Produto`).
* **Boas Práticas:** Separação clara entre a Camada de Modelo (`modelo/`) e a Camada de Acesso a Dados (`dao/`).

### 2. Persistência e ORM

* **JPA e Hibernate:** Configuração e uso para gerenciar o ciclo de vida das entidades.
* **Padrão DAO:** Implementação de classes como `ProdutoDAO` e `CategoriaDAO` para encapsular a lógica de acesso ao banco (CRUD).
* **Query Language:** (Se aplicável, mencione o uso de JPQL ou HQL para consultas complexas).

## 📄 Exemplo de Destaque: A Entidade ItemPedido

A classe `ItemPedido.java` é um excelente exemplo de entidade bem modelada.

```java
// Trecho de código da classe ItemPedido.java
@Entity
@Table(name = "itens_pedidos")
public class ItemPedido {

    // Estratégia de geração de ID
    @GeneratedValue(strategy = GenerationType.IDENTITY)
    private Long id;

    // Relacionamento com outras entidades
    @ManyToOne 
    private Pedido pedido;

    @ManyToOne 
    private Produto produto;

    private int quantidade;
    private BigDecimal precoUnitario; 
    // ...
}
```
## 🛠️ Tecnologias Utilizadas

| Categoria | Tecnologia |
| :--- | :--- |
| **Linguagem** | Java |
| **ORM (Mapeamento)** | JPA (Java Persistence API) |
| **Implementação ORM** | Hibernate |
| **Build Tool** | Maven (Provável) |
| **Database** | H2 (ou MySQL, se configurado) |
