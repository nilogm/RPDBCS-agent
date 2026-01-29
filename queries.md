# Queries

The queries below are presented in Portuguese, as they were used as such during experiments.

## Tool 1: Search for Similar Signals

The questions contain placeholder values which are replaced by:
 - [CLASSE]: any of the 5 main fault class types
 - [QTD_SINAIS]: specific amount of signals to return (in the paper, 2 or 5)
 - [FEATURE]: characteristic of the signal to use when comparing with other signals

Existe algum sinal parecido com este?\
Estou vendo algo interessante nesse sinal, tem outros assim?\
Tem algum outro sinal que tenha características parecidas com este?\
Quais sinais dariam uma boa comparação com este?\
Se eu olhar só sinais da classe [CLASSE], quais são os mais parecidos?\
Tem algum sinal da classe [CLASSE] que seja parecido com este?\
Pode me mostrar [QTD_SINAIS] sinais parecidos com este?\
Quais seriam os [QTD_SINAIS] sinais mais parecidos com este?\
Pode me mostrar os [QTD_SINAIS] sinais da classe [CLASSE] mais parecidos com este?\
Me mostre [QTD_SINAIS] exemplos da classe [CLASSE] que sejam semelhantes a este.\
Liste outros [QTD_SINAIS] sinais com [FEATURE] semelhantes.\
Estou vendo algo interessante nesse sinal, você poderia me mostrar outros [QTD_SINAIS] com [FEATURE] similar ao deste?\
Quais seriam os [QTD_SINAIS] sinais da classe [CLASSE] mais parecidos com este quando observando somente [FEATURE]?\
Você consegue listar [QTD_SINAIS] sinais da classe [CLASSE] que tenham [FEATURE] similar a deste sinal?\
Levando em conta somente [FEATURE] deste sinal, existe algum outro parecido com este?\
Considerando somente [FEATURE], tem algum outro sinal que seja semelhante a este?\
Entre os sinais da classe [CLASSE], tem algum sinal parecido com este que apresente [FEATURE] similar?\
Mostre outros exemplos da classe [CLASSE] que têm [FEATURE] igual ou similar ao deste sinal.\

## Tool 2: Get Second Fault Prediction

Não tenho certeza dessa classificação, qual outra devo considerar?\
Se o diagnóstico não estiver correto, qual seria a segunda falha mais provável?\
Se caso essa classe estiver errada, qual seria a outra alternativa?\
Existe outra classificação que pode explicar esse sinal?\
Qual outra classificação faz sentido nesse contexto?\
E se não for essa classificação, qual é a próxima mais provável?\
Há outra classificação que eu deveria investigar também?\
Caso o sistema esteja enganado, qual seria a segunda hipótese?\
Não estou seguro de que seja essa classificação, qual outra opção existente?\
Esse sinal poderia corresponder a outro tipo de diagnóstico?\
Qual a classificação seguinte que também pode ser interessante?\
Se eu descartar esse diagnóstico, qual seria a próxima classe suspeita?\
Pode haver mais de uma interpretação para esse sinal? Qual seria a segunda?\
Se essa classificação não se confirmar, o que mais poderia ser?\
Suponha que essa classificação esteja incorreta, qual outra explicação faria sentido para o sinal?\
Existe outra classificação aplicável aqui?\
Qual a segunda classificação que o sistema identificou como provável?\
Não estou totalmente convencido, qual outro diagnóstico devo me atentar?\
Se não for essa classificação, qual a segunda opção?\
Se essa classificação não for confirmada, qual seria o segundo tipo que deveria ser analisado?\
Qual classificação alternativa faz sentido além dessa?\
Se essa primeira hipótese cair, qual a segunda classificação que surge?\
Esse sinal pode indicar outra classificação provável também? Qual seria?\
Se eu não considerar essa classificação, existe outra?\
Existe alguma segunda hipótese de classificação que também se encaixa nesse sinal?\
Além dessa classificação principal, qual seria a próxima mais plausível?\
Há outra possibilidade de classificação interessante a ser analisada?\
Qual a segunda alternativa de interpretação para esse sinal?\
Se houver engano, qual classificação aparece logo em seguida?\
Essa classificação pode ser falsa? Qual seria a segunda hipótese?\
O sistema levantou mais de uma possibilidade de classificação? Qual é a próxima?\
Qual seria a segunda opção de diagnóstico que não devo ignorar?\
Há alguma outra classificação que você recomendaria investigar?\
Qual seria a segunda possibilidade de diagnóstico que deveríamos analisar?\
Se essa não for o diagnóstico correto, qual outro poderia ser?\
Se eu descartar esse diagnóstico, qual seria a próxima sugestão?\
Existe outra interpretação possível para sinal?\
Se não considerarmos essa análise, qual seria um próximo diagnóstico?\
Suponha que essa indicação não esteja correta, que outra possibilidade deveria me atentar?\
Qual outra sugestão de classificação poderia existir?\
Se essa classificação não estiver certa, que outra análise poderia fazer sentido?\
Existe outra possibilidade de resultado que poderia fazer sentido para este sinal? 
Há outra possiblidade de classificação que vale a pena conferir?


