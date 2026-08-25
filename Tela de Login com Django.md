# Projeto Tela de Login com Django

Aplicação web desenvolvida com Python e Django para autenticação de usuários e controle de acesso a páginas restritas.

## Comandos do Terminal e Documentação

### Ambiente Virtual e Instalação

* `python -m venv venv`: Cria o ambiente virtual isolado para o projeto.
* `Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser`: Ajusta a permissão do PowerShell no Windows para autorizar scripts locais.
* `.\venv\Scripts\activate`: Ativa o ambiente virtual no terminal.
* `python -m pip install django`: Instala o framework Django dentro do ambiente virtual.

### Gerenciamento do Django

* `python -m django startproject meu_site .`: Gera a estrutura principal de configurações do projeto na pasta raiz.
* `python manage.py startapp usuarios`: Cria o módulo de autenticação (aplicativo `usuarios`).
* `python manage.py migrate`: Cria as tabelas padrão de autenticação (`auth_user`) e sessões no banco SQLite.
* `python manage.py createsuperuser`: Cadastra um usuário administrador no banco de dados.
* `python manage.py runserver`: Inicia o servidor local de desenvolvimento no endereço `http://127.0.0.1:8000/`.

## Conceitos de Código Utilizados

* `INSTALLED_APPS`: Registra o módulo `usuarios` dentro de `settings.py`.
* `LOGIN_REDIRECT_URL` / `LOGOUT_REDIRECT_URL`: Define as rotas automáticas após entrar ou sair do sistema.
* `auth_views.LoginView`: View nativa do Django que processa formulários de login de forma segura.
* `@login_required`: Decorator em `views.py` que impede o acesso de usuários anônimos à página inicial.
* `{% csrf_token %}`: Tag de segurança obrigatória em formulários HTML para evitar ataques Cross-Site Request Forgery.

## Conclusão

Concluímos com sucesso a arquitetura base de autenticação no Django. Meu projeto agora conta com um ambiente virtual configurado, rotas protegidas, formulários com validação CSRF e uma documentação completa dos comandos no arquivo `README.md`.

### O que eu domino até aqui

* **Arquitetura MVT do Django:** Aprendi como funciona a comunicação entre Models (banco de dados), Views (lógica de acesso) e Templates (telas HTML).
* **Sistema de Autenticação:** Aprendi a utilizar a `LoginView` nativa do Django, criar usuários e proteger rotas com `@login_required`.
* **Configuração de Ambiente:** Aprendi a configurar e gerenciar ambientes virtuais (`venv`) e a solucionar permissões de execução de scripts no Windows.
