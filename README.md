# Projeto de B.I - Conjunto de Dados Públicos de E-Commerce Brasileiro da Olist Store
                  
## _Escolha do desafio:_

Optei por escolher um dataset do kaggle que trouxesse uma abordagem analítica e que possibilitasse uma abrangência sofisticada de tendencias e padrões mais próximos à realidade da empresa, desta forma escolhi o “Brazilian E-Commerce Public Dataset by Olist”. Este conjunto de dados contém informações públicas do comércio eletrônico brasileiro de pedidos feitos na Olist Store.
Os dados comerciais mencionados são autênticos, mas foram submetidos à anonimização. As referências específicas a empresas e parceiros citados no texto foram substituídas por nomes das grandes casas de Game of Thrones. O dataset pode ser acessado através do link: 

                 		https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce?resource=download
                        
## _Importação dos dados:_

Foi feita uma importação local padrão dos arquivos .csv. Uma vez que o dataset apresenta dados estáticos de 2016 a 2018, esta é a forma mais adequada de acessarmos estes dados. Caso os dados fossem atualizados diariamente, teriamos duas opções para importação, a padrão, via API, utilizando endereço da web dos arquivos e uma opção mais complexa, utilizando script de automação em Python para atualização das bases locais. Este último é de grande valia quando possuimos processos internos que não se comunicam de forma padrão com a web, devido a aspectos como segurança. 

Inclusive esta é uma sugestão de melhoria para importações menos compatíveis, além da economia de tempo, evita passivos de erro de atualizações manuais.
Os dados estão limpos e não necessitam de tratamento. O dataset foi estruturado de forma relacional, desta forma foi feita a montagem do relacionamento conforme apresentado na imagem relationship.

## _Montagem do dashboard:_

Como primeiro passo para início da montagem do dashboard fiz o desenvolvimento de algumas perguntas de negócios, que vão basear todo contexto. São elas:

- Como podemos categorizar as necessidades de cada página do dashboard?
- Nível Gerenciamento - Dados gerais, com uma amostragem ampla com o objetivo de mapear os principais resultados.   

        -> Qual número de vendas?
        -> Qual número de produtos?
        -> Qual número de cidades e estados de abrangência?
        -> Qual meu faturamento por período(FROM YEAR TO DAY)?
        -> Quais são as principais categorias que contribuem para o faturamento?
        
- Nível de Supervisão 1 – Com uma amostragem reduzida, o foco está nos insights críticos relacionados à visão operacional de tratamento a longo prazo.

        -> Quais as principais categorias mais importantes, em cada período(FROM YEAR TO DAY)?
        -> Escalando a pergunta acima, quais os principais produtos.
        -> A hora da compra influencia nos meus resultados?
        
- Nível de Supervisão 2 – Amostragem reduzida, com enfoque na supervisão dos indicadores de entrega.

        -> Quais produtos representam os maiores gaps de entrega?
        -> Como posso visualizar os meus indicadores de tempo entre processos
        !!(As empresas possuem diversos indicadores para aferição de medidas entre períodos, que geralmente representam processos. Foram criados indicadores específicos, baseados em intuição básica do assunto)
    
        !!Indicadores de Tempo de Processo Criados:
        -> Approval_Days_Order - Dias entre a compra e a aprovação do pedido
        -> Carrier_Receipt_Days - Dias entre a aprovação e o recebimento pela transportadora
        -> Customer_Receiver_Days - Dias entre o recebimento pela transportadora e o recebimento do cliente
        -> Estimated_Time_Gap - Gap entre a data de entrega e a data estimada
        
- Nível de Operação – A amostragem é mínima, com o objetivo de estratificar um problema específico que geralmente é detectado em níveis de visão superiores.

        -> Como posso acompanhar o status dos meus pedidos?
        -> Como posso estratificar problemas de um pedido específico?

## _Destaques Layout_

A Layout utilizado é composto por componentes e cores agradáveis. Desta forma não perdemos o foco das partes interessadas, mantendo-os, de olho nos elementos de análise. Os ícones da página inicial estão dispostos de maneira a fornencer uma explicação breve, de forma mais rápida que um texto, no painel operacional, há o uso dos dois elementos visuais, devido a quantidade de painéis, apenas o ícone poderia causar confusão ao invés de ajudar.
Foram selecionados gráficos que atendem às demandas de apresentação das análises previamente identificadas, de modo a tornar a leitura dos dados mais fácil e permitir aos leitores uma rápida conversão dos dados em informações. Como por exemplo, temos neste dasboard: gráficos de pizza, em explicações de categorias, gráficos de barra e colunas, para explicar rankings de agrupamentos, diferenciando se apenas pelo tamanho dos dados dos eixos, números consolidados exibidos por meio de cartões, entre outros.

## _Principais Impactos_

Esse projeto foi desenvolvido com o pensamento de escalonar por completo os níveis de gestão de uma empresa de e-commerce, desta forma podemos acompanhar desde a primeira página, a trajetória do sucesso ou da problematização de tópicos como: vendas por cidade, avaliações por produto, faturamento por produto, categoria ou região, alcance físico das vendas e sucesso das entregas em cada região, entre outras opções de análise.

Em uma empresa com foco operacional, essas análises provavelmente se tornariam Indicadores Chave de Performance (KPIs), onde as equipes trabalhariam para atingir diferentes tipos de metas. Esse tipo de abordagem é fundamental para garantir o controle dos resultados operacionais e financeiros da empresa. Ao estabelecer KPIs claros, mensuráveis e atingíveis, as equipes podem acompanhar seu progresso e identificar rapidamente áreas que precisam de melhorias, o que pode levar a uma maior eficiência, redução de custos e aumento da lucratividade.

Ao analisar essas equipes, podemos ver que elas são compostas por indivíduos diversos, separados em diferentes setores, cada um com suas próprias atribuições. Uma adaptação básica deste projeto poderia transformá-lo em um suporte completo para essas equipes, adicionando páginas específicas de indicadores para cada setor. Essas páginas ofereceriam análises interativas, bem como páginas estáticas que, com automação de atualização e assinatura, forneceriam resultados corriqueiros, como: dia_anterior, mês_atual, semana_anterior e semana_atual, a fim de atender às necessidades de busca por resultados por parte da equipe.

## _Contéudos:_

-> Relationship: Relacionamento aplicado ao dataset
-> Dataset: Pasta com as bases de dados utilizadas
-> Projeto Pedidos E-Commerce: Arquivo .pbix do projeto
-> 
