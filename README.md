# Etiqueta Digital
Projeto realizado para disciplina de técnicas de programação.

# Sumário

- O que é a Etiqueta Digital?
- Manual do usuário;
- Funcionamento;
- Ficha técnica.

# O que é a Etiqueta Digital?
Observando o funcionamento de um supermercado, percebemos que constantemente os funcionários precisam fazer a alteração do preço dos produtos nas prateleiras, pensando nisso, desenvolvemos uma etiqueta digital que tem como objetivo principal automatizar esta função.

A etiqueta consiste, basicamente, em uma ESP-12e (NODEMCU V3) que recebe os dados de uma central e os encaminha para um display LCD. Esses dados serão exibidos em cada prateleira, informando o nome do produto, o preço e o respectivo desconto.

![(Z:\20191610041\Downloads

Na imagem acima podemos observar o escopo do nosso produto.

#Manual do Usuário

## Funcionamento da etiqueta
A ideia do projeto é que funcionário do supermercado possa alterar o preço dos seus produtos sem a necessidade de perder tanto tempo e gastar com material. Para isso, será disponibilizada uma interface na qual haverá os campos a serem alterados para que o produto tenha seus dados de preço e desconto atualizados. Controlaremos também a necessidade de reposição do produto, através de um sensor infravermelho que detecta a ausência da mercadoria na prateleira e encaminha uma mensagem para a central.

![(

# Utilizando a etiqueta

![(

A tela inicial da aplicação do projeto é bastante direta. Primeiro, o usuário deve conectar o seu cabo microUSB da ESP-12e com alguma entrada USB do seu computador. A seguir, deve ser selecionada a porta na qual a placa está conectada. Para que as informações sejam transmitidas, faz-se necessário ter uma velocidade específica (em bauds) para comunicação, sendo definida a velocidade padrão de 115200 bauds. Em seguida, na aba "Etiqueta" preencha os seguintes dados:

- Nome do produto;
- Preço;
- Desconto geral;
- Desconto em atacado.

Por fim, basta clicar em "Atualizar" e o produto será exibido no display LCD com todos os dados atualizados

# Ficha técnica
## Materiais utilizados:
- NodeMCU ESP-12e;
- Display LCD;
- Sensor Infravermelho;
- Protoboard;
- Jumpers para conexão.

# O Circuito

![(

Utilizamos o sensor infravermelho para identificar a situação de estado da prateleira, conferindo se existe a necessidade de reposição do produto. A ESP-12e é a peça mais importante do circuito, pois recebe as informações vindas do aplicativo e as transfere para o LCD, assim como também capta dados do infravermelho e identifica a situação da prateleira.

// Nossa alternativa para realizar o funcionamento offline é plugar um cabo USB para o computador para que o usuário possa obter as informações via serial pelo software.//
 
 


