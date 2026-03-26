# 🫀 Assistente Cardiológico Inteligente - CardioIA

## 📌 Sobre o Projeto

O CardioIA é um Assistente Cardiológico Inteligente desenvolvido com o objetivo de simular interações clínicas por meio de linguagem natural, promovendo uma experiência mais acessível, organizada e contextualizada ao usuário.

A solução foi construída integrando conceitos de Inteligência Artificial, sistemas conversacionais e engenharia de software, permitindo que dados clínicos sejam interpretados e transformados em respostas compreensíveis. Diferente de um chatbot convencional, o sistema busca estruturar o fluxo de interação, interpretando intenções e mantendo coerência contextual ao longo da conversa.

Esse modelo de aplicação está alinhado com a proposta da Fase 5, onde sistemas inteligentes deixam de apenas responder perguntas e passam a apoiar decisões e organizar informações de forma estruturada :contentReference[oaicite:0]{index=0}.

---

## 🎯 Objetivo Principal

O principal objetivo do projeto é desenvolver um assistente virtual capaz de interpretar linguagem natural e fornecer respostas contextualizadas na área cardiológica, simulando um atendimento inicial ao paciente.

A proposta envolve não apenas a construção da interface conversacional, mas também a integração entre backend, serviços de IA e estrutura de dados, garantindo consistência, rastreabilidade e qualidade das informações geradas.

---

## 🏗️ Arquitetura do Software

A arquitetura do CardioIA foi projetada seguindo o princípio de separação de responsabilidades, garantindo modularidade, escalabilidade e facilidade de manutenção. O sistema está estruturado em três camadas principais: Front-end, Back-end e Watson (motor de IA).

### 1. Front-end

O front-end é responsável pela experiência do usuário e está concentrado no arquivo [`index.html`](./index.html). Nessa camada foram implementados o layout visual do chat, a área de entrada de mensagens, a renderização das respostas, o botão de reinício da conversa e os efeitos de humanização da interface, como a animação de digitação do assistente. Em termos funcionais, esse arquivo cuida da interação direta com o usuário e realiza as chamadas HTTP para o backend, servindo como ponto de entrada visual da aplicação.

### 2. Back-end

O back-end está implementado no arquivo [`main.py`](./main.py). Essa camada atua como intermediária entre a interface web e o Watson Assistant, sendo responsável por criar e encerrar sessões, receber as mensagens enviadas pelo usuário, encaminhá-las ao serviço cognitivo, tratar a resposta retornada e devolver o conteúdo formatado para o front-end. Também é no backend que ficam concentradas as rotas principais da aplicação, como carregamento inicial da interface, obtenção da mensagem de boas-vindas, envio de mensagens e reinicialização da sessão.

### 3. Watson (IBM Watson Assistant)

A camada cognitiva da aplicação está representada no arquivo [`Assistente-Cardio-dialog.json`](./Assistente-Cardio-dialog.json), que contém a estrutura conversacional do assistente no IBM Watson Assistant. Nesse arquivo estão definidas as intenções, entidades, exemplos de treinamento e nós de diálogo que permitem ao sistema reconhecer sintomas leves, sintomas graves, dúvidas sobre exames, preparo pré-exame e respostas afirmativas ou negativas. Essa camada é responsável pela interpretação semântica da mensagem e pela definição da resposta conversacional, funcionando como o núcleo de inteligência do projeto.

---

## 📊 Resultados

O sistema desenvolvido foi capaz de simular interações conversacionais de forma consistente, interpretando entradas do usuário e retornando respostas contextualizadas.

Foi possível validar a comunicação entre frontend, backend e o serviço de IA, garantindo fluxo contínuo de dados e respostas. Além disso, a implementação de mecanismos de humanização, como delay nas respostas, contribuiu significativamente para melhorar a experiência do usuário.

Do ponto de vista arquitetural, o projeto demonstrou a viabilidade de integrar serviços cognitivos em aplicações reais, reforçando que a qualidade da solução não depende apenas do modelo de IA, mas também da estrutura de dados, governança e organização do sistema como um todo :contentReference[oaicite:2]{index=2}.

---

## ⚙️ Tecnologias Utilizadas (Bibliotecas)

O backend da aplicação foi desenvolvido em Python, utilizando bibliotecas específicas para integração com serviços de IA e comunicação HTTP.

Principais bibliotecas:

- ibm-watson  
- ibm-cloud-sdk-core  
- flask
- requests  

No frontend, foram utilizadas tecnologias nativas da web:

- HTML5  
- CSS3  
- JavaScript  

Essa escolha garante uma aplicação leve, modular e de fácil manutenção.

---

## ▶️ Como Executar

Para executar o projeto localmente, é necessário ter o Python instalado na máquina. Recomenda-se criar um ambiente virtual para isolar as dependências da aplicação. Em seguida, deve-se instalar as bibliotecas listadas no arquivo [`requirements.txt`](./requirements.txt) com o comando abaixo:

```bash
pip install -r requirements.txt
```

Após a instalação, é necessário garantir que as credenciais do IBM Watson Assistant estejam corretamente configuradas no arquivo [`main.py`](./main.py), incluindo API key, URL do serviço, Assistant ID e versão utilizada.

Com isso configurado, basta iniciar a aplicação com:

```bash
python main.py
```

Depois da execução do servidor, a interface poderá ser acessada no navegador pelo endereço local informado pelo Flask. A partir desse ponto, o arquivo [`index.html`](./index.html) será carregado, as mensagens serão enviadas ao backend e o backend fará a comunicação com a estrutura conversacional definida em [`Assistente-Cardio-dialog.json`](./Assistente-Cardio-dialog.json).

---

## 🎥 Demonstração do Projeto

Para uma visualização completa do funcionamento do sistema, acesse o vídeo demonstrativo no link abaixo:

👉 [Assista ao vídeo do projeto](https://youtu.be/hjQX7jjAl3I)

O vídeo apresenta a navegação pelo sistema, fluxo de interação com o assistente e validação das funcionalidades implementadas.

---

## ⚠️ Aviso Importante

Este projeto possui finalidade **exclusivamente educacional** e **não deve ser utilizado para diagnóstico clínico**.  
Os resultados simulam um ambiente de pesquisa e não substituem avaliação profissional em saúde.
