# ProjetoDIO


# 🎤 Voice-to-Voice AI Assistant (Colab)

Este projeto demonstra a criação de um assistente virtual capaz de ouvir comandos de voz, processá-los utilizando inteligência artificial e responder também por meio de voz sintetizada. O projeto foi desenvolvido para ser executado diretamente no **Google Colab**.

## 🚀 Fluxo de Funcionamento

O pipeline da aplicação segue estas quatro etapas principais:

1.  **Captura de Áudio:** Utiliza JavaScript e a `MediaStream Recording API` para captar áudio do microfone do usuário diretamente no navegador.
2.  **Transcrição (STT):** O modelo **Whisper da OpenAI** converte o áudio gravado em texto de forma precisa.
3.  **Processamento de IA (LLM):** O texto transcrito é enviado para a API do **ChatGPT (GPT-3.5 Turbo)**, que gera uma resposta inteligente.
4.  **Sintetização de Voz (TTS):** A biblioteca **gTTS (Google Text-to-Speech)** converte a resposta em texto do ChatGPT de volta em áudio.

---

## 🛠️ Tecnologias Utilizadas

* **Python 3.x**
* **OpenAI Whisper:** Reconhecimento de fala robusto.
* **OpenAI API:** Cérebro do assistente (GPT-3.5).
* **gTTS:** Biblioteca para síntese de voz do Google.
* **JavaScript:** Interface com o hardware (microfone) via navegador.

---

## 📋 Pré-requisitos

Para rodar este projeto, você precisará de:

1.  Uma conta no **Google Colab**.
2.  Uma **API Key da OpenAI**. Você pode gerá-la em [platform.openai.com](https://platform.openai.com/account/api-keys).
    > **Atenção:** Mantenha sua chave em segurança. No código, substitua `os.environ['OPENAI_API_KEY']` pela sua chave privada.

---

## 🔧 Como Usar

1.  **Configuração Inicial:** Execute as células de instalação das bibliotecas (`whisper`, `openai`, `gTTS`).
2.  **Gravação:** Ao executar a função `record()`, o navegador solicitará permissão para usar o microfone. Fale por 5 segundos (ou o tempo definido).
3.  **Processamento:** O Whisper fará a transcrição automática.
4.  **Resposta:** O ChatGPT processará o texto e o áudio da resposta será reproduzido automaticamente no player do Colab.

---

## ⚠️ Observações Importantes

* **API do ChatGPT:** Este projeto utiliza a versão `0.28` da biblioteca da OpenAI. Caso queira usar versões mais recentes, ajustes na sintaxe de chamada (`openai.ChatCompletion`) podem ser necessários.
* **Ambiente Colab:** Como o Python roda em um servidor remoto, o uso de JavaScript é essencial para acessar o hardware local do seu computador.

---

## 📄 Licença

Este projeto é para fins educacionais. Sinta-se à vontade para clonar, modificar e melhorar!

---

### Dicas para o seu Repositório:
* **Segurança:** Eu notei que no seu código há uma API Key real exposta (`sk-proj-...`). **Recomendo fortemente que você revogue essa chave no painel da OpenAI e gere uma nova**, pois chaves expostas publicamente podem ser drenadas por bots em poucos minutos.
* **GIF/Demo:** Se puder, grave um pequeno vídeo ou GIF do assistente funcionando e coloque no topo do README. Isso valoriza muito o portfólio!
