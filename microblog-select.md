# Trabalho

## Consultas básicas
```sql
SELECT * FROM usuarios; -- (1)
SELECT nome, email FROM usuarios; -- (2)
SELECT * FROM categorias; -- (3)
SELECT titulo, data_publicacao FROM noticias; -- (4)
SELECT nome AS NOME, tipo_usuario AS "TIPO DE USUARIO" FROM usuarios; -- (5)
```

## Filtros com WHERE
```sql
SELECT * FROM usuarios WHERE usuarios.tipo_usuario = 'admin'; -- (6)
SELECT * FROM noticias WHERE noticias.destaque = 'sim'; -- (7)
SELECT * FROM noticias WHERE noticias.id_categoria = 4; -- (8)
SELECT * FROM usuarios WHERE usuarios.tipo_usuario <> 'admin'; -- (9)
```

## Combinando condições
```sql
SELECT * FROM usuarios WHERE 
usuarios.tipo_usuario = 'editor' 
AND MOD(usuarios.id, 2) = 0; -- (10)

SELECT * FROM usuarios WHERE 
usuarios.id = 2 OR
usuarios.id = 3 OR
usuarios.id = 8;  -- (11)
```

## Pesquisa com LIKE
```sql
SELECT * FROM noticias
WHERE noticias.texto_completo LIKE '%inteligência artificial%'; -- (12)
SELECT * FROM noticias
WHERE noticias.texto_completo LIKE 'O%%'; -- (13)
```

## Ordenação
```sql
SELECT * FROM noticias
ORDER BY noticias.data_publicacao ASC; -- (14)
SELECT * FROM usuarios
ORDER BY usuarios.nome ASC; -- (15)
```

## Funções de agregação
```sql
SELECT COUNT(*) AS "Quantidade de usuários" FROM usuarios; -- (16)
SELECT COUNT(*) AS "Quantidade de noticias" FROM noticias; -- (17)
SELECT
    MIN(noticias.data_publicacao) AS "DATA MAIS RECENTE",
    MAX(noticias.data_publicacao) AS "DATA MENOS RECENTE"
FROM noticias; -- (18)
```

## Desafio
```sql
SELECT id, nome AS NOME, email AS "E-MAIL" FROM usuarios
WHERE usuarios.tipo_usuario = 'editor' AND MOD(usuarios.id, 2) = 0; -- (19)
```