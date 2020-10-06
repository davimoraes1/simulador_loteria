# Simulador de Loteria

Este projeto é um simulador da *megasena*, onde o usuário informa seis números, sorteamos aleatoriamente outros seis números e comparamos para verificar quantos números você acertou.

**Não é para jogos oficiais.**

## Tecnologia utilizadas

1. **HTML:** HTML é uma linguagem de marcação utilizada na construção da estrutura de páginas na Web.
2. **CSS:** Cascading Style Sheets (CSS) é um mecanismo para adicionar estilo (cores, fontes, espaçamento, etc.) a um documento web.
3. **JS:** JavaScript (frequentemente abreviado como JS) é uma linguagem de programação interpretada estruturada, de script em alto nível com tipagem dinâmica fraca e multiparadigma (protótipos, orientado a objeto, imperativo e, funcional).
4. ~~**Jquery**~~: não foi utilizado.

## Funções principais
Aqui serão apresentadas as duas funções principais do site.

### Sorteio de números
Nessa função os números são sorteados aleatoriamente.
```
function sortearNumeros() {
  numSort = [];
  let sort;
  for (var i = 0; i < 6; i++) {
    do{
      sort = Math.ceil(Math.random() * 60);
      sort = (sort == 0) ? 1 : sort;
    }while (numSort.includes(sort));

    numSort.push(sort);
  }
}
```

### Lendo os números digitados
Lê as entradas de números digitados pelo usuário.
```
function addToList(num, pos) {
  if(num.length == 2){
    if(numEsco.includes(num)){
      alert("Número escolhido anteriormente. Digite outro número.")
    } else if (parseInt(num) > 60){
      alert("O número digitado não pode ser maior que 60.")
    } else {
      numEsco[pos-1] = num;
    }
  }
}
```

## Como rodar o código
> Simplesmente baixe o código e abra o arquivo **_index.html_** no seu navegador.

## Exemplos de tabela
Exemplo   | Valor do exemplo | Quantidade
----------|------------------|-----------
Exemplo 1 | R$ 10            | 5
Exemplo 2 | R$ 8             | 4
Exemplo 3 | R$ 7             | 34
Exemplo 4 | R$ 8             | 23

## Imagens da tela
tela 1: tela de abertura.
![tela 1](/imagens/tela1.png)
tela 2: 6 números digitados, nenhum sorteado.
![tela2](/imagens/tela2.png)
#### Referências
* HTML: [wikipedia](https://pt.wikipedia.org/wiki/HTML)
* CSS: [w3Schools](https://www.w3schools.com/css/)
* JavasScript [wikipedia](https://pt.wikipedia.org/wiki/JavasScript)
