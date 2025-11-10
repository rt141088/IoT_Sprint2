# 🛰️ Disruptive Architectures: IoT, IOB & Generative IA — Sprint 2

## 🎯 Objetivo da Sprint
Apresentar o **protótipo IoT funcionando**, desenvolvido no **Node-RED**, demonstrando a coleta, o processamento e a visualização de dados simulados de sensores conectados, representando a base de uma arquitetura inteligente em nuvem.

---

## 🧩 Descrição do Projeto
O projeto tem como objetivo criar um **fluxo IoT funcional** capaz de simular sensores que coletam dados em tempo real.  
Nesta sprint foi desenvolvido um **protótipo no Node-RED**, que realiza:

- Geração de dados simulados (exemplo: temperatura);  
- Processamento das informações via nó *Function*;  
- Visualização dos resultados no painel de *Debug*;  
- Preparação da estrutura para futura integração com o banco de dados Oracle APEX.  

---

## ⚙️ Componentes Utilizados

| Ferramenta | Descrição |
|-------------|------------|
| **Node-RED** | Ambiente de fluxo visual para Internet das Coisas (IoT). |
| **Function Node** | Responsável pelo processamento e formatação dos dados gerados. |
| **Inject Node** | Simula a leitura de um sensor físico. |
| **Debug Node** | Exibe os resultados no painel lateral para verificação. |

---

## 💡 Funcionamento do Fluxo
1. O nó **Inject** é acionado para simular a leitura de um sensor.  
2. O **Function** processa os dados, gerando um valor aleatório de temperatura.  
3. O resultado é exibido no **Debug**, representando o envio de dados para a nuvem.  

### 📜 Código no Function Node:
```javascript
msg.payload = {
    sensor: "SensorTemperatura",
    valor: Math.floor(Math.random() * 10) + 20,
    unidade: "°C",
    horario: new Date().toLocaleString()
};
return msg;
📈 Evoluções em relação à Sprint 1
Implementação do primeiro fluxo funcional em Node-RED;

Simulação de dados IoT dinâmicos;

Estruturação do pipeline de leitura, tratamento e exibição;

Preparação da integração com Oracle APEX e nuvem;

Documentação e vídeo explicativo do protótipo.

🚀 Próximos Passos (Sprint 3)
Enviar os dados gerados para o banco Oracle em nuvem;

Integrar dashboards e relatórios em APEX;

Aplicar algoritmos de Machine Learning para análise de dados;

Criar interface de monitoramento em tempo real.

🎥 Demonstração do Protótipo
O vídeo mostra o fluxo em funcionamento no Node-RED:

Apresentação dos nós configurados;

Deploy do fluxo;

Geração dos dados simulados;

Visualização das leituras no painel de debug.

📺 Link do vídeo: [adicione aqui o link do seu vídeo no YouTube ou no Canvas]

📂 Arquivos do Repositório
Arquivo	Descrição
fluxos_node_red.json	Contém o fluxo completo exportado do Node-RED.
README.md	Documentação do projeto (Sprint 2).
https://www.youtube.com/watch?v=jcJ-Qrw8uHE	Link direto do vídeo de demonstração.

👥 Integrantes do Grupo
Nome Completo	RM	Função
Rafael Terra Teodoro	560955	
Enzo Elia Tarraga	560901	
Otoniel Arantes Barbado	560112	
