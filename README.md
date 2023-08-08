# Classificação - Taxa de Satisfação de Clientes

## Data Science Project - Taxa de Satisfação de Clientes

<div align='center'>

![Loja_01](https://github.com/caiomichelan/classification-customer_satisfaction_rate/assets/104601836/ff284138-c63d-4add-859a-34c51d9a7580)

</div>

# 1. Problema do Negócio
<p align='justify'>Uma rede de Lojas de Roupas (empresa fictícia) está passando por problemas de Customer Experience (Avaliação da Experência do Cliente).</p>
<p align='justify'>Foi observado pela equipe de negócios que o grande desafio em escalar o faturamento das lojas consiste em manter a qualidade do produto e atendimento ao cliente, com sua Taxa de Satisfação em alta.</p>
<p align='justify'>Com base no aumento de clientes ocasionado pelo crescimento da rede, os processos internos partindo desde a concepção dos produtos, passando pela divulgação do marketing, sistemas de pagamento e adequação do atendimento aos clientes começaram a apresentar problemas.</p>
<p align='justify'>Enquanto a equipe de produtos encontra dificuldade em determinar a necessidade da maioria dos clientes, a equipe de marketing esbarra em desafios para determinação da abordagem ideal aos mesmos e a equipe de desenvolvimento encontra problemas como instabilidades nos sistemas de pagamento e vendas online devido ao grande volume de acessos simultâneos, o que gera reclamações sobre o atendimento, gerenciado pela equipe de Customer Experience. Neste contexto, a medição da Taxa de Satisfação dos Clientes é muito importante para que a empresa mantenha sua boa reputação no mercado.</p>
<p align='justify'>Desta forma, foi designado à Equipe de Dados o desafio de, com base nos dados de clientes (gênero, tipo de compra, avaliações de serviços das lojas, dentre outros) cadastrados no sistema, seja desenvolvido um Modelo de Machine Learning capaz de identificar quais clientes têm propensão de avaliar as lojas da rede com “Satisfeito” ou “Neutro/Insatisfeito”, de modo que a equipe Customer Experience consiga definir ações de melhoria e entender prontamente se o cliente estaria propenso a fazer uma avaliação negativa, podendo implementar ações de maneira rápida e efetiva para reverter esta avaliação, trazendo uma melhora significativa neste indicador.</p>

# 2. Premissas do Negócio
<p align='justify'>Foram desconsiderados fatores externos como economia e segmento do negócio.</p>

# 3. Estratégia da Solução
<p align='justify'>O modelo foi desenvolvido com utilização dos seguintes Algoritmos de Classificação: XGBoost, Gradient Boosting, Random Forest e LightGBM.</p>
<p align='justify'>Foi implementada a técnica de Hyperparameter Fine Tuning, de modo a otimizar os hiperparâmetros dos modelos, trazendo uma melhora significativa em seus desempenhos, como também realizado o Cross Validation visando garantir a qualidade da predição do modelo.</p>
<p align='justify'>Após implementação dos algoritmos, foi realizado um comparativo entre os modelos com a geração da moda e posterior avaliação do melhor valor a ser considerado na projeção.</p>

# 4. Insights de Dados
<p align='justify'>Inicialmente foi identificado que a Taxa de Satisfação dos Clientes está abaixo do ideal, sendo que 57% estão Neutros/Insatisfeitos, enquanto 43% permanecem Satisfeitos com as lojas da rede.</p>
<p align='justify'>O Índice de Consumidores Leais (os quais possuem um compromisso sólido com lojas da rede) consta em 82%, contra os 18% de consumidores que não garantem consumir apenas nas lojas da rede.</p>
<p align='justify'>Foi observado que 69% optam pela compra de presentes a terceiros, enquanto 31% seguem realizando compras a si mesmos.</p>
<p align='justify'>Sobre o tamanho das lojas da rede, podemos identificar que 48% são lojas grandes, 45% de tamanho médio e 7% pequenas, constatando que a rede possui grandes lojas, em sua maioria.</p>
<p align='justify'>Dos itens avaliados pelos clientes, foi constatado que a maioria possui nota 4 em uma escala de 0 a 5.</p>

# 5. Produto Final
<p align='justify'>Com base nos dados de características dos clientes, foi desenvolvido um modelo de previsão do seu nível de satisfação, o qual visa prever a variável alvo "Satisfaction", retornando 1 em caso de Cliente Satisfeito, e 0 em caso de Cliente Neutro/Insatisfeito.</p>

# 6. Conclusão
<p align='justify'>O objetivo do projeto foi desenvolver um modelo de previsão do nível de satisfação dos clientes da rede de lojas que visa entender rapidamente se o mesmo possui propensão em avaliar a loja de maneira negativa, permitindo à equipe responsável implementar ações para tentar reverter esse quadro.</p>
<p align='justify'>Com base nos resultados, a equipe de Customer Experience pode identificar me maneira instantânea se o cliente tem propensão a avaliar negativamente e entender junto ao mesmo o que poderia ser feito para que esse quadro fosse revertido, buscando proporcionar maior satisfação aos seus clientes, contribuindo para a retenção dos mesmos.</p>
<p align='justify'>Com a implementação do modelo foi possível prever a taxa de avaliação dos clientes com uma precisão de 96%, ou seja, dentre 100 avaliações de clientes, é viável que 96 avaliações sejam previstas com exatidão.</p>
<p align='justify'>Traduzindo em valores, tendo como premissa que o preço médio do LTV (Lifetime Value, estimativa média de quanto um cliente irá gerar valor à empresa ao longo de sua vida) seja $ 15.000 (Considerado 30 anos x $ 500 ao ano) e a rede de lojas atende aproximadamente 10.000 clientes ao mês, a previsão da satisfação de cada cliente com 96% de precisão implicaria à rede de lojas uma garantia de aproximadamente $ 82 milhões em receita com a retenção destes 57% de clientes que a avaliaram negativamente.</p>
<p align='justify'>Observação: Para este cálculo foi considerado: 96% (Precisão do Modelo) x (5.700 (Quantidade de Clientes Neutros/Insatisfeitos) x $ 15.000 (LTV do Cliente)).</p>
<p align='justify'>Considerando ainda o custo de retenção de cada cliente como sendo $ 100 e sob a premissa de 57% dos clientes estarem insatisfeitos, pode-se observar que os 5.700 clientes demandariam da empresa um custo de $ 570.000.</p>
<p align='justify'>Tendo como base $ 82.000.000 de receita com a retenção dos clientes, debitando os custos de $ 570.000, foi observado uma receita de $ 81,5 milhões provenientes destes clientes. Apenas estes, considerando uma expectativa de vida de mais 30 anos, valor considerado no LTV, contribuirão com uma receita anual de $ 2,7 milhões. </p>
<p align='justify'>Finalizando, todos estes cálculos foram feitos sem considerar a receita proveniente da aquisição de novos clientes.</p>

# 7. Próximos Passos
<p align='justify'>Como próximos passos serão definidos estudos detalhados sobre as características dos clientes de modo isolado, permitindo que as equipes de Marketing, Comercial e Customer Experience possam focar em cada tipo de público considerando suas particularidades, permitindo a definição de uma estratégia mais assertiva na publicidade, vendas, retenção e satisfação dos clientes.</p>
