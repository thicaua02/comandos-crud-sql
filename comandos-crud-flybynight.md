# Comandos CRUD para o banco de dados Fly By Night

## INSERT na tabela de Fornedores

```sql
INSERT INTO fornecedores (nome) VALUES ('Eletrônicos Tabajara');

INSERT INTO fornecedores (nome) VALUES 
    ('Games ABCD'), 
    ('Supermercado Tem de Tudo'), 
    ('Livraria Demais da Conta');
```

## INSERT na tabela de Produtos

```sql
INSERT INTO produtos (nome, descricao, preco, quantidade, fornecedor_id) 
VALUES (
    'Samsung Galaxy A16', 
    'É um telefone moderno e economico', 
    1000, 
    2, 
    1 -- id do fornecedor Eletrônicos Tabajara.
);

INSERT INTO produtos (nome, descricao, preco, quantidade, fornecedor_id) 
VALUES (
    'Senhor dos Anéis: As Duas Torres', 
    'Volume 2 da série de livros criadas pelo autor J.R.R. Tolkien', 
    90.01, 
    100, 
    5 -- id do fornecedor Eletrônicos Tabajara.
);

INSERT INTO produtos (nome, descricao, preco, quantidade, fornecedor_id) 
VALUES (
    'TV Led', 
    'Tela de 50 polegadas, resolução 4K, 4 entradas HDMI e etc e tal', 
    3400, 
    12, 
    1 -- id do fornecedor Eletrônicos Tabajara.
);
```

## INSERT na tabela de Produtos
```sql
INSERT INTO lojas(nome) VALUES 
('Casas Bahia'), 
('Shopping Zona Leste'), 
('Bazar das Coisas'), 
('Americanas');
```

## INSERT na tabela de Lojas_Produtos
Esta é uma tabela intermediária (também conhecida como **tabela_pivot**), ou seja, 
ela se relaciona com outras duas tabelas: **produtos** e **lojas** através de chaves
estrangeiras. 

```sql
INSERT INTO lojas_produtos (loja_id, produto_id, estoque) VALUES (2, 1, 20);

INSERT INTO lojas_produtos (loja_id, produto_id, estoque) VALUES (4, 2, 3);
INSERT INTO lojas_produtos (loja_id, produto_id, estoque) VALUES (2, 3, 10);
INSERT INTO lojas_produtos (loja_id, produto_id, estoque) VALUES (1, 1, 5);
INSERT INTO lojas_produtos (loja_id, produto_id, estoque) VALUES (4, 1, 2);
```

---

## UPDATE na tabela fornecedores
```sql
UPDATE fornecedores SET nome = 'Mundo dos Games'
WHERE id = 2;
```

## UPDATE na tabela produtos
```sql
UPDATE produtos SET preco = 2999, quantidade = 5 WHERE id = 3;
```

## UPDATE na tabela lojas_produtos
```sql
UPDATE lojas_produtos SET estoque = 4 WHERE loja_id = 2 AND produto_id = 1;

-- SQL aceita operadores lógicos: AND (E), OR (OU), NOT (NÃO).
```