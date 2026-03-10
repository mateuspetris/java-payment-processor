#  Moo Pay

> Sistema simples de processamento de transações financeiras desenvolvido para praticar conceitos de Programação Orientada a Objetos em Java.

![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)
![Status](https://img.shields.io/badge/Status-Em%20Desenvolvimento-yellow?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-blue?style=for-the-badge)
![POO](https://img.shields.io/badge/Conceito-POO-green?style=for-the-badge)

---

## 📋 Sobre o Projeto

O **Moo Pay** é um sistema de pagamentos que simula o processamento de transações via **PIX** e **Cartão de Crédito**. 

Este projeto foi criado como exercício prático para aplicar conceitos fundamentais de POO (Programação Orientada a Objetos) aprendidos durante estudos de Java.

---

## 🎯 Conceitos Aplicados

Durante o desenvolvimento deste projeto, pratiquei os seguintes conceitos:

- ✅ **Herança** - Classes filhas herdam de `Transacao`
- ✅ **Polimorfismo** - Diferentes tipos de pagamento com comportamentos distintos
- ✅ **Encapsulamento** - Atributos privados com getters/setters
- ✅ **Classes Abstratas** - `Transacao` como base abstrata
- ✅ **Enums** - `StatusTransacao` para controle de estados
- ✅ **Sobrecarga de Construtores** - Múltiplas formas de inicializar objetos
- ✅ **Override de Métodos** - Sobrescrita de `processarPagamento()` e `toString()`
- ✅ **Modificadores de Acesso** - `private`, `protected`, `public`

---

## 🏗️ Arquitetura do Sistema

```
Moo Pay
│
├── Transacao (abstract)
│   ├── id:  int
│   ├── valor:  double
│   ├── status: StatusTransacao
│   └── processarPagamento(): void (abstract)
│
├── PagamentoPix extends Transacao
│   ├── chave: String
│   └── processarPagamento(): void
│
├── PagamentoCartao extends Transacao
│   ├── numero: String
│   └── processarPagamento(): void
│
└── StatusTransacao (enum)
    ├── PENDENTE
    ├── APROVADO
    └── REJEITADO
```

---

## 🚀 Funcionalidades

- 💳 **Pagamento via Cartão de Crédito**
  - Processa pagamentos com validação de cartão
  - Exibe apenas os 4 últimos dígitos (segurança)
  
- 🔑 **Pagamento via PIX**
  - Processa pagamentos usando chave PIX
  - Validação de chave

- 📊 **Controle de Status**
  - Acompanhamento do status da transação (Pendente, Aprovado, Rejeitado)

- 🎭 **Polimorfismo em Ação**
  - Lista de transações que processa diferentes tipos de pagamento

---

## 💻 Como Usar

### Pré-requisitos

- Java JDK 8 ou superior
- IDE de sua preferência (IntelliJ IDEA, Eclipse, VS Code)

### Executando o Projeto

1. Clone o repositório:
```bash
git clone https://github.com/seu-usuario/moo-pay.git
```

2. Abra o projeto na sua IDE

3. Execute a classe `Main.java`

### Exemplo de Uso

```java
import mooPay.PagamentoCartao;
import mooPay.PagamentoPix;
import mooPay.StatusTransacao;

// Criando transações
PagamentoPix pix = new PagamentoPix(1, 150.00, StatusTransacao.PENDENTE, "chave@email.com");
PagamentoCartao cartao = new PagamentoCartao(2, 299.90, StatusTransacao.PENDENTE, "1234567812345678");

// Processando pagamentos
pix.

processarPagamento();
cartao.

processarPagamento();

// Exibindo informações
System.out.

println(pix);
System.out.

println(cartao);
```

**Saída esperada:**
```
Processando pix de R$ 150.0 na Chave: chave@email.com
Pagamento de R$ 299.9 no Cartão final 5678

PagamentoPix{id=1, valor=150.0, status=APROVADO, chave='chave@email.com'}
PagamentoCartao{id=2, valor=299.9, status=APROVADO, numero='****5678'}
```

---

## 📁 Estrutura de Arquivos

```
src/
└── Projetos/
    ├── Main.java
    ├── Transacao.java
    ├── PagamentoPix.java
    ├── PagamentoCartao.java
    └── StatusTransacao.java
```

---

## 🔮 Melhorias Futuras

Ideias para expandir o projeto:

- [ ] Adicionar mais formas de pagamento (Boleto, Transferência Bancária)
- [ ] Implementar validações mais robustas
- [ ] Adicionar tratamento de exceções
- [ ] Criar histórico de transações
- [ ] Implementar cálculo de taxas por tipo de pagamento
- [ ] Adicionar interface gráfica (GUI)
- [ ] Integrar com banco de dados
- [ ] Adicionar testes unitários

---

## 🧠 Aprendizados

Este projeto me ajudou a compreender melhor:

1. **Como usar herança de forma efetiva** - Entendi quando criar classes abstratas e como as filhas herdam comportamentos
2. **O poder do polimorfismo** - Ver o mesmo método se comportar diferente dependendo do objeto foi revelador
3. **Importância do encapsulamento** - Proteger dados sensíveis e controlar o acesso
4. **Enums para estados** - Muito melhor que usar Strings ou números mágicos
5. **Boas práticas** - Código limpo, nomenclatura clara, segurança de dados

---

## 👨‍💻 Autor

Desenvolvido por **[Mateus Petris]** durante estudos de Java e POO. 

📫 Entre em contato: 
- GitHub: [@mateuspetris](https://github.com/mateuspetris)
- LinkedIn: [Mateus Petris](https://linkedin.com/in/mateuspetris)

---

## 📝 Licença

Este projeto está sob a licença MIT.  Sinta-se livre para usar, modificar e aprender com ele!

---

## 🙏 Agradecimentos

- Curso Java10x do Fiasco - Base dos conceitos aplicados
- Comunidade Java - Pela documentação e recursos disponíveis

---

<div align="center">

### ⭐ Se este projeto te ajudou de alguma forma, considere dar uma estrela! 

**Feito com ☕ e muito aprendizado**

</div>
