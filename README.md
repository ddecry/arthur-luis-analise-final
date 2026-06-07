# State of Data Brazil 2024: fatores associados ao salário

**Integrantes:** Arthur de Holanda e Luis Felipe  
**Dashboard público:** [Looker Studio](https://datastudio.google.com/reporting/b035699e-19c4-4010-85e2-b66ddfe8f1fb)

## Pergunta central

Quais fatores mais influenciam o salário de um profissional de dados no Brasil em 2024?

## Resposta executiva

A análise de 4,863 respostas com faixa salarial informada indica que **senioridade e experiência acumulada em dados** são os fatores mais diretamente associados ao salário. O salário mediano estimado passa de R$ 3.500 entre profissionais júnior para R$ 14.000 entre profissionais sênior. Na correlação de Spearman, senioridade apresenta coeficiente de 0.734 e experiência em dados, 0.658.

A **família de cargo** também ajuda a explicar diferenças: carreiras de engenharia, ciência de dados e IA, análise e produto ocupam posições distintas no mercado. Região, escolaridade, gênero, raça/cor e uso de ferramentas complementam o contexto, mas não devem ser interpretados isoladamente como causas. A base é observacional e os salários são estimados a partir dos pontos médios das faixas respondidas.

## Estrutura do repositório

```text
arthur-luis-analise-final/
├── README.md
├── notebook/
│   └── arthur-luis-felipe-analise.ipynb
├── relatorio/
│   └── arthur-luis-felipe-relatorio.pdf
├── dashboard/
│   └── dados_dashboard.csv
└── dados/
    └── Final Dataset - State of Data 2024 - Kaggle - df_survey_2024.csv
```

## Principais decisões de limpeza

- Renomeamos 17 colunas-chave usando as descrições oficiais presentes na base.
- Convertemos faixas salariais fechadas em pontos médios. Para `Menos de R$ 1.000/mês`, adotamos R$ 500; para `Acima de R$ 40.001/mês`, adotamos R$ 45.000.
- Preservamos não respostas e a opção `Prefiro não informar` em gênero e raça/cor. Esses valores não foram imputados.
- Padronizamos famílias de cargo com um mapa explícito, mantendo o cargo original para auditoria.
- Tratamos SQL, Python e R como variáveis binárias independentes.

## Referências

- [State of Data Brazil 2024-2025 - Data Hackers + Bain & Company](https://www.kaggle.com/datasets/datahackers/state-of-data-brazil-20242025)
- Python, pandas, NumPy, Matplotlib e seaborn.

## Limitações

Os resultados descrevem associações em uma pesquisa voluntária; não comprovam causalidade. A conversão das faixas salariais introduz aproximação, especialmente na faixa aberta superior. Diferenças salariais por gênero e raça/cor exigem cuidado ético e controle de fatores como senioridade, cargo, região e setor.
