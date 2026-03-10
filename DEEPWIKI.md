# DeepWiki - DISC Framework

## 📌 Visão Geral
O **DISC Framework** é uma aplicação robusta baseada em Django projetada para realizar avaliações comportamentais utilizando a metodologia DISC (Dominância, Influência, Estabilidade e Conformidade). O objetivo principal é fornecer insights sobre o perfil comportamental de usuários, especialmente estagiários e profissionais em início de carreira, auxiliando no autoconhecimento e na orientação profissional.

---

## 🏗️ Arquitetura do Sistema

A aplicação segue o padrão MVT (Model-View-Template) do Django, organizada nos seguintes módulos:

### 1. `assessment_disc_project` (Core Settings)
Contém as configurações globais do projeto, definições de banco de dados, middlewares e roteamento principal.

### 2. `disc` (Motor de Avaliação)
Este é o coração da aplicação.
- **Models**: `Pergunta` (armazena as questões do teste) e `ResultadoDISC` (armazena as pontuações calculadas).
- **Forms**: `QuestionnaireForm` gera o teste dinamicamente.
- **Logic**: Calcula a média das respostas para determinar o perfil predominante.

### 3. `user_auth` (Gestão de Usuários)
Gerencia o ciclo de vida do usuário.
- **Custom User**: Estende o modelo padrão do Django para incluir o link com `ResultadoDISC`.
- **Social Auth**: Integração com `django-allauth`.

### 4. `core` (Portal/Frontend)
Gerencia as páginas institucionais (Home, Sobre, Contato) e a interface geral.

---

## 📊 Modelo de Dados (DISC)

O cálculo do perfil DISC baseia-se em 4 eixos principais:

| Sigla | Perfil | Descrição Breve |
| :--- | :--- | :--- |
| **D** | Dominante | Foco em resultados, assertividade e controle. |
| **I** | Influente | Foco em pessoas, comunicação e persuasão. |
| **S** | Estabilidade | Foco em harmonia, paciência e lealdade. |
| **C** | Conformado | Foco em processos, precisão e lógica. |

### Fluxo de Dados:
1. O usuário responde ao formulário (`disc/views.py:QuestionnaireView`).
2. O sistema agrupa as respostas por perfil (`d, i, s, c`).
3. Calcula-se a média de pontuação para cada perfil.
4. Um objeto `ResultadoDISC` é criado e associado ao usuário.
5. A `ResultadoView` renderiza os insights baseados no perfil mais alto.

---

## 🛠️ Tecnologias
- **Backend**: Python 3.x, Django 5.x.
- **Frontend**: HTML5, CSS3 (Custom), Bootstrap 5, JavaScript.
- **Autenticação**: Django Allauth.
- **Visualização**: Chart.js (presumido pela lógica de estatísticas).
- **Banco de Dados**: SQLite (Desenvolvimento) / MySQL (Produção).

---

## 🚀 Próximos Passos
- Integração com APIs de recrutamento.
- Dashboard administrativo para RH.
- Expansão da cobertura de testes.
