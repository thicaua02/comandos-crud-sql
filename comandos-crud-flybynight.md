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