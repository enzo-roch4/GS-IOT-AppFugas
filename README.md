# GS-IOT-AppFugas

# Previsão de Inundações com IoT e Machine Learning

## Descrição do Projeto

Este projeto tem como objetivo criar uma solução para previsão de risco de inundações utilizando dados simulados de sensores IoT (nível de água), integrando Machine Learning para análise e previsão em tempo real. A ideia principal é desenvolver um modelo que, baseado em dados ambientais, possa alertar sobre riscos de desastres naturais, contribuindo para a segurança e evacuação em áreas de risco.

Este projeto está relacionado ao tema do app de rotas de fuga para casos de desastres naturais, onde a previsão de inundações é uma funcionalidade-chave para alertar usuários e indicar rotas seguras.

---

## Tecnologias Utilizadas

- Python 3.x
- Bibliotecas: scikit-learn, numpy, pandas, matplotlib, pyserial (para leitura serial com Arduino físico)
- Google Colab (para desenvolvimento e testes)
- Tinkercad (simulação de Arduino + sensor de nível via potenciômetro)

---

## Estrutura do Projeto

### 1. Simulação de Dados IoT

- Simulamos dados de nível de água para 200 dias, com variações normais e picos que representam situações de risco.
- A variável alvo é binária: `risco_inundacao` (0 = sem risco, 1 = risco).
- Visualização gráfica dos dados simulados.

### 2. Modelo de Machine Learning

- Utilizamos um classificador Random Forest para prever o risco de inundação baseado no nível de água.
- O modelo é treinado e avaliado com os dados simulados.
- Avaliação com matriz de confusão e relatório de classificação.

### 3. Simulação em Tempo Real

- Criamos um script Python para simular o envio contínuo de dados de sensores (nível de água variando aleatoriamente).
- O modelo realiza previsões em tempo real e imprime se há risco de inundação.

### 4. Simulação de Hardware com Tinkercad

- Montamos um circuito no Tinkercad com Arduino Uno e potenciômetro, simulando um sensor analógico de nível de água.
- Código Arduino para enviar o valor do potenciômetro pela porta serial a cada segundo.
- Possibilidade de ler esses dados em Python (com hardware real) e alimentar o modelo.

---

## Como Executar

### Rodar no Google Colab (Simulação Completa)

1. Crie um notebook no [Google Colab](https://colab.research.google.com).
2. Cole e execute o código que:
   - Simula os dados históricos.
   - Treina o modelo Random Forest.
   - Simula o envio em tempo real de dados do sensor.
   - Faz previsões de risco em tempo real.
   
### Simulação no Tinkercad

1. Acesse [Tinkercad Circuits](https://www.tinkercad.com/circuits).
2. Crie um circuito com Arduino Uno e potenciômetro conectado ao pino A0.
3. Use o código Arduino para enviar o valor do potenciômetro via serial.
4. Simule a variação do potenciômetro para alterar o "nível de água".

---

## Referências

- [Scikit-learn Documentation](https://scikit-learn.org/stable/)
- [Tinkercad Circuits](https://www.tinkercad.com/circuits)
- [Google Colab](https://colab.research.google.com/)
- [PySerial Documentation](https://pythonhosted.org/pyserial/)

---
# Autores

***Enzo Franco - RM: 553643
Herbert Santos de Sousa - RM: 553227
João Pedro Pereira - RM: 553698***


