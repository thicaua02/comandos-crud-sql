```sql
INSERT INTO categorias (nome) 
VALUES ('Tecnologia'), ('Educação'), ('Entretenimento');
```

```sql
INSERT INTO usuarios (nome, email, senha, tipo_usuario) VALUES
('Ana Silva', 'ana@email.com', '123abc', 'editor'),
('Bruno Souza', 'bruno@email.com', 'abc456', 'admin'),
('Carla Mendes', 'carla@email.com', '789xyz', 'editor');
```

```sql
INSERT INTO noticias (titulo, resumo, texto_completo, nome_imagem, destaque, id_usuario, id_categoria) VALUES (
    'Feira de tecnologia reúne estudantes e projetos inovadores',
    'Evento apresenta soluções desenvolvidas por alunos para desafios',
    'Estudantes de escolas públicas e privadas participaram, nesta sexta-feira, de uma feira de tecnologia. Entre os projetos apresentados estavam sistemas de economia de água, aplicativos educacionais e soluções de acessibilidade.',
    'feira-tecnologia-estudantes.jpg',
    'sim',
    1,
    2
);

INSERT INTO noticias (titulo, resumo, texto_completo, nome_imagem, destaque, id_usuario, id_categoria) VALUES (
    'Parque municipal recebe 200 novas árvores',
    'Ação ambiental amplia as áreas verdes e envolve moradores voluntários',
    'O parque municipal recebeu o plantio de 200 mudas de espécies nativas. A iniciativa contou com voluntários e profissionais da área ambiental, que também orientaram os participantes sobre preservação e cuidados com as árvores.',
    'plantio-arvores-parque.jpg',
    'nao',
    3,
    2
);

INSERT INTO noticias (titulo, resumo, texto_completo, nome_imagem, destaque, id_usuario, id_categoria) VALUES (
    'Parque municipal recebe 100 novas árvores',
    'Ação ambiental amplia as áreas verdes e envolve moradores voluntários',
    'O parque municipal recebeu o plantio de 100 mudas de espécies nativas. A iniciativa contou com voluntários e profissionais da área ambiental, que também orientaram os participantes sobre preservação e cuidados com as árvores.',
    'plantio-arvores-parque.jpg',
    'nao',
    3,
    1
);
```

```sql
UPDATE usuarios SET nome = 'Maria Silva' WHERE id = 1;
UPDATE usuarios SET tipo_usuario = 'admin' WHERE id = 1;
UPDATE categorias SET nome = 'Política' WHERE id = 2;
UPDATE noticias SET titulo = 'Feira de estudantes destinada a tecnologias e projetos inovadores' WHERE id = 1;
UPDATE noticias SET destaque = 'nao' WHERE id = 1;
UPDATE noticias SET id_categoria = 1 WHERE id = 1;
```

```sql
DELETE FROM noticias WHERE id = 3;
DELETE FROM categorias WHERE id = 3;
DELETE FROM usuarios WHERE id = 2;
```