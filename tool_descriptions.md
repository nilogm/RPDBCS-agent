# Tool descriptions

The tool descriptions below are presented in Portuguese, as used during experiments.

## Tool 1: Search for Similar Signals

Obtém os sinais mais semelhantes com base nas features fornecidas.\
Execute SEMPRE que o usuário solicitar exemplos de sinais similares ao fornecido.\
\
A relação entre as características do sinal e as features está descrita abaixo:\
- nível de ruído em torno de 3Hz e 5Hz: ['median(3,5)']
- comportamento da curva entre 5Hz e 19Hz: ['a', 'b']
- amplitude do pico na primeira harmônica: ['peak1x']
- ruído ao redor da primeira harmônica: ['median(freq-1,freq+1)', 'rms(freq-1,freq+1)']
- amplitude do pico na segunda harmônica: ['peak2x']
- rotação real do equipamento em Hz: ['real_rotation_hz']

Busca os sinais mais semelhantes a um fornecido com base nas features especificadas.\
Args:
- features (dict[str, float]): Dicionário com nomes das features como chaves para os valores reais (float).
    - Chaves OBRIGATÓRIAS esperadas:
      - "a"
      - "b"
      - "real_rotation_hz"
      - "peak1x"
      - "peak2x"
      - "rms(freq-1,freq+1)"
      - "median(freq-1,freq+1)"
      - "median(3,5)"
- num_examples (int): Número de sinais semelhantes a serem retornados.
- fault_class (str, optional): Classe de falha para filtrar os sinais. Se não fornecida, serão considerados sinais de todas as classes.
  - Valores válidos: 'Normal', 'Roçamento', 'Desalinhamento', 'Desbalanceamento', 'Falha de sensor'.
- feature_filter (list[str], optional): Lista com os nomes das features que devem ser consideradas na análise se o usuário explicitamente citar a característica que deve ser considerada. Por exemplo: ['a', 'b'], ao considerar somente o comportamento da curva entre 5Hz e 19Hz ou ['median(freq-1,freq+1)', 'rms(freq-1,freq+1)'] ao considerar somente o ruído ao redor da primeira harmônica.

## Tool 2: Get Second Fault Prediction

Obtém a segunda classe de falha mais provável de um sinal com base em todas as 8 features de entrada.\
Use esta ferramenta SOMENTE quando a intenção do usuário é obter uma classificação alternativa SEM remover algumas características do sinal no processo.\
NUNCA use essa ferramenta se o usuário quiser uma classificação com remoção de uma característica do sinal.\


Args:
 - features (dict[str, float]): Dicionário com nomes das features como chaves e valores float.
   - Chaves OBRIGATÓRIAS esperadas:
      - "a"
      - "b"
      - "real_rotation_hz"
      - "peak1x"
      - "peak2x"
      - "rms(freq-1,freq+1)"
      - "median(freq-1,freq+1)"
      - "median(3,5)"

## Tool 3: Predict Without a Feature
Executa a classificação e identifica o tipo de falha mais provável de um sinal, permitindo realizar a análise com alguma feature intencionalmente desconsiderada.\
Utilize esta ferramenta SEMPRE que o usuário solicitar uma análise parcial, em que deseja ignorar, remover ou desconsiderar alguma característica do sinal.\
NUNCA execute esta ferramenta se não for fornecido explicitamente quais características devem ser omitidas.\
\
A relação entre as características do sinal e as features está descrita abaixo:
- nível de ruído em torno de 3Hz e 5Hz: ['median(3,5)']
- comportamento da curva entre 5Hz e 19Hz: ['a', 'b']
- amplitude do pico na primeira harmônica: ['peak1x']
- ruído ao redor da primeira harmônica: ['median(freq-1,freq+1)', 'rms(freq-1,freq+1)']
- amplitude do pico na segunda harmônica: ['peak2x']
- rotação real do equipamento em Hz: ['real_rotation_hz']


Args:
 - features (dict[str, float]): Dicionário com nomes das features como chaves para os valores reais (float).
   - Chaves OBRIGATÓRIAS esperadas:
    - "a"
    - "b"
    - "real_rotation_hz"
    - "peak1x"
    - "peak2x"
    - "rms(freq-1,freq+1)"
    - "median(freq-1,freq+1)"
    - "median(3,5)"
 - ommitted_features (list[str]): Lista com os nomes das features que serão omitidas na análise. Por exemplo: ['a', 'b'], ao desconsiderar o comportamento da curva entre 5Hz e 19Hz ou ['median(freq-1,freq+1)', 'rms(freq-1,freq+1)'] ao desconsiderar o ruído ao redor da primeira harmônica.
