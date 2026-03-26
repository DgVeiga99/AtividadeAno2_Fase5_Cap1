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

O Front-end foi desenvolvido utilizando HTML, CSS e JavaScript, sendo responsável por toda a interação com o usuário. A interface simula um ambiente de chat, permitindo a entrada de mensagens e a visualização das respostas do assistente em tempo real.

Além da comunicação com o backend, essa camada implementa melhorias na experiência do usuário, como a simulação de digitação do assistente (delay), organização visual das mensagens e controle da sessão de conversa. O foco dessa camada é tornar a interação mais natural e intuitiva.

### 2. Back-end

O Back-end foi implementado em Python e atua como a camada intermediária entre a interface e o serviço de inteligência artificial. Sua principal função é gerenciar o fluxo de comunicação, recebendo as mensagens do usuário, estruturando as requisições e encaminhando-as ao Watson Assistant.

Essa camada também é responsável pelo tratamento das respostas recebidas, garantindo que o retorno ao usuário esteja formatado corretamente. Além disso, permite a futura implementação de regras de negócio, logs, persistência de dados e integrações com outros sistemas.

### 3. Watson (IBM Watson Assistant)

O Watson Assistant representa o núcleo cognitivo da aplicação, sendo responsável pelo processamento de linguagem natural. Ele interpreta as mensagens enviadas pelo usuário, identificando intenções, entidades e contexto da conversa.

Com base nessa análise, o Watson gera respostas coerentes e contextualizadas, seguindo fluxos de diálogo previamente definidos. Esse modelo se encaixa em sistemas conversacionais modernos, que utilizam NLU para entendimento da linguagem e podem evoluir para abordagens híbridas mais avançadas :contentReference[oaicite:1]{index=1}.

A utilização do Watson permite desacoplar a inteligência do sistema da lógica de aplicação, facilitando a evolução do assistente sem necessidade de alterações estruturais no software.

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
- flask (ou equivalente)  
- requests  

No frontend, foram utilizadas tecnologias nativas da web:

- HTML5  
- CSS3  
- JavaScript  

Essa escolha garante uma aplicação leve, modular e de fácil manutenção.

---

## ▶️ Como Executar

Para executar o projeto localmente, é necessário possuir o Python instalado na máquina.

Recomenda-se iniciar criando um ambiente virtual para isolamento das dependências. Após isso, deve-se instalar as bibliotecas necessárias utilizando o arquivo requirements.txt.

Com o ambiente configurado, o servidor Python deve ser iniciado, ativando a API responsável pelo processamento das requisições.

Por fim, basta colocar o software python em run mode para gerar o link da pagina do Flask, que por sua vez interage com o Watson, retornando respostas em tempo real ao usuário.

---

## 🎥 Demonstração do Projeto

Para uma visualização completa do funcionamento do sistema, acesse o vídeo demonstrativo no link abaixo:

👉 [Assista ao vídeo do projeto](https://youtu.be/hjQX7jjAl3I)

O vídeo apresenta a navegação pelo sistema, fluxo de interação com o assistente e validação das funcionalidades implementadas.

---

## 👨‍💻 Autor

Diego Veiga  
Tecnólogo em Inteligência Artificial – FIAP  
CEO – DKV Automação
