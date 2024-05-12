# Apresentação: Chatbot Social Media Expert

## Introdução

O **Chatbot Social Media Expert** é uma ferramenta inovadora que utiliza o poder da inteligência artificial do Google Gemini Pro para gerar posts originais e envolventes para o Instagram. Com este chatbot, você pode criar conteúdo personalizado para diferentes públicos e tons de voz, elevando suas estratégias de mídia social a um novo patamar.

## Funcionalidades

- **Geração de Posts Personalizados:** Crie posts originais e envolventes para qualquer assunto, adaptando o conteúdo ao seu público-alvo e ao tom de voz desejado.
- **Prompt Detalhado para Resultados Precisos:** Coleta informações sobre o tópico, público-alvo, tom de voz e exemplos (opcional) para gerar um prompt detalhado, guiando o Gemini Pro para resultados precisos.
- **Flexibilidade Criativa:** Explore diferentes estilos e abordagens, personalizando seus posts com base em exemplos que você fornece, ou deixando o Gemini Pro usar sua criatividade para gerar conteúdo único.
- **Eficiência e Produtividade:** Economize tempo e esforço na criação de conteúdo, permitindo que o chatbot gere sugestões de posts em segundos.

## Como Funciona

1. **Instalação:** O chatbot requer a instalação do SDK do Google Generative AI (`!pip install -q -U google-generativeai`) e a configuração da sua API Key.
2. **Interação:** O chatbot inicia uma conversa, perguntando sobre o assunto do post, público-alvo, tom de voz e se deseja fornecer exemplos.
3. **Geração de Conteúdo:** Com base nas suas respostas, o chatbot cria um prompt detalhado para o Gemini Pro, que gera um post original e envolvente para o Instagram, incluindo hashtags relevantes.
4. **Apresentação do Resultado:** O chatbot exibe o post gerado, pronto para ser copiado e colado no Instagram.

## Benefícios

- **Crie Conteúdo Original e Atraente:** Supere o bloqueio criativo e gere posts que realmente engajam seu público.
- **Otimize seu Tempo:** Concentre-se em outras tarefas importantes enquanto o chatbot cuida da criação de conteúdo.
- **Aprimore sua Estratégia de Mídias Sociais:** Adapte seus posts a diferentes públicos e tons de voz, maximizando o impacto das suas campanhas.

## Conclusão

O Chatbot Social Media Expert é uma ferramenta essencial para qualquer pessoa que busca impulsionar seus resultados no Instagram. Experimente agora e descubra o poder da IA na criação de conteúdo!


## Como Usar

1. **Instalação:**
    ```bash
    !pip install -q -U google-generativeai
    ```
2. **Configuração:**
    - Substitua `SUA_API_KEY` pela sua API Key do Google Cloud:
    ```python
    import os
    import google.generativeai as genai

    GOOGLE_API_KEY="SUA_API_KEY"
    os.environ["GOOGLE_API_KEY"] = GOOGLE_API_KEY

    # ... (restante do código)
    ```
3. **Execute o código:** 
    - Responda às perguntas do chatbot sobre o tema, público, tom de voz e exemplos (opcional).
    - O chatbot gerará um post para o Instagram, pronto para ser usado!

## Código

```python
# Instalando o SDK do Google
!pip install -q -U google-generativeai

# Configurações iniciais
import os
import google.generativeai as genai

GOOGLE_API_KEY="SUA_API_KEY" # Substitua pela sua API Key
os.environ["GOOGLE_API_KEY"] = GOOGLE_API_KEY

# Configurações de geração 
generation_config = genai.GenerationConfig(
    temperature=0.9,  
    top_k=40,         
    max_output_tokens=200  
)

# Carregando o modelo Gemini Pro 
model = genai.GenerativeModel(
    model_name="models/gemini-pro", 
    generation_config=generation_config
)

# Função para gerar conteúdo para o Instagram com Gemini Pro
def generate_instagram_post(topic, audience, tone, examples=None):
  # ... (código da função)

# Chatbot
try:
  # ... (código do chatbot)
except KeyboardInterrupt:
  print("\nChat interrompido.")

print("Fim do programa.")
