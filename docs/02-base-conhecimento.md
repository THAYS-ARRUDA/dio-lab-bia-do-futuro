# Base de Conhecimento

## Dados Utilizados

Descreva se usou os arquivos da pasta `data`, por exemplo:

| Arquivo | Formato | Utilização no Agente |
|---------|---------|---------------------|
| `historico_conversas.csv` | CSV | Contextualizar interações anteriores |
| `dados_triagem.csv` | CSV | Verificar dados e usar as informações para passar para o cliente |

---

## Adaptações nos Dados

> Você modificou ou expandiu os dados mockados? Descreva aqui.

Por ter alterado o tipo de agente de financeiro para um que auxilia a gestão de serviços eu não utilizei os dados

---

## Estratégia de Integração

### Como os dados são carregados?
> Descreva como seu agente acessa a base de conhecimento.

CSV são carregados no início da sessão e incluídos no contexto do prompt via código, o panda

```python
import pandas as pd
df = pd.read_csv('seu_arquivo.csv')
```


### Como os dados são usados no prompt?
> Os dados vão no system prompt? São consultados dinamicamente?

```text
HISTÓRICO DE CONVERSAS

DADIS DE TRIAGEM:

```
---

## Exemplo de Contexto Montado

> Mostre um exemplo de como os dados são formatados para o agente.

```
Dados do Cliente:
- Nome: João Silva
- Perfil: Moderado
- Saldo disponível: R$ 5.000

Últimas transações:
- 01/11: Supermercado - R$ 450
- 03/11: Streaming - R$ 55
...
```
