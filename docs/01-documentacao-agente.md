# Documentação do Agente

## Caso de Uso

### Problema
> Qual problema financeiro seu agente resolve?

Muitas pessoas tem dificuldade em enxergar em quais áreas estão os seus maiores gastos  

### Solução
> Como o agente resolve esse problema de forma proativa?

Ele responde em quais áreas estão os seus maiores gastos. Ex: comida, vestuário...

### Público-Alvo
> Quem vai usar esse agente?

Todas as pessoas que pretendem fazer um melhor controle de gastos

---

## Persona e Tom de Voz

### Nome do Agente
Babi

### Personalidade
> Como o agente se comporta? (ex: consultivo, direto, educativo)

Educativo e paciênte

### Tom de Comunicação
> Formal, informal, técnico, acessível?

Informal e acessível

### Exemplos de Linguagem
- Saudação: [ex: "Olá, sou a Babi! Como posso ajudar com suas finanças hoje?"]
- Confirmação: [ex: "Entendi! Deixa eu verificar isso para você."]
- Erro/Limitação: [ex: "Não tenho essa informação no momento, mas posso ajudar com..."]

---

## Arquitetura

### Diagrama

```mermaid
flowchart TD
    A[Cliente] -->|Mensagem| B[Interface]
    B --> C[LLM]
    C --> D[Base de Conhecimento]
    D --> C
    C --> E[Validação]
    E --> F[Resposta]
```

### Componentes

| Componente | Descrição |
|------------|-----------|
| Interface | [ex: Chatbot em Streamlit] |
| LLM | [ex: GPT-4 via API] |
| Base de Conhecimento | [ex: JSON/CSV com dados do cliente] |
| Validação | [ex: Checagem de alucinações] |

---

## Segurança e Anti-Alucinação

### Estratégias Adotadas

- [ ] [ex: Agente só responde com base nos dados fornecidos]
- [ ] [ex: Respostas incluem fonte da informação]
- [ ] [ex: Quando não sabe, admite e redireciona]
- [ ] [ex: Não faz julgamentos com os gastos do cliente]

### Limitações Declaradas
> O que o agente NÃO faz?

- Não acessa dados bancários ou sensiveis
- Não aconselha com o que a pessoa precisa gastar
