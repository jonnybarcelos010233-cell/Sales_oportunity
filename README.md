# Sales_oportunity
Modelagem de dados e pipeline ETL de oportunidades de vendas utilizando
# Sales Opportunity

Projeto de modelagem de dados e pipeline ETL baseado em oportunidades de vendas.

O conjunto de dados é dividido em quatro tabelas principais: `accounts`, `products`, `sales_teams` e `sales_pipeline`.

## Estrutura dos dados

### accounts

Contém as informações das empresas/clientes envolvidos nas oportunidades de venda.

```text
account_id        PK
account
sector
year_established
revenue
employees
office_location
subsidiary_of
```

- `account_id`: identificador único da empresa.
- `account`: nome da empresa.
- `sector`: setor de atuação.
- `year_established`: ano de fundação.
- `revenue`: receita da empresa.
- `employees`: número de funcionários.
- `office_location`: localização do escritório.
- `subsidiary_of`: empresa controladora, caso seja uma subsidiária.

---

### products

Contém os produtos comercializados pela empresa.

```text
product_id        PK
product
series
sales_price
```

- `product_id`: identificador único do produto.
- `product`: nome do produto.
- `series`: linha ou série do produto.
- `sales_price`: preço de venda.

---

### sales_teams

Contém as informações dos vendedores e da estrutura comercial.

```text
sales_agent_id    PK
sales_agent
manager
regional_office
```

- `sales_agent_id`: identificador único do vendedor.
- `sales_agent`: nome do vendedor.
- `manager`: gerente responsável.
- `regional_office`: escritório regional.

---

### sales_pipeline

Tabela principal do projeto, contendo as oportunidades de vendas e relacionando clientes, produtos e vendedores.

```text
opportunity_id    PK
sales_agent_id    FK -> sales_teams.sales_agent_id
product_id        FK -> products.product_id
account_id        FK -> accounts.account_id
deal_stage
engage_date
close_date
close_value
```

- `opportunity_id`: identificador único da oportunidade.
- `sales_agent_id`: vendedor responsável pela oportunidade.
- `product_id`: produto relacionado à oportunidade.
- `account_id`: cliente relacionado à oportunidade.
- `deal_stage`: estágio atual da negociação.
- `engage
