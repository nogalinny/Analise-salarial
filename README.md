Análise de Dados de Salários em Tecnologia

Este projeto realiza uma análise exploratória de um conjunto de dados de salários no setor de tecnologia, utilizando Python e bibliotecas de manipulação e visualização de dados. O objetivo é extrair insights sobre os fatores que influenciam os salários, como nível de experiência, tipo de emprego, cargo, localização da empresa, modelo de trabalho e tamanho da empresa, além de observar tendências salariais ao longo dos anos.

Como Executar o Projeto
Para rodar este projeto em sua máquina e replicar a análise e os gráficos, siga os passos abaixo:

Pré-requisitos
Certifique-se de ter o Python instalado (versão 3.x recomendada).

Você precisará instalar as seguintes bibliotecas Python. Você pode fazer isso usando pip:

Bash

pip install pandas matplotlib seaborn numpy plotly scikit-learn
Estrutura do Projeto
salaries.csv: Este é o arquivo CSV que contém os dados de salários. Certifique-se de que ele esteja na mesma pasta que o seu script Python.
analise_salarios.py: Salve todo o código Python fornecido por você (desde a importação das bibliotecas até a geração dos gráficos) em um arquivo com este nome (ou outro de sua preferência, mas lembre-se de usá-lo na execução).
README.md: Este arquivo que você está lendo.
Execução
Clone o repositório (se estiver no Git) ou baixe os arquivos (salaries.csv e analise_salarios.py) para uma pasta em seu computador.
Abra seu terminal ou prompt de comando.
Navegue até o diretório onde você salvou os arquivos:
Bash

cd caminho/para/sua/pasta/do/projeto
Execute o script Python:
Bash

python analise_salarios.py
Ao executar o script, os gráficos serão exibidos sequencialmente em janelas separadas ou em seu ambiente Jupyter/IPython, se você estiver usando um.

Análise de Dados e Insights
Este projeto passa por várias etapas, desde o carregamento e tratamento dos dados até a geração de gráficos para visualização e extração de insights.

1. Tratamento de Dados
O dataset foi inspecionado para verificar a estrutura, tipos de dados, valores nulos e a quantidade de registros.

Tipos de Dados: Verificado que as colunas numéricas e categóricas estão com os tipos corretos (int64 para números e object para texto).
Valores Nulos: Não foram encontrados valores nulos, garantindo a integridade dos dados para análise.
Padronização: A coluna job_title foi padronizada para letras minúsculas e sem espaços em branco (.str.lower().str.strip()) para evitar duplicidade de registros.
Mapeamento: Colunas como experience_level, employment_type, remote_ratio e company_size foram mapeadas para valores mais descritivos e legíveis, facilitando a compreensão.

2. Processamento e Agrupamento de Dados
Após o tratamento, foram realizados agrupamentos para calcular as médias salariais com base em diversas variáveis:

Salário por Cargo: analytics engineering manager, data science tech lead e applied ai ml lead são os cargos com as maiores médias salariais.
Salário por País: Países como QA (Qatar), VE (Venezuela) e CZ (República Tcheca) aparecem com médias salariais elevadas, embora a maior parte dos dados seja concentrada nos EUA.
Salário por Nível de Experiência: A média salarial aumenta significativamente com o nível de experiência, sendo Executive Director o mais bem pago, seguido por Senior Expert, Intermediate e Junior.
Salário por Modelo de Trabalho: On-Site (presencial) apresenta a maior média salarial, seguido por Fully Remote (totalmente remoto) e Hybrid (50% Remote).
Salário por Tamanho da Empresa: Empresas de Mid-Sized Company (médio porte) pagam, em média, mais do que Large Enterprise (grandes empresas), e ambas superam Small Business (pequenas empresas).
Salário por Tipo de Contrato: Full-Time (tempo integral) é o tipo de contrato com a maior média salarial, superando Contract-Based, Part-Time e Freelance.
Salário por Ano: Há uma tendência de aumento nos salários médios ao longo dos anos, com 2024 e 2025 apresentando as maiores médias.

3. Visualização de Dados
Diversos gráficos foram gerados para facilitar a compreensão dos insights:

Top 10 Países com Maior Número de Registros no Dataset
Este gráfico de barras mostra que os Estados Unidos (US) dominam o conjunto de dados, representando a vasta maioria dos registros. Canadá (CA) e Reino Unido (GB) vêm em seguida, mas com uma representatividade muito menor. Isso indica um viés do dataset para o mercado americano.

