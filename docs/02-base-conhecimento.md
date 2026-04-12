# Base de Conhecimento

## Dados Utilizados

Descreva se usou os arquivos da pasta `data`, por exemplo:

| Arquivo | Formato | Utilização no Agente |
|---------|---------|---------------------|
| `historico_atendimento.csv` | CSV | Contextualizar interações anteriores |
| `perfil_investidor.json` | JSON | Personalizar recomendações |
| `https://huggingface.co/spaces/FelipeBatista/finance/blob/main/index.html#L6` | JSON | Sugerir produtos adequados ao perfil |
| `transacoes.csv` | CSV | Analisar padrão de gastos do cliente |

> [!TIP]
> **Quer um dataset mais robusto?** Você pode utilizar datasets públicos do [Hugging Face](https://huggingface.co/datasets) relacionados a finanças, desde que sejam adequados ao contexto do desafio.

---

## Adaptações nos Dados

> Você modificou ou expandiu os dados mockados? Descreva aqui.

Foi sugerido produtos de finanças como :ações,Tesouro Direto,FLLS e Renda Fixa extraído da plataforma de repositórios fixos sugestionado.

---

## Estratégia de Integração

### Como os dados são carregados?
> Descreva como seu agente acessa a base de conhecimento.

O agente carrega a base de dados CSV buscando o produto ou listagem desses com base de entrada do usuário, após descarta os mesmo para limpeza 
e evitar conflitos de dados (informações) com novas entradas do usuário.

### Como os dados são usados no prompt?
> Os dados vão no system prompt? São consultados dinamicamente?

tecnologia systems prompt

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
