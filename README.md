# Chatbot Social Media Expert

## Descrição

Este chatbot utiliza o poder do Google Gemini Pro para gerar posts originais e envolventes para o Instagram. 

## Funcionalidades

- **Geração de Posts Personalizados:** Crie posts únicos para qualquer assunto, adaptando-os ao seu público e tom de voz.
- **Prompt Detalhado:** Coleta informações sobre o tópico, público, tom de voz e exemplos (opcional) para gerar um prompt detalhado, guiando o Gemini Pro para resultados precisos.
- **Flexibilidade Criativa:** Explore diferentes estilos e abordagens, personalizando seus posts com base em exemplos fornecidos ou permitindo que o Gemini Pro gere conteúdo original.
- **Eficiência e Produtividade:** Economize tempo e esforço na criação de conteúdo.

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