Top 10 Países com Maior Média Salarial (USD)
Apesar do volume de dados, o gráfico de barras das médias salariais por país revela que, embora o US tenha muitos registros, outros países como QA (Qatar), VE (Venezuela) e CZ (República Tcheca) aparecem com médias salariais muito altas, destacando o potencial de remuneração em mercados específicos.

Salário vs. Nível de Experiência (com Cargo no Hover)
Intermediate e Senior Expert: Representam as maiores concentrações de pontos, indicando a maioria dos profissionais. Há uma variação salarial significativa nesses grupos, com profissionais de ambos os níveis recebendo salários baixos e altos.
Junior: Concentra-se em salários mais baixos, mas alguns pontos destoam com salários notavelmente altos, o que pode ser devido a cargos raros ou exceções.
Executive Director: Possui menos registros, mas uma faixa salarial muito alta e consistente, com pouca dispersão, o que é comum em cargos executivos de alto nível.

Média Salarial por Cargo e Tipo de Contrato
Full-Time: Dominante com as maiores médias salariais na maioria dos cargos, especialmente em Machine Learning Engineer, Research Scientist e Software Engineer, onde os salários facilmente ultrapassam $190k.
Contract-Based: É competitivo em áreas como Software Engineer, Data Engineer e Research Scientist, sugerindo que contratos por projeto em tecnologia avançada podem ser muito bem remunerados.
Freelance: Apresenta valores medianos, mas é interessante em Machine Learning Engineer (quase $100k) e Software Engineer.
Part-Time: Em geral, representa os menores salários. Curiosamente, Software Engineer em meio período pode ultrapassar $150k, talvez devido a carga horária reduzida em empresas de alto valor agregado.

Distribuição de Salários por Modelo de Trabalho
On-Site (Presencial) – 79,9%: A maior parte dos salários está concentrada em empregos presenciais, indicando um maior número de posições presenciais no dataset ou que empresas pagam mais nesse modelo.
Fully Remote (100% Remoto) – 20%: Apesar do crescimento do trabalho remoto, a fatia de salários é significativamente menor, podendo sugerir menos vagas bem remuneradas ou salários menores (compensados por flexibilidade).
Hybrid (50% Remoto) – 0,17%: Praticamente inexistente, o que pode indicar pouquíssimos registros híbridos no dataset ou que essas posições pagam valores muito baixos comparativamente.

Média Salarial por Tamanho da Empresa
Mid-Sized Company (Empresa de Médio Porte) – 160k USD: Maior média salarial, possivelmente devido à necessidade de atrair talentos em fase de crescimento acelerado.
Large Enterprise (Grande Empresa) – 150k USD: Fica ligeiramente atrás das médias empresas, talvez devido a estruturas salariais mais padronizadas e benefícios indiretos.
Small Business (Pequena Empresa) – 90k USD: Menor média salarial, o que é natural devido a menores recursos, embora possam oferecer outros benefícios.

Média Salarial por Tipo de Contrato e Nível de Experiência
Contract-Based: Executive Director lidera com mais de 190k USD.
Freelance: Médias mais baixas, especialmente para níveis mais altos.
Part-Time: Faixas mais compactas e médias salariais mais baixas.
Full-Time: Apresenta os valores mais altos em todas as categorias, especialmente para Executive Director (acima de 200k USD) e Senior Expert (cerca de 175k USD), reafirmando que a carreira tradicional oferece maior retorno financeiro com mais experiência.

Evolução da Média Salarial por Cargo ao Longo dos Anos
Machine Learning Engineer: Teve um pico em 2020, mas se estabilizou em 190k–200k USD.
Data Scientist & Software Engineer: Queda em 2021, forte alta em 2022, e estabilidade acima de 180k USD em 2025, mostrando alta valorização.
Manager: Crescimento acentuado entre 2021 e 2023, mantendo-se no topo (cerca de 200k USD) em 2024 e 2025.
Data Engineer: Crescimento constante desde 2021, aproximando-se de 150k USD em 2025.
Research Scientist: Cresce até 2023, mas cai em 2024–2025.
Engineer (genérico) e Data Analyst: Mantêm os salários mais baixos da lista, com Data Analyst abaixo de 100k USD, reforçando que quanto mais especializada a função, maior a remuneração.
