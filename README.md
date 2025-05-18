 TeachAi
Bem-vindo ao projeto que transforma o aprendizado de inglês em uma aventura personalizada! Este não é apenas mais um aplicativo de idiomas; é o seu tutor pessoal de IA, pronto para guiá-lo desde os primeiros passos até a fluidez total, adaptando-se ao seu ritmo e nível.

Imagine ter um professor dedicado que entende suas necessidades, corrige seus erros com explicações claras e o desafia suavemente à medida que você melhora. É exatamente isso que construímos aqui, usando o poder do Google ADK e da API Gemini.

A História por Trás do Projeto
Tudo começou com a ideia de tornar o aprendizado de idiomas mais interativo e menos intimidante. Muitos de nós lutamos com a consistência ou encontramos materiais que não se encaixam perfeitamente em nosso nível. E se pudéssemos criar um ambiente onde a prática de conversação fosse natural, adaptável e sempre disponível?

Com a ascensão dos modelos de linguagem avançados, vimos a oportunidade de criar agentes de conversação que não apenas respondem, mas ensinam, corrigem e motivam. Assim nasceu o conceito de um sistema de tutoria multinível, onde você progride por diferentes estágios de proficiência, como em uma jornada épica de aprendizado.

Sua Jornada Começa: Nível A1 - Os Primeiros Passos
Ao iniciar sua sessão, você será recebido pelo nosso Agente A1. Ele é gentil, paciente e focado no básico. Você aprenderá a se apresentar, falar sobre coisas simples e construir suas primeiras frases em inglês.

Nosso tutor A1 está atento aos erros comuns de iniciantes (como a ordem das palavras e verbos básicos) e os corrige com explicações em português, oferecendo alternativas para ajudar a fixar o aprendizado. A cada interação, ele o encoraja e faz uma pergunta simples para manter a conversa fluindo.


![image](https://github.com/user-attachments/assets/f314db00-ff0b-4acc-8f48-67a0d34421f6)

![image](https://github.com/user-attachments/assets/4d5ff549-0649-4548-83f2-184c3f11b9bf)

![image](https://github.com/user-attachments/assets/f37c34e3-94d0-4c52-8269-5c5496ccfbfd)


Construindo Fluidez: Níveis A2 a B2 - Explorando Novos Horizontes
À medida que você ganha confiança e seu vocabulário cresce, o sistema percebe sua evolução. Quando você estiver pronto, será suavemente escalado para o próximo nível.

A2: Comece a construir frases mais complexas, falar sobre rotinas e experiências passadas. O Agente A2 introduz novos tempos verbais e estruturas, sempre corrigindo e incentivando.

B1: Você já consegue lidar com situações de viagem e conversar sobre tópicos de interesse pessoal. O Agente B1 foca em refinar suas frases, expandir seu vocabulário e usar tempos verbais de forma mais precisa.

B2: A fluidez aumenta significativamente. Você pode entender textos complexos e interagir com mais espontaneidade. O Agente B2 desafia você com tópicos mais abstratos e refina o uso de estruturas gramaticais avançadas.

Em cada nível intermediário, os agentes se adaptam, aumentando a complexidade das perguntas e o escopo das correções, garantindo que você esteja sempre aprendendo e sendo desafiado na medida certa.

Dominando o Idioma: Níveis C1 e C2 - O Ápice da Proficiência
Chegar aos níveis C1 e C2 significa que você está se aproximando da proficiência nativa.

C1: Você pode usar o inglês de forma eficaz para fins acadêmicos e profissionais, compreendendo significados implícitos. O Agente C1 foca em nuances, expressões idiomáticas e um uso mais sofisticado da língua.

C2: No nível de domínio, você compreende praticamente tudo e se expressa com total fluidez e precisão. O Agente C2 atua como um parceiro de conversação avançado, refinando os detalhes mais sutis do seu inglês.

Neste ponto, a jornada de escalonamento chega ao seu ápice dentro do framework CEFR, mas a prática e o refinamento continuam, permitindo que você mantenha e aprimore seu alto nível de proficiência.

Como Esta Mágica Acontece (Sob o Capô)
Este projeto é construído sobre uma arquitetura inteligente:

Google ADK (Agent Development Kit): Fornece a estrutura para definir e gerenciar os agentes de conversação.

Google Gemini API: O coração do sistema, oferecendo os poderosos modelos de linguagem (gemini-2.0-flash ou outros) que alimentam a inteligência dos agentes.

Sistema Multi-Agente: Cada nível CEFR (A1 a C2) é representado por um agente especializado, com instruções e foco gramatical/vocabular apropriados para aquele nível.

Escalonamento Inteligente: Os agentes são instruídos a identificar quando a proficiência do usuário excede o nível atual, sinalizando a prontidão para a transição para o próximo agente. Isso é feito através de um "gatilho" oculto na resposta do agente.

Feedback Estruturado: A resposta de cada agente segue um formato unificado de quatro partes: a frase original do usuário, a correção gramatical (em português), uma alternativa/correção em inglês com tradução, e a resposta do agente com uma pergunta para continuar a conversa (também com tradução). Isso garante feedback claro e consistente.

Interface Interativa (Widgets): Utiliza ipywidgets para criar uma interface simples no ambiente do notebook (como Google Colab), permitindo que o usuário selecione o nível inicial e interaja facilmente.

Começando Sua Jornada
Para embarcar nesta aventura de aprendizado, você precisará:

Obter uma Chave API do Google Gemini: Siga as instruções na documentação do Google AI Studio para conseguir sua chave.

Configurar o Ambiente: Este código é projetado para rodar em um ambiente como o Google Colab.

Instalar Dependências: Execute a primeira célula do notebook para instalar as bibliotecas necessárias (google-genai, google-adk, ipywidgets).

Configurar a Chave API no Colab Secrets: Adicione sua chave API como um segredo no Colab com o nome GOOGLE_API_KEY.

Executar o Código: Rode as células restantes no notebook.

Interagir: Use a interface de widgets para selecionar seu nível inicial e começar a conversar com seu tutor de IA!

Próximos Capítulos da História
Este projeto é um ponto de partida. Há muitas maneiras de expandir esta jornada:

Adicionar mais níveis de proficiência (se aplicável, embora C2 seja o topo do CEFR).

Incorporar feedback de pronúncia.

Expandir os tipos de exercícios (escrita, audição, etc.).

Desenvolver uma interface web mais robusta.

Personalizar ainda mais a experiência do agente com base nos interesses do usuário.

Contribuindo
Sua contribuição pode ajudar a moldar os próximos capítulos desta história. Sinta-se à vontade para fazer um fork do repositório, propor melhorias e enviar pull requests.

Licença
Este projeto está sob a Licença [Nome da Licença, por exemplo, MIT]. Veja o arquivo LICENSE para mais detalhes.

Que sua jornada no aprendizado de inglês seja repleta de descobertas e sucesso! Happy practicing!
