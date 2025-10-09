
# PRP (Product Requirement Prompts)

Coleção de **prompts de requisitos de produto (PRP)** para uso no desenvolvimento de software assistido por IA, otimizados para squads de engenharia.

---

## 📌 O que é PRP?

**PRP (Product Requirement Prompt)** é uma metodologia estruturada para fornecer tudo que um agente de IA precisa para gerar **código pronto para produção já na primeira iteração**.

Um PRP é composto por:

- **Contexto detalhado** (arquivos, trechos de código, exemplos)
- **Objetivo e justificativa do produto**
- **Blueprint de implementação e testes automatizados**

O PRP expande o tradicional Documento de Requisito de Produto (PRD), adicionando informações técnicas e exemplos necessários para que a IA entregue uma fatia vertical de software funcional.

---

## 🗂️ Estrutura Recomendada do Projeto

```text
seu-projeto/
|-- .claude/
|   |-- commands/
|-- PRPs/
|   |-- templates/
|   |-- scripts/
|   |-- ai_docs/
|-- CLAUDE.md
|-- src/
|-- tests/
```

---

## 🚀 Como Usar PRPs

### Opção 1: Adaptação a Projeto Existente

Copie os comandos do Claude:

```bash
cp -r /path/to/PRPs-agentic-eng/.claude/commands .claude/
```

Copie os templates e scripts:

```bash
cp -r /path/to/PRPs-agentic-eng/PRPs/templates PRPs/
cp -r /path/to/PRPs-agentic-eng/PRPs/scripts PRPs/
cp /path/to/PRPs-agentic-eng/PRPs/README.md PRPs/
```

(Opcional) Copie a documentação de IA:

```bash
cp -r /path/to/PRPs-agentic-eng/PRPs/ai_docs PRPs/
```

---

### Opção 2: Novo Projeto

Clone o repositório:

```bash
git clone https://github.com/AD-Thiago/PRPs-agentic-eng
cd PRPs-agentic-eng
```

Estruture seu projeto:

```bash
mkdir -p src/tests
touch src/__init__.py
touch pyproject.toml
touch CLAUDE.md
```

(Para projetos Python) Inicie o ambiente:

```bash
uv venv
uv sync
```

---

## ⚙️ Comandos Pré-Configurados

O diretório `.claude/commands/` inclui comandos para:

- Criação e execução de PRPs
- Planejamento e especificação
- Revisão e refatoração de código
- Integração com Git/GitHub
- Utilidades (onboarding, debug, etc)

Digite `/` no Claude Code para visualizar os comandos disponíveis.

---

## ✍️ Como Criar um PRP

Copie e edite um template:

```bash
cp PRPs/templates/prp_base.md PRPs/sua-feature.md
```

Preencha as seções:

- **Objetivo**
- **Justificativa**
- **Contexto e exemplos**
- **Blueprint de implementação** (plano detalhado)
- **Testes de validação**

Também é possível gerar um PRP via comando no Claude:

```text
/create-base-prp implementar autenticação com JWT
```

---

## 🧪 Execução e Testes

Execute PRPs via scripts ou comandos, por exemplo:

```bash
uv run PRPs/scripts/prp_runner.py --prp sua-feature --interactive
```

Inclua sempre testes automatizados e documente as seções críticas.

---

## ✅ Boas Práticas de PRP

- Inclua documentação e exemplos relevantes  
- Forneça testes automatizados sempre que possível  
- Mantenha os prompts objetivos e informativos  

---

## 📚 Recursos Inclusos

- Templates de PRP e planejamento  
- Documentação principal  
- Exemplos reais  
