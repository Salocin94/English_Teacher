# English_Teacher
Instrutor de inglês que corrige o usuário e continua uma conversa no nível selecionado.

PARA UTILIZAR, COPIE TODO O CÓDIGO E COLE NO SEU GOOGLE COLAB.

Prática de Conversação em Inglês com Ai Teacher

Este projeto oferece um ambiente interativo para praticar conversação em inglês em diferentes níveis do CEFR (Quadro Comum Europeu de Referência para Línguas), de A1 a C2. 
Ele utiliza o modelo Google Gemini para atuar como um professor de inglês AI, fornecendo respostas, correções e formas alternativas de expressão com base na sua entrada e no nível de proficiência selecionado.FuncionalidadesPrática em Vários Níveis: Escolha praticar nos níveis CEFR A1, A2, B1, B2, C1 ou C2.

Interaja com um agente AI adaptado ao nível de proficiência selecionado.Feedback em Tempo Real: Receba feedback imediato sobre suas frases, incluindo correções e explicações em português.Formas Alternativas: Obtenha maneiras alternativas de expressar suas ideias naturalmente em inglês, com traduções para o português.

Escalonamento de Nível: A AI pode detetar quando você está pronto para avançar para um nível CEFR superior e indicará isso durante a conversa (até C2).

Interface Interativa: Interface amigável construída com ipywidgets para selecionar o nível e enviar mensagens.

Requisitos: Google ColabAs seguintes bibliotecas Python:google-genaigoogle-adkipywidgets


Configuração
Configurar Chave da API do Google: O projeto requer uma Chave da API do Google para usar o modelo Gemini.Vá para o Google AI Studio ou Google Cloud Console para obter uma chave da API.No Google Colab, clique no ícone "Secrets" (🔑) na barra lateral esquerda. Adicione um novo segredo com o nome GOOGLE_API_KEY e cole a sua chave da API como valor.

Se estiver a executar localmente, será necessário definir a variável de ambiente GOOGLE_API_KEY antes de executar o notebook.

Como Executar

Abra o notebook Frontend.ipynb no Google ColabExecute todas as células do notebook sequencialmente.Como UsarApós executar as células, uma interface interativa irá aparecer.
Selecione o seu nível de proficiência em inglês desejado usando o menu pendente (A1 a C2).Clique no botão "Iniciar Sessão".
O professor AI irá cumprimentá-lo no nível selecionado.Escreva a sua mensagem em inglês na caixa de entrada e clique em "Enviar".
O professor AI irá responder, fornecer feedback (correção ou alternativa) e fazer uma nova pergunta para continuar a conversa.
Correções e alternativas aparecerão numa caixa colorida (verde para correto, laranja para precisar de revisão). 
Pode clicar em "Tradução" para ver a tradução para português da frase alternativa/corrigida.
Para terminar a sessão, escreva sair na caixa de entrada e prima Enter ou clique em "Enviar".

Níveis CEFR e Escalonamento
O projeto utiliza diferentes agentes AI, cada um especializado para um nível CEFR específico (A1, A2, B1, B2, C1, C2). Cada agente é instruído a:
Usar vocabulário e gramática apropriados para o seu nível.Corrigir erros comuns para esse nível.Gerar perguntas que incentivem a prática nesse nível.
Para os níveis A1 a C1, o agente monitoriza a conversa. Se as suas respostas indicarem prontidão para o nível seguinte (por exemplo, usando estruturas ou vocabulário mais complexos), o agente indicará isso e a sessão atual terminará, permitindo que inicie uma nova sessão no nível superior sugerido. O nível C2 é o mais alto e não inclui escalonamento.Estrutura do Projeto (Frontend.ipynb)

O notebook contém as seguintes partes principais:
Instalação de Bibliotecas e Configuração da Chave da API: Configura o ambiente e carrega a chave da API.
Importações: Importa as classes e bibliotecas necessárias (google.adk, google.generativeai, ipywidgets, etc.).
Variáveis Globais: Define variáveis para gerir o estado da sessão e os elementos da interface.
Widgets de Feedback: Configura os ipywidgets usados para exibir correções e alternativas.
Função on_translation_button_clicked: Lida com o evento de clique para o botão de tradução.
Função call_agent: Uma função auxiliar para enviar mensagens ao agente AI e obter a resposta bruta.
Função parse_agent_response: Analisa a resposta estruturada de quatro partes do agente AI.
Definições de Agentes (get_teacherA1_agent a get_teacherC2_agent): Funções que definem a instrução e o comportamento para cada agente de nível CEFR usando google.adk.agents.Agent.
Mapeamento de Níveis de Agente: Um dicionário que mapeia os níveis CEFR para as suas respetivas funções de criação de agente e gatilhos de escalonamento.
Função start_session_clicked: Lida com o evento de clique para o botão "Iniciar Sessão", inicializa a sessão e o agente apropriado.
Função send_message_clicked: Lida com o evento de clique para o botão "Enviar", envia a mensagem do utilizador, processa a resposta da AI, atualiza a interface e verifica o escalonamento de nível.
Configuração de Widgets da Interface: Define os ipywidgets para a seleção de nível, caixa de entrada, botão de envio e área de saída.
Layout e Exibição: Organiza os widgets e exibe a interface.Ligação de Eventos: Conecta os eventos de clique dos botões às suas respetivas funções.
Mensagem Inicial: Exibe uma mensagem de boas-vindas e verificação do estado da chave da API na área de saída.

Contribuições: Contribuições são bem-vindas! Se você quiser ajudar a melhorar este projeto, aqui estão algumas áreas onde a sua contribuição seria muito valiosa:
Melhorar a Interface: Aprimorar a experiência do usuário e o design da interface interativa.
Adicionar Sistema de Pontos: Implementar um sistema de gamificação para motivar os usuários.
Criar Jogos Interativos: Desenvolver pequenos jogos ou atividades baseadas em texto para tornar a prática mais divertida.
Adicionar Base de Dados de Vocabulário: Criar um sistema para rastrear e reforçar o vocabulário aprendido pelo usuário.
Refinar a Lógica dos Agentes: Melhorar as instruções e o comportamento dos agentes AI para fornecer feedback ainda mais preciso e útil.
Expandir Níveis ou Tópicos: Adicionar suporte para outros níveis de proficiência ou tópicos de conversação específicos.
