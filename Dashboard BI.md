## Dashboard de Queijos Canadenses

Este projeto apresenta um dashboard interativo no Power BI, que oferece uma análise detalhada da indústria de queijos produzidos no Canadá. O painel aborda aspectos como variedades, províncias de origem, categorias, tipos de fabricação e o uso de diferentes leites.

**Observação**: Para garantir a precisão e a clareza das visualizações, os dados ausentes ("missings") foram tratados e filtrados durante o processo de preparação dos dados.

## Objetivo do Projeto

- Explorar a diversidade de queijos;
- Visualizar a produção por província;
- Comparar os diferentes tipos de fabricação;
- Analisar as categorias de queijos e seus percentuais;
- Analisar o tipo de leite usado.

  ## Base de Dados
- **Fonte**: Dataset público sobre queijos canadenses (Canadian Cheese Directory).  
- **Colunas principais**:  
  - Nome do queijo  
  - Província de origem  
  - Categoria  
  - Tipo de fabricação  
  - Tipo de leite utilizado  
  - Percentual de umidade  

## Visualização do Dashboard

![Image](https://github.com/user-attachments/assets/ec0b1818-bf3a-4ea1-9d22-b7387c76efc9)


## Medidas e Cálculos DAX


- **Total de informações na base de dados**: total_dados = COUNT(cheese_data[CategoryTypeEn])
- **Total de províncias**: total_prov_distic = DISTINCTCOUNT(cheese_data[ManufacturerProvCode])
- **Total de categorias**: total_categorias = COUNT(cheese_data[ManufacturingTypeEn])
- **Umidade média**: media_umidade = AVERAGE(cheese_data[MoisturePercent])/100
- **Distribuição por províncias**: total_prov = COUNT(cheese_data[ManufacturerProvCode])
- **Tipo de Fabricação**: total_fabricacao = COUNT(cheese_data[ManufacturingTypeEn])
- **Produção de leite**: total_leite = COUNT(cheese_data[MilkTypeEn])

## Análise

Uma análise do painel revela que a umidade média dos queijos é de aproximadamente 47,17%. Em termos de produção, a província de Quebec se destaca como a principal produtora. Quanto à categorização, os queijos mais produzidos são o Firm Cheese (34,25%) e o Soft Cheese (26,2%), respectivamente. Por fim, o leite de vaca é o insumo mais utilizado na fabricação de queijos no país.
