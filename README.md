#  Projeto individual Database - modulo 3

Este repositório contém o script SQL para criar e popular um banco de dados simples para gerenciar informações sobre empresas, tecnologias e colaboradores. O banco de dados é nomeado "resilia".

# RESPOSTAS
**Respostas:**

1. **Entidades Necessárias:**
   - Empresas
   - Tecnologias
   - Colaboradores

2. **Principais Campos e Tipos:**
   - **Empresas:**
     - `id` (int, primary key, auto_increment)
     - `nome` (varchar(40))
     - `descricao` (varchar(40))

   - **Tecnologias:**
     - `id` (int, primary key, auto_increment)
     - `nome` (varchar(40))
     - `area` (varchar(40))

   - **Colaboradores:**
     - `id` (int, primary key, auto_increment)
     - `nome` (varchar(40))
     - `cargo` (varchar(40))
     - `empresa_id` (int, foreign key referenciando `empresas`)
     - `tecnologia_id` (int, foreign key referenciando `tecnologia`)

3. **Relacionamentos:**
   - A tabela `colaboradores` possui duas chaves estrangeiras (`empresa_id` e `tecnologia_id`) que se relacionam com as tabelas `empresas` e `tecnologia`, respectivamente.
   - Isso indica que um colaborador está associado a uma empresa específica e utiliza uma tecnologia específica em seu trabalho.

4. **Simulação de 2 Registros para Cada Entidade:**
   - **Empresas:**
     1. Nome: Resilia, Descrição: Curso de capacitação bootcamp
     2. Nome: Senac, Descrição: Curso voltado para a educação profissional

   - **Tecnologias:**
     1. Nome: Rede de computadores, Área: Webdev
     2. Nome: Programação, Área: Dados

   - **Colaboradores:**
     1. Nome: João, Cargo: Desenvolvedor, Empresa: Resilia, Tecnologia: Rede de computadores
     2. Nome: Maria, Cargo: Analista de Dados, Empresa: Senac, Tecnologia: Programação


## Estrutura do Banco de Dados

### Tabelas

#### Empresas
- `id` (int, primary key, auto_increment): Identificador único da empresa.
- `nome` (varchar(40)): Nome da empresa.
- `descricao` (varchar(40)): Descrição da empresa.

#### Tecnologias
- `id` (int, primary key, auto_increment): Identificador único da tecnologia.
- `nome` (varchar(40)): Nome da tecnologia.
- `area` (varchar(40)): Área da tecnologia.

#### Colaboradores
- `id` (int, primary key, auto_increment): Identificador único do colaborador.
- `nome` (varchar(40)): Nome do colaborador.
- `cargo` (varchar(40)): Cargo do colaborador.
- `empresa_id` (int): Chave estrangeira referenciando a tabela `empresas`.
- `tecnologia_id` (int): Chave estrangeira referenciando a tabela `tecnologia`.

### Relacionamentos

- A tabela `colaboradores` possui duas chaves estrangeiras: `empresa_id` e `tecnologia_id`, que se relacionam com as tabelas `empresas` e `tecnologia`, respectivamente.

## Instruções para Execução

1. Crie um banco de dados chamado "resiliaa" no seu sistema de gerenciamento de banco de dados.

2. Execute os comandos SQL fornecidos no script `create_database.sql` para criar as tabelas necessárias no banco de dados "resiliaa".

3. Execute os comandos SQL fornecidos no script `insert_data.sql` para popular as tabelas com dados de exemplo.

4. Agora você tem um banco de dados "resiliaa" pronto para ser utilizado!

## Exemplo de Dados

### Empresas

1. Nome: Resilia, Descrição: Curso de capacitação bootcamp
2. Nome: Senac, Descrição: Curso voltado para a educação profissional

### Tecnologias

1. Nome: Rede de computadores, Área: Webdev
2. Nome: Programação, Área: Dados

### Colaboradores

1. Nome: João, Cargo: Desenvolvedor, Empresa: Resilia, Tecnologia: Rede de computadores
2. Nome: Maria, Cargo: Analista de Dados, Empresa: Senac, Tecnologia: Programação

### Versões de Tecnologias em Empresas

1. Empresa: Resilia, Tecnologia: Rede de computadores, Versão: 1.0
2. Empresa: Senac, Tecnologia: Programação, Versão: 2.5

Este banco de dados de exemplo representa uma estrutura básica para armazenar informações sobre empresas, tecnologias e seus colaboradores. Sinta-se à vontade para adaptar e expandir conforme necessário para atender às suas necessidades específicas.
