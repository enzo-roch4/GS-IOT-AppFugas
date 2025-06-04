# GS-IOT-AppFugas

## Previsão de Inundações com IoT e Machine Learning

### Descrição do Projeto

Este projeto visa criar uma solução para previsão de risco de inundações utilizando dados simulados de sensores IoT (nível de água, temperatura e abalos sismicos), integrando **Machine Learning (ML)** para análise e previsão em tempo real. A ideia principal é desenvolver um modelo que, com base em dados ambientais coletados, possa alertar sobre riscos de desastres naturais, contribuindo para a segurança e evacuação em áreas de risco.

Este projeto está relacionado ao tema do app de rotas de fuga para casos de desastres naturais, onde a previsão de inundações, temperaturas altas e terremotos são funcionalidades-chave para alertar usuários e indicar rotas seguras.

---

## Tecnologias Utilizadas

- **Hardware**: ESP32 (simulado no Wokwi)
- **Software**: Python 3.x
- **Bibliotecas**: scikit-learn, numpy, pandas, matplotlib, pyserial
- **Plataformas**: Google Colab (para desenvolvimento e testes), Wokwi (simulação de ESP32 + sensores)
- **Comunicação**: ThingSpeak (para monitoramento em tempo real)

---

## Estrutura do Projeto

### 1. Sistema IoT com ESP32

- **Sensores**: Utilizamos três sensores simulados via **potenciômetros** para medir o **nível de água**, **temperatura** e **dados de terremoto**.
- **Envio para ThingSpeak**: O ESP32 coleta dados dos sensores e os envia periodicamente para o **ThingSpeak** para monitoramento.

### 2. Modelo de Machine Learning (ML) no Google Colab

- **Simulação e Análise**: O modelo de ML no **Google Colab** é treinado com dados simulados de nível de água e utiliza o classificador **Random Forest** para prever o risco de inundação.
- **Previsões em Tempo Real**: O modelo de ML pode receber novos dados simulados e prever em tempo real se há risco de inundação.

### 3. Conectividade em Tempo Real

Este projeto integra **sensores IoT (ESP32)** com o backend **Flask** rodando no Google Colab, onde a previsão de risco é realizada em tempo real:

1. **Sensores IoT**: O ESP32 lê os valores dos sensores e envia os dados para o backend Flask via **API REST**.
2. **Backend Flask**: O backend processa os dados, utiliza o modelo de **Machine Learning** para prever o risco de inundação e retorna a previsão.
3. **Visualização**: Os dados e alertas são enviados para o **ThingSpeak**, onde podem ser visualizados em tempo real.

### 4. Testes e Simulações

- **ESP32** é simulado no **Wokwi**, enviando dados para o backend que está em execução no **Google Colab**.
- [Wokwi - Simulação de ESP32](https://wokwi.com/projects/432769374785470465)
- **Backend Flask** é exposto via **ngrok** e processa as previsões de risco.

---

## Como Executar

### Rodar no Google Colab

1. Crie um notebook no [Google Colab](https://colab.research.google.com).
2. Cole e execute o código que:
   - Treina o modelo de ML (Random Forest).
   - Simula o envio de dados de sensores (nível de água, temperatura e terremoto).
   - Faz previsões de risco de inundação em tempo real.
   - Roda o backend Flask para receber dados via API REST.

---

## Referências

- [Scikit-learn Documentation](https://scikit-learn.org/stable/)
- [Google Colab](https://colab.research.google.com/)
- [ThingSpeak](https://thingspeak.com/)
- [Wokwi - Simulação de ESP32](https://wokwi.com/projects/432769374785470465)
- [Flask Documentation](https://flask.palletsprojects.com/)
  
---

## Autores

***Enzo Franco - RM: 553643  
Herbert Santos de Sousa - RM: 553227  
João Pedro Pereira - RM: 553698***
