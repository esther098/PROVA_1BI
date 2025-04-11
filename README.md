# PROVA_1BI

//ALTERNATIVAS de assinalar 2:E  4:C 5: C

//1QUESTÃO
function convert(metro){// o nome da função é convert, metro é a palavra reservada para o parametro
  let cent=metro*100 //declaração de variável a partir do parâmetro, só funciona dentro da função.
  let mili=metro*1000
  return  metro +' metros é igual á ' +cent+ ' centímetros e ' + mili +' milímetros' //retorno da função
}
console.log(convert(1))//para exibir o retorno no pc e indicar o parâmetro

//3 QUESTÃO
// 1. Crie uma função chamada registrarPedido que receba cliente, prato, mesa e idade
function registrarPedido(cliente, prato, mesa, idade) {
  return {
    cliente: cliente,
    prato: prato,
    mesa: mesa,
    idade: idade
  };
}

// 2. Crie um array vazio chamado pedidos
let pedidos = [];

// 3. Adicione 3 pedidos ao array usando a função criada
pedidos.push(registrarPedido("Ana", "Hambúrguer", 1, 10));
pedidos.push(registrarPedido("Bruno", "Lasanha", 2, 17));
pedidos.push(registrarPedido("Carlos", "Feijoada", 3, 65));

// 4. Crie uma função chamada classificarIngresso que retorna o tipo com base na idade
function classificarIngresso(idade) {
  if (idade < 12) {
    return "Infantil";
  } else if (idade >= 12 && idade <= 17) {
    return "adolescente";
  } else if (idade >= 18 && idade <= 59) {
    return "Adulto";
  } else {
    return "Sênior";
  }
}

// 5. Atendimento dos pedidos (sem laço de repetição)

// Atendimento do primeiro pedido
let pedido1 = pedidos.shift();
let tipo1 = classificarIngresso(pedido1.idade);
let valor1 = 29.9;
console.log("Cliente atendido:", pedido1.cliente);
console.log("Tipo de ingresso:", tipo1);
console.log("Valor da conta: R$", valor1.toFixed(2));
console.log("atendido");

// Atendimento do segundo pedido
let pedido2 = pedidos.shift();
let tipo2 = classificarIngresso(pedido2.idade);
let valor2 = 38.9;
console.log("Cliente atendido:", pedido2.cliente);
console.log("Tipo de ingresso:", tipo2);
console.log("Valor da conta: R$", valor2.toFixed(2));
console.log("atendido");

// Atendimento do terceiro pedido
let pedido3 = pedidos.shift();
let tipo3 = classificarIngresso(pedido3.idade);
let valor3 = 29.9;
console.log("Cliente atendido:", pedido3.cliente);
console.log("Tipo de ingresso:", tipo3);
console.log("Valor da conta: R$", valor3.toFixed(2));
console.log("atendido");

// 6. Exiba a quantidade de pedidos restantes
console.log("Pedidos restantes:", pedidos.length);
