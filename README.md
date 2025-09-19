# Python Insights - Analisando Dados de Cancelamento de Clientes 

## Sobre o Projeto
Este projeto simula um **case real de Data Analytics**: uma empresa de serviços, com mais de **800 mil clientes**, percebeu que boa parte de sua base é composta por clientes **inativos** (cancelaram o serviço).  

O objetivo é **entender os principais motivos de cancelamento** e propor **ações práticas para reduzir a taxa de churn (cancelamento de clientes)**.

Base de dados: [Google Drive - cancelamentos_sample.csv](https://drive.google.com/drive/folders/1uDesZePdkhiraJmiyeZ-w5tfc8XsNYFZ?usp=drive_link)  

---

## Tecnologias e Bibliotecas Utilizadas
- **Python 3.x**
- [Pandas](https://pandas.pydata.org/) → manipulação e limpeza da base de dados  
- [Plotly Express](https://plotly.com/python/plotly-express/) → criação de gráficos dinâmicos  
- **Jupyter Notebook** → análise interativa e visualização dos dados  

---

## Etapas da Análise

### 1. Importação da base
- Carregamos a base `cancelamentos_sample.csv` usando **Pandas**.  
- Removemos a coluna `CustomerID` (não traz valor analítico).

###  2. Limpeza da base
- Identificação de valores nulos.  
- Exclusão de registros incompletos (`dropna`).  
- Ajuste dos tipos de dados.

###  3. Análise inicial
- Verificação da quantidade e percentual de clientes cancelados.  
- Resultado: **56,7%** dos clientes cancelaram.

### 4. Análise exploratória
- Criação de gráficos interativos com **Plotly** para entender:
  - Relação entre **ligações ao call center** e cancelamento.
  - Impacto da **duração do contrato** no churn.
  - Relação entre **dias de atraso no pagamento** e cancelamento.
  - Perfil de clientes ativos vs. cancelados.

###  5. Insights e Simulações
- **Clientes com mais de 4 ligações ao call center** → alta taxa de cancelamento.  
- **Contratos mensais** → quase todos cancelam.  
- **Atrasos acima de 20 dias** → clientes tendem a cancelar.  

   **Ações simuladas:**
- Criar alerta ao atingir 3 ligações no call center.  
- Oferecer desconto para clientes de contrato mensal.  
- Acionar cobrança preventiva a partir de 10 dias de atraso.  

Após aplicar esses filtros, a taxa de cancelamento caiu de **56,7% para 18,3%**.

---

##  Resultados Obtidos
- Identificação dos principais fatores de churn.  
- Redução potencial da taxa de cancelamento em mais de **38 pontos percentuais**.  
- Propostas de ações práticas para retenção de clientes.

---

##  Como Executar o Projeto

1. Instalar dependências:
```bash
pip install pandas numpy openpyxl nbformat ipykernel plotly
