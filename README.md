# House-Rocket
![image](https://user-images.githubusercontent.com/94385953/148582727-3bca26ba-63e5-4869-9614-7273fe771316.png)
**AVISO:**  Os seguintes dados foram retirados do site:
<br> https://www.kaggle.com/harlfoxem/housesalesprediction. O CEO citado no tópico Problema de Negócio não existe, o contexto foi feito somente para fins ilustrativos. As hipóteses foram formuladas e desmistificadas por mim. 

# 1. Sobre a Empresa
A House Rocket é uma plataforma digital que tem como modelo de negócio a compra e venda utilizando tecnologia. Sua principal estratégia na compra de imóveis é mapear a região e saber quanto custo o (R$) a mediana de preço dessa localidade. Quanto maior a diferença entre a compra e a venda, maior é o lucro da empresa, e portanto mais receita. 
<br>
A House Rocket atua em algumas frentes na compra de imóveis um deles seria a compra de imóveis Regulares, Bons e Ruins. Quando necessário ela oferece manutenção nesses imóveis para conseguir prezar pelo maior rendimento em uma futura venda.

# 2. Questão de Negócio
A principal estratégia é comprar boas casas com preço abixo e revendê-las por um preço mais alto. Quanto maior a diferença entre compra e venda maior será a sua receita. 

# 3. Problema de Negócio
O CEO da empresa fez uma reunião e colocou alguns pontos que as casas fossem compradas. 
<br>

As cassa possuem muitos atributos que as tornam mais atrativas para compra um deles seria o período em que estamos, como a casa se encontra (sua situação), seu preço e sua localização.

<br>

**PERGUNTAS**
* 1- Quais casas o CEO da House Rocket deveria comprar e por qual preço de compra?

* 2- A House Rocket deveria fazer uma reforma para aumentar o preço da venda? Quais seriam as sugestões de mudanças? Qual o incremento no preço dado por cada opção de reforma?

* 3 - Qual seria o lucra das vendas seguindo a análise?


# 4. Planejamento da Solução

## 4.1 Primeira Análise 
Nossa primeira análise foi verificar do que se tratavam os dados que tínhamos em mãos. Fizemos uma tabela com informações de média, mediana, desvio padrão, máximo, mínimo, range... 
![image](https://user-images.githubusercontent.com/94385953/148584168-aa4e6b93-3ef4-4d02-8a97-7f352929d43b.png)
Já por meio dessa primeira análise podemos verifica que o empreendimento mais caro custou $ 7.700.000,00 e nosso empreendimento com menor custo foi de $ 75.000,00. Tendo em média aproximadamento o custo de $ 540.000,00 e como mediana o custo de $ 450.000,00. A mediana nessa análise se torna mais juta pelo simples fato de que os outliers dos preços dos empreendimentos podem influenciar muito nossa média. 

## 4.2 Cálculo da mediana por região.
Utilizamos comandas em python com a biblioteca "pandas" para conseguir organizar o que precisavamos para calcular o preço da mediana pelo ZIP CODE.
![image](https://user-images.githubusercontent.com/94385953/148584917-556f1aef-adf5-4fd5-a0a3-615d87516cb8.png)
Ao final tivemos uma nova tabela com uma coluna chamada de "price_median", como também uma nova coluna chamada "STATUS": caso o preço que a casa custa esteja acima do preço da mediana de mercado aparecerá a palavra **"não compra"**, porque o preço que iremos pagar seria mais alto e ficaremos no prejuízo. Caso o preço esteja abaixo da mediana de mercado a palavra que aparecerá será "**compra**". 


# 5. Desenvolvimento da Hipótese e Correlação

* **H1.** A maioria das casas com 3 quartos são acima da mediana do preço? 
<br> 
**FALSA** A maioria das casas estão abaixo da mediana de mercado. 

* **H2.** A maioria das casas com 3 quartos e 2 banheiros são acima da mediana do preço. 
<br>
**FALSA** Pelo o que conseguimos apurar algo que influência muito é a localização que se encontra esse empreendimento. 

* **H3.** Casas com com vista para água são 100% mais caras que a mediana do preço.
<br> **VERDADEIRO** Casas que tem a vista para o mar são 100% mais caras que a mediana do preço. Esse é um motivo clássico da procura e oferta, temos poucas casas disponíveis em frente ao mar. Quando há vendas essas custam o dobre do preço da compra. 
![image](https://user-images.githubusercontent.com/94385953/148585909-3c0783b3-6e3b-49b1-9353-e1400177cd61.png)
Visualizaação da quantidade sem vistas para o mar x vistas para o mar. 

* **H4.** A maioria das casas com porão e 2 andares são mais caras que que a mediana do preço.
<br> **VERDADEIRO** A maioria as casas com essas caractetrísticas são mais caras do que a mediana de mercado. 

* **H5.** A maioria das casas com datas acima de 1990 que tiveram reformas são mais caras que a mediana.
<br> **VERDADEIRO** Todas as casas com essas caractetrísticas são mais caras do que a mediana de mercado. 

* **H6.** A maioria das casas antigas são mais caras que a mediana de mercado. 
<br> **VERDADEIRO** A maioria das casas antigas forma vendidas mais caro do que a mediana de mercado. Porém essa diferença ficou com uma diferença de quase 100 casas vendidas mais cara do que a mediana de mercado. 

* **H7.** A maioria das casas novas são mais caras que a mediana de mercado¶
<br> **VERDADEIRO** A maioria das casas novas são mais caras que a mediana de mercado.


