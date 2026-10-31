# DIO Agent - Especialização em Cibersegurança & AppSec

Este repositório apresenta a evolução do **DIO Agent**, transformando-o de um assistente de IA genérico em um **mentor especialista em Cibersegurança e Segurança de Aplicações (AppSec)**. O agente foi especializado utilizando apenas arquivos de configuração e conhecimento em Markdown, sem nenhum tipo de retreinamento de modelo.

---

## 🎯 A Especialização e o Porquê

No desenvolvimento de software, é comum que desenvolvedores encontrem ou introduzam vulnerabilidades (como falhas de *SQL Injection* ou má configuração de servidores). Assistentes de IA tradicionais costumam entregar o código corrigido de imediato, o que não promove a educação ou a segurança preventiva.

**A especialização criada (`vulnerability-analysis`) resolve isso ao instruir o agente a:**
1. **Perguntar primeiro:** Investigar o contexto do ambiente (se é produção, homologação ou laboratório).
2. **Avaliar riscos:** Classificar formalmente o impacto, a probabilidade e a severidade do problema.
3. **Mapear ameaças:** Conectar a falha a frameworks de mercado como o **MITRE ATT&CK**.
4. **Orientar a remediação:** Ensinar o princípio defensivo por trás da correção antes de entregar o código pronto.

---

## 📂 Arquivos Criados e Alterados

A arquitetura do agente foi estendida com os seguintes componentes:

| Arquivo | Ação | Descrição |
| :--- | :--- | :--- |
| `skills/vulnerability-analysis/SKILL.md` | **Criado** | Roteiro de comportamento e regras defensivas que regem a análise do agente. |
| `skills/vulnerability-analysis/README.md` | **Criado** | Documentação detalhada da skill para humanos. |
| `agent/knowledge/security-basics.md` | **Criado** | Base de conhecimento conceitual (Tríade CIA, definições de Risco/Ameaça/Vulnerabilidade e boas práticas). |
| `agent/persona.md` | **Alterado** | Incorporação da persona analítica e preventiva de AppSec. |
| `AGENTS.md` | **Alterado** | Registro da nova skill na tabela de habilidades do agente. |
| `app.py` | **Criado** | Script de laboratório propositalmente vulnerável a *SQL Injection* utilizado para os testes práticos. |

---

## 🚀 Como Rodar o Agente no Hermes

Para testar o agente especializado em seu ambiente local:

1. **Pré-requisitos:** Tenha o Python e o Hermes instalados conforme a documentação oficial do projeto base da DIO.
2. **Clone o repositório:**
   ```bash
   git clone https://github.com/SEU-USUARIO/nome-do-repositorio.git
   cd nome-do-repositorio
   ```
3. **Abra o terminal estritamente na pasta raiz** do projeto para que o Hermes reconheça os arquivos de contexto.
4. **Inicie o Hermes:**
   ```bash
   hermes
   ```
5. **Faça o teste prático:** Envie uma mensagem simulando a entrega de um código vulnerável (como o `app.py` presente neste repositório):
   > *"Sou dev e criei uma rotina de login em app.py. Pode analisar a segurança para mim?"*

---

## 📸 Evidências do Funcionamento

### 1. Coleta de Contexto Inicial
> *(Adicione aqui um print da tela do terminal onde o agente pergunta se o servidor é de produção, laboratório ou homologação antes de dar a resposta definitiva)*

### 2. Análise de Risco e MITRE ATT&CK (`app.py`)
> *(Adicione aqui um print da análise estruturada do `app.py` com impacto, probabilidade, severidade e o direcionamento de correção)*

---

## 🛠️ Melhoria Escolhida
Além de cumprir os requisitos fundamentais do desafio, esta implementação incorporou a **padronização rigorosa de relatórios baseados na Matriz de Risco** e a **trava comportamental de questionamento prévio**, aproximando a resposta da IA à conduta de um auditor de segurança sênior.
