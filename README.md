# DISC Framework - Plataforma de Avaliação Comportamental

[![Framework](https://img.shields.io/badge/Framework-Django-green)](https://www.djangoproject.com/)
[![License](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)

## 📌 Visão Geral

O **DISC Framework** é uma solução completa para gestão e execução de avaliações de perfil comportamental baseadas na metodologia DISC. Desenvolvido para ser modular e escalável, o framework permite que organizações integrem testes de personalidade de forma fluida em seus ecossistemas de RH e desenvolvimento humano.

### 📚 Documentação Rápida
- [📘 DeepWiki](./DEEPWIKI.md) - Detalhes técnicos e arquitetura.
- [🎨 Diagramas (Excalidraw)](./EXCALIDRAW.md) - Fluxos e modelos de dados.

---

## 🚀 Funcionalidades Principais


### ✉️ Contato e Suporte
Para dúvidas, suporte ou sugestões, entre em contato através do email: [goncalvesdani54@gmail.com](mailto:goncalvesdani54@gmail.com).

---

### 🛡️ Segurança e Autenticação
- **Sistema de Cadastro e Login**: Utiliza `django-allauth` para autenticação segura e flexível.
- **Segurança Django**: Hashing de senhas robusto e proteção contra vulnerabilidades web comuns.

### 🎨 Interface e Experiência
- **Dashboard Interativo**: Visualização de perfis e estatísticas globais em tempo real.
- **Formulário Dinâmico**: Questionário guiado para avaliação precisa.
- **Sugestões de Carreira**: Insights personalizados baseados no perfil comportamental (D, I, S ou C).

---

## 🛠️ Stack Tecnológica
- **Backend**: Python & Django.
- **Frontend**: Bootstrap 5, Custom CSS & JavaScript.
- **Banco de Dados**: Suporta SQLite (dev) e MySQL (prod).

## Como Rodar o Projeto

Siga estes passos para configurar e executar o projeto em seu ambiente local:

1. **Clone o Repositório**:
   - Use o comando `git clone https://github.com/Daniiizita/disc_assessment` para clonar o repositório no seu sistema.

2. **Instale as Dependências**:
   - Navegue até a pasta do repositório clonado e execute `pip install -r requirements.txt` para instalar todas as dependências necessárias.

3. **Execute as Migrações**:
   - Inicie as migrações do banco de dados com `python manage.py migrate` para estruturar o banco de dados.

4. **Inicie o Servidor Local**:
   - Finalmente, execute `python manage.py runserver` para iniciar o servidor local. Após isso, acesse `http://localhost:8000` no seu navegador para visualizar o projeto.

## Contribuições e Desenvolvimento Futuro

Este projeto está em constante evolução, e estamos abertos a contribuições que enriqueçam a sua capacidade e alcance. Atualmente, estamos focados em implementar as seguintes melhorias e funcionalidades no futuro:

1. **Integração com APIs de Recrutamento**: Planejamos expandir a funcionalidade da plataforma incorporando APIs de recrutamento. Isso permitirá sugerir vagas de emprego em tempo real, alinhadas com o perfil comportamental do usuário. Tal integração busca oferecer um caminho prático para que os usuários explorem oportunidades de carreira que se alinhem às suas habilidades e preferências.

2. **Dashboard de Administração Personalizado**: Estamos desenvolvendo um dashboard de administração avançado, que proporcionará uma visão abrangente da atividade dos usuários na plataforma. Essa ferramenta não só facilitará o monitoramento do comportamento do usuário, mas também permitirá a geração de relatórios detalhados, auxiliando na análise e melhoria contínua do sistema.

3. **Implementação de Testes Automatizados**: A qualidade do código é fundamental para o sucesso de qualquer projeto. Com isso em mente, pretendemos implementar uma suíte abrangente de testes automatizados. Esses testes garantirão a funcionalidade e a confiabilidade do código, além de facilitar a manutenção e as futuras atualizações do sistema.

## Licença do Projeto

Este projeto é distribuído sob a licença MIT, uma das licenças de software mais permissivas, que oferece grande liberdade para uso privado, comercial, ou de código aberto. A licença MIT é conhecida por sua simplicidade e flexibilidade. Para entender os termos específicos sob os quais o projeto é disponibilizado, por favor, consulte o arquivo [LICENSE.md](LICENSE) incluído no repositório.

## Entre em Contato

Se você tiver perguntas, sugestões, ou estiver interessado em colaborar com o projeto, não hesite em entrar em contato. Estou sempre aberta a feedback e oportunidades de colaboração para melhorar e expandir este projeto. Você pode me alcançar diretamente no seguinte endereço de email: <goncalvesdani54@gmail.com>.
