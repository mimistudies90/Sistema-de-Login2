# Sistema-de-Login2
1. Introdução
Nome do Projeto: Sistema_Login

## 1 Introdução
O Sistema_Login é uma aplicação simples desenvolvida em PHP com MySQL que permite autenticação de usuários. Ele serve como base para sistemas maiores, garantindo que apenas usuários cadastrados possam acessar áreas protegidas do sistema.

Tecnologias Utilizadas:
PHP, MySQL, HTML,, Visual Studio Code

Autores:Júlia Carla do Carmo Júlio , Maria Cecília da Conceição Pinto
Responsável: Paula Maria da Rocha Celidorio

Data de Início:
06/06/2025

## 2 Estrutura do Projeto

LOGIN/
├── config/
│   └── Database.php          # Arquivo de configuração e conexão com o banco de dados
│
├── models/
│   ├── Usuario.php           # Classe que representa o usuário
│   └── UsuarioDAO.php        # Classe responsável pela manipulação de dados do usuário
│
├── public/
│   ├── login.php             # Página com o formulário de login
│   └── process_login.php     # Lógica que processa o login do usuário
│
├── utils/
│   └── Sanitizacao.php       # Funções auxiliares para tratar dados de entrada
│
├── sistema_login.sql         # Script SQL para criação da tabela de usuários
│
└── README.md                 # Documentação do projeto

## 3 Configuração do Ambiente ### **Requisitos**
    • Servidor XAMP
    • Visual Studio Code[1.98.2]
    • MySQL  Workbench[8.0.36]
    • Sistema operacinal: Windows 11;
    ### **Instalação**
    
# 4 Como Executar o Projeto
Clone o repositório:

bash
Copiar
Editar
git clone https://github.com/seuusuario/Sistema_Login.git
Importe o banco de dados:

Use o phpMyAdmin ou o MySQL para importar o arquivo sistema_login.sql.

Configure o banco de dados:

No arquivo config/Database.php, edite os dados de conexão conforme seu ambiente:

php
Copiar
Editar
private $host = 'localhost';
private $db_name = 'nome_do_banco';
private $username = 'root';
private $password = '';
Acesse o sistema:

Execute o servidor local (como XAMPP) e acesse http://localhost/Sistema_Login/public/login.php.

## 4 Estrutura do Banco de Dados 

  CREATE DATABASE sistema_login;
USE sistema_login;
-- Cria a tabela de usuários
CREATE TABLE usuarios (
    id INT PRIMARY KEY AUTO_INCREMENT,
    email VARCHAR(255) NOT NULL UNIQUE,
    senha_hash VARCHAR(255) NOT NULL,
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
-- Insere um usuário de exemplo (senha = 'senha123')
INSERT INTO usuarios (email, senha_hash) 
VALUES ('usuario@exemplo.com', '$2y$10$92IXUNpkjO0rOQ5byMi.Ye4oKoEa3Ro9llC/.og/at2.uheWG/igi');
 
