# Hub Financeiro Pessoal

Planilha em Excel que reúne **lançamentos, dashboard com filtros, simulador de investimentos e apoio à declaração de IR** em um único arquivo, com menu de navegação.

Projeto final do bootcamp **Santander – Excel com IA e Claude**, realizado na plataforma da **Digital Innovation One (DIO)**. Ele une, em uma só planilha, os três projetos que desenvolvi durante o curso.

> Todos os dados, valores e percentuais são **fictícios** e servem apenas para fins educacionais.

![Dashboard](images/dashboard_geral.png)

## Objetivo

Responder, em um só lugar, a três perguntas do dia a dia financeiro:

1. **Para onde vai o meu dinheiro?** Dashboard com indicadores e gráficos filtrados por ano e trimestre.
2. **Quanto da minha sobra pode virar patrimônio?** Simulador de investimentos em FIIs, com divisão do aporte por perfil de investidor.
3. **Como organizo os dados da declaração de IR?** Consolidação de rendimentos, deduções e checklist de documentos a partir dos mesmos lançamentos.

## O que o projeto reúne

| Projeto do bootcamp | O que veio para o Hub |
|---|---|
| **IR Fácil** (organizador da declaração) | Menu com HYPERLINK, validação de dados, formatação condicional, checklist de documentos |
| **Dashboard GameZone** (painel de vendas) | Tabela estruturada, SUMIFS com filtros, Top 5 com LARGE + INDEX/MATCH, gráficos dinâmicos |
| **Fersan Invest** (simulador de FIIs) | VF, PROCV com chave composta, perfis de investidor, gráfico de pizza |

Novo neste projeto: a sobra mensal calculada pelos lançamentos alimenta o simulador, e o **NPER** estima em quantos anos a meta de patrimônio é atingida.

## Abas

| Aba | Função |
|---|---|
| **Menu** | Botões de navegação para todas as abas e legenda de cores |
| **Lançamentos** | Base de receitas e despesas em tabela (`tb_lanc`), com listas suspensas e validações |
| **Dashboard** | Filtros de ano e trimestre, 6 indicadores, 4 gráficos e Top 5 categorias de gasto |
| **Simulador** | Patrimônio, dividendos, cenários por prazo, tempo até a meta e divisão do aporte por perfil |
| **IR** | Rendimentos do ano, deduções com limites e checklist de documentos |
| **Apoio** | Listas, parâmetros editáveis e tabelas de cálculo que alimentam as demais abas |
| **Sobre** | Recursos usados, premissas, limitações e registro do uso de IA |

## Funcionalidades

**Dashboard**
- Indicadores: receitas, despesas, saldo, taxa de poupança, maior gasto e número de lançamentos.
- Gráficos: receitas x despesas por mês, despesas por categoria, composição das receitas e saldo acumulado.
- Filtros de **Ano** e **Trimestre** que atualizam todos os indicadores e gráficos.

**Simulador**
- Calcula o patrimônio acumulado e os dividendos mensais estimados com `VF`.
- Mostra cenários de 2 a 30 anos e o tempo até a meta com `NPER`.
- Divide o aporte entre seis tipos de FII conforme o perfil (Conservador, Moderado ou Arrojado), com `PROCV` e conferência automática de 100%.

**IR**
- Consolida rendimentos tributáveis e isentos do ano-calendário escolhido.
- Aplica os limites de dedução de educação e PGBL, que ficam como parâmetros editáveis na aba Apoio.
- Checklist de documentos com status colorido (Pendente, Recebido, Não se aplica).

## Recursos de Excel utilizados

`SUMIFS` · `COUNTIFS` · `INDEX/MATCH` · `LARGE` · `VF` · `NPER` · `PROCV` · `HYPERLINK` · `IFERROR` · tabela estruturada · intervalos nomeados · validação de dados · formatação condicional · gráficos de colunas, barras, linha e pizza

## Como usar

1. Baixe o arquivo `hub_financeiro_pessoal.xlsx` e abra no **Excel**.
2. Comece pelo **Menu** e navegue pelos botões. Cada aba tem o link **<< Voltar ao Menu**.
3. Em **Lançamentos**, para incluir um registro, preencha Data, Tipo, Categoria, Descrição e Valor na última linha e copie as colunas cinzas (Ano, Mês, Trim) da linha acima. A planilha lê até a linha 1000.
4. No **Dashboard**, escolha o ano e o trimestre nos seletores amarelos.
5. No **Simulador**, ajuste perfil, prazo, % da sobra investida e meta.
6. Em **IR**, escolha o ano-calendário e atualize o status do checklist.

**Cores:** texto azul = pode editar · fundo cinza = calculado por fórmula · fundo amarelo = filtros e seletores principais.

## Premissas e limitações

- O retorno mensal (0,80%) e o rendimento em dividendos (0,70%) do simulador são **premissas de exemplo**, sem garantia de resultado.
- Os percentuais por perfil de investidor são exemplos de estudo e **não constituem recomendação de investimento**.
- O limite de dedução com educação (R$ 3.561,50) e o limite do PGBL (12% da renda tributável) são parâmetros editáveis. Confira os valores vigentes no site da Receita Federal.
- A aba IR **consolida os dados e não calcula o imposto devido**.
- A sobra média considera anos completos na base (meses = anos x 12).

## Uso de IA

O projeto foi planejado, montado e conferido com apoio do **Claude**: estrutura das abas, fórmulas, validações e gráficos. Os resultados foram verificados comparando os totais da planilha com cálculos independentes. O registro está na aba **Sobre**.

## Estrutura do repositório

```
hub-financeiro-pessoal-excel/
├── hub_financeiro_pessoal.xlsx
├── README.md
└── images/
    ├── menu.png
    ├── dashboard_geral.png
    ├── dashboard_filtrado.png
    ├── simulador.png
    └── sobre.png
```

## Prints

| Dashboard (todos os períodos) | Dashboard (2025 + T1) |
|---|---|
| ![Dashboard geral](images/dashboard_geral.png) | ![Dashboard filtrado](images/dashboard_filtrado.png) |

| Menu | Simulador |
|---|---|
| ![Menu](images/menu.png) | ![Simulador](images/simulador.png) |

## Autor

**Gabriel** · [GitHub](https://github.com/Gabriielll)

Bootcamp **Santander – Excel com IA e Claude** · [Digital Innovation One (DIO)](https://www.dio.me)
