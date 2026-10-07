# Sales_oportunity
Modelagem de dados e pipeline ETL de oportunidades de vendas utilizando

accounts
--------
account_id          PK
account
sector
year_established
revenue
employees
office_location
subsidiary_of


products
--------
product_id          PK
product
series
sales_price


sales_teams
-----------
sales_agent_id      PK
sales_agent
manager
regional_office


sales_pipeline
--------------
opportunity_id      PK
sales_agent_id      FK → sales_teams.sales_agent_id
product_id          FK → products.product_id
account_id          FK → accounts.account_id
deal_stage
engage_date
close_date
close_value
