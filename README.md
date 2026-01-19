# 📊 Dashboard Analítico de Vendas | Power BI

![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![DAX](https://img.shields.io/badge/DAX-0078D4?style=for-the-badge&logo=microsoft&logoColor=white)
![Status](https://img.shields.io/badge/Status-Em%20Desenvolvimento-yellow?style=for-the-badge)

## 🎯 Sobre o Projeto

Dashboard executivo desenvolvido para análise estratégica de vendas e forecast preditivo, utilizando **DAX avançado** e técnicas de análise de dados sem necessidade de Python ou R.

### 📈 Principais Métricas
```
💰 Receita Total: R$ 33,88 Milhões
📊 Receita Média Diária: R$ 4,84 Milhões  
🎯 Taxa de Conversão: 19,83%
🎫 Ticket Médio: R$ 470,56
📦 Total de Leads: 363
✅ Total de Vendas: 72
📅 Período Analisado: Janeiro 2026
```

---

## 🚀 Funcionalidades Principais

### ✨ Análises Implementadas

- **KPIs Dinâmicos** - Métricas em tempo real com comparativos mensais
- **Análise Temporal** - Visualização de tendências diárias e evolução de receita
- **Forecast Inteligente** - Previsão de R$ 145,20 milhões baseada em média móvel
- **Análise de Conversão** - Funil de vendas com taxa de conversão de leads
- **Elasticidade de Preço** - Simulação de impacto de variações de preço
- **Performance por Período** - Comparativo de vendas por data

### 🎨 Recursos Visuais

- Design responsivo e profissional
- Paleta de cores estratégica para tomada de decisão
- Gráficos interativos com drill-down
- Indicadores visuais de performance (🔥 Excelente, ✅ Bom, ⚠️ Atenção)

---

## 🛠️ Tecnologias Utilizadas

| Ferramenta | Aplicação |
|------------|-----------|
| **Power BI Desktop** | Desenvolvimento e visualização |
| **DAX** | Medidas calculadas e análises avançadas |
| **Power Query (M)** | ETL e transformação de dados |
| **Excel** | Fonte de dados simulados |

---

## 📊 Medidas DAX Destacadas

### 1️⃣ Forecast com Média Móvel
```dax
Forecast Receita = 
VAR MediaMovel7Dias = 
    CALCULATE(
        AVERAGE(Vendas[Valor]),
        DATESINPERIOD(Calendar[Date], LASTDATE(Calendar[Date]), -7, DAY)
    )
VAR TendenciaCrescimento = [Receita MoM%]
RETURN
    MediaMovel7Dias * (1 + TendenciaCrescimento)
```

### 2️⃣ Taxa de Conversão Dinâmica
```dax
Taxa Conversão = 
DIVIDE(
    [Total de Vendas],
    [Total Leads],
    0
)
```

### 3️⃣ Crescimento Month-over-Month
```dax
Receita MoM% = 
VAR ReceitaMesAtual = [Receita Total]
VAR ReceitaMesAnterior = 
    CALCULATE([Receita Total], DATEADD(Calendar[Date], -1, MONTH))
RETURN
    DIVIDE(ReceitaMesAtual - ReceitaMesAnterior, ReceitaMesAnterior, 0)
```

---

## 💡 Principais Insights

🔍 **Descobertas da Análise:**

1. **Padrão de Sazonalidade** - Picos de receita identificados nos dias 4 e 6 de janeiro
2. **Elasticidade Positiva** - Ticket médio elevado indica potencial para segmentação premium
3. **Oportunidade de Conversão** - Taxa de 19,83% sugere espaço para otimização do funil
4. **Crescimento Projetado** - Forecast indica potencial de R$ 145M no próximo período

---

## 📁 Estrutura do Projeto
```
dashboard-vendas-powerbi/
│
├── 📊 Dashboard_Vendas.pbix          # Arquivo principal do Power BI
├── 📈 dados/                          # Dados de exemplo
│   └── vendas_sample.xlsx
├── 📸 screenshots/                    # Capturas de tela
│   ├── dashboard_principal.png
│   ├── analise_temporal.png
│   └── forecast.png
├── 📝 medidas_dax/                    # Biblioteca de medidas DAX
│   ├── kpis.dax
│   ├── time_intelligence.dax
│   └── forecasting.dax
└── 📚 README.md                       # Este arquivo
```

---

## 🎓 O Que Aprendi

### Competências Desenvolvidas:

✅ **DAX Avançado** - Criação de medidas complexas com time intelligence  
✅ **Storytelling com Dados** - Transformação de números em narrativas  
✅ **Design de Dashboards** - UX/UI aplicado a Business Intelligence  
✅ **Análise Preditiva** - Forecasting sem necessidade de Python/R  
✅ **Otimização de Performance** - Modelagem eficiente de dados  

### Desafios Superados:

💪 Implementar forecast preditivo apenas com DAX  
💪 Criar visualizações que equilibram estética e funcionalidade  
💪 Otimizar tempo de refresh para grandes volumes de dados  
💪 Desenvolver análise de elasticidade-preço simplificada  

---


---

## ## 📸 Prévia do Dashboard

   ### Dashboard Principal
   ![Dashboard Overview](dashboard_principal.png)

   ### Análise Temporal de Receita
   ![Análise Temporal](analise_temporal.png)

   ### Forecast Preditivo
   ![Forecast](forecast.png)

---

## 🤝 Como Contribuir

Contribuições são bem-vindas! Sinta-se à vontade para:

1. Fazer fork do projeto
2. Criar uma branch para sua feature (`git checkout -b feature/NovaAnalise`)
3. Commit suas mudanças (`git commit -m 'Adiciona nova análise de cohort'`)
4. Push para a branch (`git push origin feature/NovaAnalise`)
5. Abrir um Pull Request

---

## 👤 Autor

**[José Alexandre dos Santos Junior**

💼Supervisor de Vendas / Analista de Dados | Especialista em Power BI  
📧 email juninho-83@hotmail.com
🔗 [LinkedIn](www.linkedin.com/in/joséalexandredossantosjunior)  
🐙 [GitHub](https://github.com/junior19071983)

---

## 📝 Licença

Este projeto está em desenvolvimento contínuo e aberto para fins educacionais.

---

## ⭐ Agradecimentos

Se este projeto foi útil para você, considere dar uma ⭐!

---

**Última atualização:** Janeiro 2026