## Tool 3: Predict Without a Feature

The questions contain placeholder values which are replaced by:
 - [FEATURE]: characteristic of the signal to omit from the training process

Será que sem [FEATURE] o tipo de falha mudaria?
Se a gente não olhar [FEATURE], que outro problema poderia estar acontecendo?
Não tenho certeza se essa é a falha certa, será que ignorando [FEATURE] da análise surge outra possibilidade?
Se eu não considerar [FEATURE], o sistema poderia indicar outro tipo de falha?
Se deixarmos de lado [FEATURE], existe outra falha que faria sentido?
Qual outro problema poderia aparecer se ignorarmos [FEATURE]?
Será que [FEATURE] está influenciando muito? Que falha daria sem ela?
Se não levarmos em conta [FEATURE], o que mais o sistema poderia sugerir?
Olhando esse sinal, se não considerarmos [FEATURE], qual outra falha poderia ser relevante?
Os padrões nesse sinal me chamaram atenção, será que sem [FEATURE] surge outra hipótese de falha?
Não tenho certeza sobre essa indicação de falha; será que existe outra explicação sem [FEATURE]?
Se a leitura de [FEATURE] for ignorada, qual outra falha poderia se encaixar nesse padrão?"
Esse sinal ainda aponta para a mesma falha se a gente não considerar [FEATURE]?
Se a gente desconsiderar [FEATURE], tem alguma outra falha que vale a pena checar?
Se eu não usar [FEATURE], que falha alternativa o sistema mostraria?
Será que existe alguma outra falha que explique esse sinal sem [FEATURE]?
O que o sistema sugeriria se deixássemos [FEATURE] de fora?
Se eu excluir [FEATURE], quais outras possibilidades de falha ainda fazem sentido?
Que outra falha poderia aparecer sem [FEATURE]?
Se ignorarmos [FEATURE], que tipo de falha alternativa poderia surgir?
Se deixarmos [FEATURE] de fora, qual problema seria indicado?
Será que essa falha indicada se mantém para a mesma falha sem considerar [FEATURE]?
Se a gente deixar de lado [FEATURE], existe algum outro problema que o sistema apontaria?
Se retirarmos [FEATURE], qual falha alternativa faria sentido?
Observando esse sinal, que outro tipo de falha poderia aparecer sem [FEATURE]?
Se não contarmos [FEATURE], qual seria a próxima suspeita de falha?
Será que há outra falha que explique esse sinal sem [FEATURE]?
Se a gente não usar [FEATURE], quais falhas poderiam ser consideradas?
Sem [FEATURE] presentes nesse sinal, que outra falha poderia ser indicada?
Será que ignorar [FEATURE] mudaria totalmente a interpretação da falha?
Se a gente não levar [FEATURE] em conta, existe outra falha compatível com esse sinal?
Observando esse sinal sem [FEATURE], qual outro tipo de falha poderia ser apontado pelo sistema?
Estou em dúvida sobre a falha exibida, se omitirmos [FEATURE], o que pode surgir?
Supondo que não levemos [FEATURE] em conta, que falha poderia aparecer?
Se [FEATURE] não for confiável, qual outra falha o sistema poderia levantar?
