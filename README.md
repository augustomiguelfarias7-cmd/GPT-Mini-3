GPT-Mini 3 – Biblioteca Python

GPT-Mini 3 é um modelo de linguagem avançado, inspirado na arquitetura GPT, projetado para ser multimodal, multilíngue e possuir memória de curto prazo. Ele combina capacidades de geração de texto, processamento de áudio, análise e geração de imagens, e ainda pode atuar como um agente controlado com limite de acesso a sites específicos.

Principais Funcionalidades

1. Processamento de Texto

Suporte a múltiplos idiomas, incluindo português, inglês, francês, espanhol, alemão, italiano, russo, chinês, japonês e coreano.

Memória de curto prazo: armazena informações recentes para contextualizar respostas.

Capacidade de gerar códigos e manipular arquivos através do modo agente.


2. Multimodalidade

Imagens: Geração de imagens com integração DALLE e análise de imagens via OpenCLIP.

Áudio: Transcrição de áudio com Whisper.

Combina inputs de texto, áudio e imagens para respostas mais completas.


3. Modo Agente

Controle de acesso a sites com limite de tempo (ex.: ChatGPT, Gmail, Drive).

Pode gerar código, criar arquivos e pastas, interagir com o ChatGPT para suporte em tarefas complexas.

Limites configuráveis de tempo de sessão (10 minutos por site, por padrão).


4. Fácil Integração em Python

from gpt_mini_3 import GPTMini3Agent, SimpleTokenizer, GPTMini3Config

tokenizer = SimpleTokenizer()
config = GPTMini3Config(vocab_size=tokenizer.vocab_size)
model = GPTMini3Agent(config)

print(model.enter_site("chatgpt"))
print(model.enter_site("gmail"))

5. Aplicações

Assistentes virtuais inteligentes.

Geração automática de código e arquivos.

Ferramenta de multimodalidade para projetos de IA.

Agentes autônomos controlados em Python.


========================≈============
pip install torch transformers datasets pillow open-clip-torch whisper dalle-pytorch beautifulsoup4 requests


gpt_mini_3/
├── __init__.py
├── agent.py         # contém GPTMini3Agent, SimpleTokenizer, GPTMini3Config

from gpt_mini_3 import GPTMini3Agent, SimpleTokenizer, GPTMini3Config

tokenizer = SimpleTokenizer()
config = GPTMini3Config(vocab_size=tokenizer.vocab_size)
model = GPTMini3Agent(config)

print(model.enter_site("chatgpt"))
print(model.enter_site("gmail"))
