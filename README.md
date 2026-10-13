# Gerenciador de Filmes

Aplicação web em PHP e MariaDB para cadastrar, listar, editar e excluir filmes.

[![PHP](https://img.shields.io/badge/PHP-puro-777BB4?logo=php)](https://www.php.net/)
[![MariaDB](https://img.shields.io/badge/MariaDB-MySQLi-003545?logo=mariadb)](https://mariadb.org/)
[![HTML5](https://img.shields.io/badge/HTML-5-E34F26?logo=html5)](https://developer.mozilla.org/pt-BR/docs/Web/HTML)
[![CSS3](https://img.shields.io/badge/CSS-3-1572B6?logo=css3)](https://developer.mozilla.org/pt-BR/docs/Web/CSS)

<!-- Adicionar uma captura de tela em docs/screenshots/ e descomentar a linha abaixo. -->
<!-- ![Tela principal](docs/screenshots/tela-principal.png) -->

## Sobre

O projeto é um CRUD de filmes feito em PHP puro, sem framework. A página principal reúne, lado a lado, a tabela de filmes cadastrados e o formulário de cadastro. Os dados ficam em um banco MariaDB, acessado com a extensão MySQLi.

## Funcionalidades

- Cadastro de filmes com título, ano de lançamento, gênero e sinopse
- Listagem dos filmes em tabela, lida diretamente do banco de dados
- Edição dos dados de um filme cadastrado
- Exclusão de filmes
- Validação dos dados no servidor antes da inserção (campos preenchidos e ano com quatro dígitos)

## Tecnologias

| Camada | Tecnologia |
|---|---|
| Linguagem | PHP, com a extensão MySQLi |
| Banco de dados | MariaDB (compatível com MySQL) |
| Interface | HTML5, CSS3, fonte Poppins (Google Fonts) |
| Ambiente local | XAMPP |

## Modelo de dados

| Entidade | Campos principais | Relacionamentos |
|---|---|---|
| `filmes` | idFilme, titulo, ano_lancamento, genero, sinopse (opcional), data_criacao | Tabela única, sem relacionamentos |

## Como executar

### Pré-requisitos

- [XAMPP](https://www.apachefriends.org/) com Apache e MySQL (MariaDB), ou PHP com MariaDB/MySQL instalados separadamente
- Git

### Instalação

Clone o repositório dentro da pasta `htdocs` do XAMPP (no Windows, `C:\xampp\htdocs`):

```bash
cd C:\xampp\htdocs
git clone https://github.com/joaomnz23/Projeto-Filmes-PHP.git
```

### Banco de dados

1. No XAMPP Control Panel, inicie os módulos **Apache** e **MySQL**.
2. Acesse o phpMyAdmin em `http://localhost/phpmyadmin`.
3. Abra a aba **Importar**, selecione o arquivo `filmes.sql` na pasta `BD` e clique em **Executar**, sem selecionar nenhum banco antes.

O arquivo cria o banco `filmes`, a tabela `filmes` e três registros de exemplo. Se o banco já existir, a tabela é recriada.

A conexão está configurada em `conexaoBD.php` com o padrão do XAMPP (servidor `localhost`, usuário `root`, sem senha, banco `filmes`). Ajuste os valores nesse arquivo caso seu ambiente use outras credenciais.

### Execução

Com o Apache e o MySQL em execução, acesse:

```
http://localhost/Projeto-Filmes-PHP/
```

Também é possível iniciar pelo servidor embutido do PHP, com o MariaDB em execução:

```bash
cd Projeto-Filmes-PHP
php -S localhost:8000
```

## Licença

Distribuído sob a licença MIT. Consulte o arquivo `LICENSE`.

## Autor

[joaomnz23](https://github.com/joaomnz23)