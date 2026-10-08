# Sistema de Locação de Veículos

## Autor
- **Nome:** Seu Nome Completo  
- **Matrícula:** 123456  

---

## Arquitetura
O sistema é composto pelas seguintes classes:

- **Cliente**: representa quem realiza a locação.  
- **Veículo**: classe genérica que contém atributos comuns a todos os carros.  
- **CarroPopular, SUV, Sedan**: subclasses de Veículo que representam categorias específicas.  
- **Locação**: registra o contrato de aluguel, conectando Cliente e Veículo.  

**Fluxo principal:**  
Cliente → Locação → Veículo (Popular/SUV/Sedan)

---

## Instruções de Execução
1. Compile o projeto com:
   ```bash
   javac src/*.java
Cenário 1: Locação bem-sucedida
Entrada: Cliente "João", Veículo "Fiat Uno (Popular)", período de 01/10 a 05/10

Ação: Registrar a locação

Saída esperada: Locação criada com status "Ativa"

Cenário 2: Veículo indisponível
Entrada: Cliente "Maria", Veículo "Fiat Uno (Popular)" já alugado no mesmo período

Ação: Tentar registrar a locação

Saída esperada: Mensagem de erro "Veículo indisponível"

Cenário 3: Locação de SUV
Entrada: Cliente "Carlos", Veículo "Toyota Hilux (SUV)", período de 10/10 a 15/10

Ação: Registrar a locação

Saída esperada: Locação criada com status "Ativa" e diária calculada com preço de SUV

Cenário 4: Locação de Sedan
Entrada: Cliente "Ana", Veículo "Honda Civic (Sedan)", período de 20/10 a 25/10

Ação: Registrar a locação

Saída esperada: Locação criada com status "Ativa" e diária calculada com preço de Sedan

Código
