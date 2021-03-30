# Calculadora de Cartão Ponto

- Calculadora que recebe os horários trabalhados do funcionário e exibe um total.
<br>
<br>
<img src="https://user-images.githubusercontent.com/50367720/113009480-5d13fe00-914e-11eb-829f-f35d8aa09bf1.png"/>
<br>
<br>
<br>
# Funcionalidades:
<br>
<br>
<br>
1- Permite a seleção de faltas individuais para cada período:
<br>
<br>
<img src="https://user-images.githubusercontent.com/50367720/113009828-b2500f80-914e-11eb-9637-a94ba4679a4a.png"/>
<br>
<br>
<br>
2- Calcula e exibe individualmente cada período e o Tempo Extra.
<br>
<br>
2.1- Na imagem abaixo mostra o calculo nos períodos e no Tempo Extra que subtrai sempre o valor da saída pelo valor de entrada:<br>
<br>
<br>
<img src="https://user-images.githubusercontent.com/50367720/113015975-6a33eb80-9154-11eb-9aba-e5b1dbe1c7a3.png"/>
<br>
<br>
<br>
3- A coluna "Total trabalhado" faz o cálculo somando os dois períodos e o Tempo Extra:
<br>
<br>
<img src="https://user-images.githubusercontent.com/50367720/113019080-99982780-9157-11eb-9ecf-8c27f39bf2f9.png"/>
<br>
<br>
<br>
4- A coluna "Total c/ tolerância" faz alguns cálculos condicionais, ou seja:
<br>
<br>
4.1- Ela verifica SE a soma dos períodos e do Tempo Extra é maior OU menor que o intervalo de "TOLERÂNCIA". A "TOLERÂNCIA" é definida somando ou subtraindo com as "Hoas diárias a cumprir", isso define um intervalo.<br>
4.1.1- Caso o resultado seja maior ou menor que a "TOLERÂNCIA" será exibido a soma dos períodos e do Tempo Extra.<br>
4.1.2- Caso o resultado esteja dentro do intervalo de "TOLERÂNCIA" será exibido as "Horas diárias a cumprir".<br>
<br>
<br>
- A imagem abaixo mostra a fórmula identada: <br>
<img src="https://user-images.githubusercontent.com/50367720/113031651-58a70f80-9165-11eb-8ac5-d5bcab0f8ed8.png"/>
<br>
<br>
- A imagem abaixo mostra a fórmula na planilha:<br>
<img src="https://user-images.githubusercontent.com/50367720/113032232-ff8bab80-9165-11eb-9407-bfdb51cd7e07.png"/>
<br>
<br>
<br>
5- Na coluna "Excedente" temos o cálculo condicional principal, ou seja:
<br>
<br>
5.1- Ela verifica primeiramente SE em ambos os períodos esta marcado a opção "Faltou".<br>
5.1.1- Caso ambos estejam marcados será exibido as "Horas diárias a cumprir" negativa, simbolizando que a pessoa faltou.<br>
5.1.2- Caso a pessoa não faltou então verifica SE a opção "Faltou de manhã?" está marcada E a opção "Faltou a tarde?" está desmarcada.<br>
5.1.2.1- Caso corresponda é exibido o resultado da subtração do "Período da Tarde" pelas "Horas diárias a cumprir", simbolizando que a pessoa faltou apenas no período da manhã.<br>
5.1.2.2- Caso a pessoa não tenha faltado no período da manhã, então verifica SE a opção "Faltou a tarde?" está marcada E a opção "Faltou de manhã?" está desmarcada.<br>
5.1.2.2.1- Caso corresponda é exibido o resultado da subtração do "Período da Manhã" pelas "Horas diárias a cumprir", simbolizando que a pessoa faltou apenas no período da tarde.<br>
5.1.2.2.2- Caso a pessoa não faltou no período da tarde também, então quer dizer que ela trabalhou o dia todo. Então agora verifica SE o "Total c/ tolerância" é MAIOR que 0.<br>
5.1.2.2.2.1- Caso corresponda então verifica SE a subtração do "Total c/ tolerância" pelas "Horas diárias a cumprir" é MAIOR que 0.<br>
5.1.2.2.2.1.1- Caso corresponda é exibido a subtração do "Total c/ tolerância" pelas "Horas diárias a cumprir", exibindo então um excedente positivo.<br>
5.1.2.2.2.1.2- Caso contrário então verifica SE o botão do campo "Trabalha de Sábado?" está marcado.<br>
5.1.2.2.2.1.2.1- Caso esteja marcado é exibido a subtração do "Período da Manhã" por "4:00", simbolizando que a pessoa trabalhou no sábado e assim desconsidera o período da tarde.<br>
5.1.2.2.2.1.2.2- Caso a pessoa não trabalhe de sábado então verifica SE o botão do campo "Está sob aviso?" está marcado.<br>
5.1.2.2.2.1.2.2.1- Caso esteja marcado é exibido a soma de "2:00" com o resultado da subtração do "Total c/ tolerância" pelas "Horas diárias a cumprir", simbolizando que a pessoa está sob o aviso de 2 horas a menos na carga horária.<br>
5.1.2.2.2.1.2.2.2- Caso a pessoa não esteja sob aviso, então é exibido a subtração do "Total c/ tolerância" pelas "Horas diárias a cumprir", exibindo então um excedente negativo.<br>
5.1.2.2.2.2- Caso contrário é exibido o valor 0.<br>





