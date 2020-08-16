# fraud-detection-ml: Aplicação de Machine Learning em Análise de Fraude de Cartão de Crédito



Com a expansão do uso da Internet e seus adventos, o meio comercial foi transformado pela possibilidade de se comprar e vender online. O comércio eletrônico trouxe inúmeras vantagens, como a praticidade na hora de pesquisar e comprar, redução de custos de infraestrutura, como consequência, redução de preço dos produtos, e a facilitação da logística geográfica, tornando viável comprar de lojas distantes de sua região e até em outros países.

Os sites e-commerce costumam oferecer variadas formas de pagamento, dentre elas há, por exemplo, opções de Boleto Bancário, Débito Online e Cartão de Crédito. Os cartões de crédito tem sido campeões de vendas no meio online. De acordo com o estudo E-commerce Radar 2018, 70,4% dos pedidos aprovados no comércio eletrônico brasileiro são feitos a partir dessa forma de pagamento, que ainda tem a maior taxa de aprovação, que chega a 87,1%.

Porém esta grande preferência por parte da população traz consigo um recorrente problema: o cartão de crédito se tornou um dos meios mais visados para a realização de golpes e fraudes. Muitos desses casos de fraudes são resultado do descuido dos usuários ou incidentes de furto e roubo. Os portadores do cartão de crédito devem tomar os cuidados necessários para que não haja vazamento de suas informações pessoais, todavia, é também uma obrigação da organização que oferece o serviço do cartão estar provida de ferramentas antifraude para evitar o transtorno de ambos os lados.


<b> O problema proposto</b>

Casos de fraude em compra de cartão de crédito, podem causar transtornos tanto para a operadora do cartão, que poderá ter que cobrir a dívida gerada, tanto para o usuário, que precisará entrar em contato com a empresa responsável e estar munido de provas de que não foi o mesmo que realizou a compra. Por esse motivo, é importante que as instituições financeiras que oferecem esse serviço, tenham processos fortes de validação e segurança. Dentre os principais tipos de fraude de cartão de créditos, temos: Clonagem de cartão de crédito; Gerador de números falsos de cartões; Ligações e mensagens falsas para roubo de dados.

Como ferramentas para evitar que esses problemas ocorram, é importante que seja realizado um cruzamento de dados, garantindo a identidade do comprador. Outro aspecto importante é investir na inteligência e análise de dados, avaliando o histórico financeiro e perfil do cliente. A comunicação com o cliente nesse cenário é fundamental, seja mantendo-o avisado sobre sua movimentação ou até confirmando uma transação financeira, antes de efetivá-la, se a mesma apresentar um comportamento diferente do usual. Essa avaliação, porém, deve ser feita com cautela, para que também não sejam gerados transtornos em bloqueios de compras sem fraude. 

De modo a demonstrar a importância e usabilidade da ciência de dados no contexto de detecção de fraudes, será analisada uma base de dados contendo 284.807 transações de cartão de crédito realizadas em 2013. As administradoras dos cartões de crédito são europeias e 0.172% das transações são fraudulentas. O intuito deste estudo é aplicar machine learning para detecção de operações com fraude e demonstrar como o uso de inteligência artificial pode antecipar riscos e ajudar na tomada de decisão por parte das instituições financeiras responsáveis.

<b> Coleta de Dados </b>

A base de dados que será utilizada para demonstrar a aplicação de machine learning na detecção de fraudes, se trata de um conjunto de dados de transações de cartão de crédito de administradoras europeias. Este dataset foi coletado e analisado em 2013 durante uma pesquisa da Worldline and the Machine Learning Group da ULB (Université Libre de Bruxelles) sobre mineração de big data e detecção de fraude.

O conjunto de dados foi disponibilizado no site Kaggle (kaggle.com/mlg-ulb/creditcardfraud), onde foi realizado o donwload do mesmo no formato CSV. O Kaggle é uma plataforma online da comunidade de cientistas de dados e machine learning, onde são disponibilizados datasets, resolução de problemas, competições e cursos, de propriedade da Google.

O dataset é composto por 284,807 registros, na qual 492 caracterizam fraude. O mesmo contém apenas variáveis de entradas numéricas, que são o resultado de uma transformação PCA. A Análise de componentes principais (PCA) é uma das reduções de dimensões lineares mais populares e é um método baseado em projeção que transforma os dados projetando-os em um conjunto de eixos ortogonais. O PCA foi usado nesse cenário para proteger as informações pessoais dos clientes, por esse motivo, não será possível ter acesso aos rótulos e informações básicas da maioria das variáveis que serão aqui tratadas.

<ul>
<li>Time (Tempo): Número de segundos decorridos entre esta transação e a primeira transação no conjunto de dados - Inteiro</li>
<li>Amount (Valor): Valor da transação - Decimal</li>
<li>Classe: 	1 para fraudulenta / 0 para não fraudulenta	- Inteiro</li>
<li>V1 [...] V28: 28 variáveis que são resultado de uma redução de dimensionalidade (PCA) para proteger a identidade do usuário e recursos confidenciais - Decimal</li>
</ul>

<b> Scripts </b>

O repositório está dividido em 3 scripts

<ul>
<li>Script para tratamento de dados: Contempla as análises sobre a melhor forma de tratar os dados e o que foi considerado para a escolha das técnicas;</li>
<li>Script para exploração de dados: Contempla as análises das features disponíveis nas bases;</li>
<li>Script para aplicação dos modelos de machine larning: Após tratamento dos dados e escolha das features, nesse script há a aplicação dos modelos de Machine Learning e a avaliação de métricas dos mesmos.</li>

