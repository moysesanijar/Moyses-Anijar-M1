# Instruções

- Faça uma cópia deste arquivo .md para um repositório próprio
- Resolva as 6 questões objetivas assinalando a alternativa correta
- Resolva as 4 questões dissertativas escrevendo no próprio arquivo .md
  - lembre-se de utilizar as estruturas de código como ``esta aqui com ` `` ou
```javascript
//esta aqui com ```
let a = "olá"
let b = 10
print(a)
```
- Resolva as questões com uso do Visual Studio Code ou ambiente similar.
- Teste seus códigos antes de trazer a resposta para cá.
- Cuidado com ChatGPT e afins: entregar algo só para ganhar nota não faz você aprender e ficar mais inteligente. Não seja dependente da máquina!
- ao final, publique seu arquivo lista_01.md com as respostas em seu repositório, e envie o link pela Adalove. 

# Questões objetivas

**1)** O que o código a seguir faz?

![Uma imagem](assets/ex01.PNG)

Escolha a opção que responde corretamente:

c) Imprime os números pares de 2 a 10.

______

**2)** Identificar a linha que falta no código para criar uma classe Veiculo com atributo marca, e uma classe Carro que herda de Veiculo com um método ligar(). 

![Uma imagem](assets/ex02.PNG)

No lugar onde está escrito “// linha” qual das opções abaixo deve estar para funcionar corretamente o código?

A) let carro = new Carro("Toyota");

______

**3)** Qual é o valor de resultado após a execução deste código?

![Uma imagem](assets/ex03.PNG)

Escolha a opção que responde corretamente:

A) 18

______

**4)** Como você criaria um método `acelerar()` em uma classe `Carro`, que recebe um parâmetro `velocidade` e o adiciona a um atributo `velocidadeAtual`?


C) ![Uma imagem](assets/ex04_3.PNG)

______

**5)** Qual a forma correta de definir uma classe Carro em JavaScript, com um método ligar() e um atributo marca?

A) ![Uma imagem](assets/ex05_1.PNG)

______

**6)** Observe o código abaixo:

![Uma imagem](assets/ex06.PNG)

Qual será a saída do código acima?

A) "Olá, meu nome é João. Olá, meu nome é Maria."

______

# Questões dissertativas

**7)** 
class Animal {
  constructor(nome, idade) {
    this.nome = nome;
    this.idade = idade;
  }

  descrever() {
    console.log(`${this.nome} tem ${this.idade} anos.`);
  }
}

let cachorro = new Animal("Cachorro", 5);
let gato = new Animal("Gato", 3);

cachorro.descrever();
gato.descrever();

______

**8)** 
class Gato extends Animal {
  constructor(nome, idade, cor) {
    super(nome, idade);
    this.cor = cor;
  }

  miar() {
    console.log("Miau!");
  }
}

let gato = new Gato("Gato", 3, "preto");

gato.descrever();
gato.miar();



______

**9)** 
class SomadorDeNotas {
  constructor() {
    this.total = 0;
  }

  adicionarNota(nota) {
    this.total += nota;
  }

  verTotal() {
    console.log(`Total das notas: ${this.total}`);
  }
}

let somador = new SomadorDeNotas();

somador.adicionarNota(10);
somador.adicionarNota(8);
somador.adicionarNota(9.5);

somador.verTotal();



______

**10)** 
class Funcionario {
  constructor(nome, idade, salarioBase) {
    this.nome = nome;
    this.idade = idade;
    this.salarioBase = salarioBase;
  }

  calcularSalario() {
    throw new Error("Método abstrato 'calcularSalario' não implementado!");
  }
}

class Professor extends Funcionario {
  constructor(nome, idade, salarioBase, disciplina, horasAula) {
    super(nome, idade, salarioBase);
    this.disciplina = disciplina;
    this.horasAula = horasAula;
  }

  calcularSalario() {
    const valorHoraAula = 50;
    return this.horasAula * valorHoraAula + this.salarioBase;
  }
}

const professor1 = new Professor("Ana", 35, 2000, "Matemática", 20);
const professor2 = new Professor("João", 40, 2500, "Física", 30);

console.log(`Salário Professor(a) ${professor1.nome}: R$${professor1.calcularSalario()}`);
console.log(`Salário Professor(a) ${professor2.nome}: R$${professor2.calcularSalario()}`);


