:speech_balloon: # Document Translator

Este projeto traduz documentos do formato `.docx` utilizando a API do **Microsoft Translator Text**. Ele é capaz de processar texto de um arquivo `.docx`, traduzir os parágrafos para o idioma desejado e gerar um novo documento traduzido.

## Recursos
- Tradução de texto usando a API do **Microsoft Translator Text**.
- Processamento de documentos `.docx` para leitura e escrita.
- Suporte para múltiplos idiomas de destino.

## Pré-requisitos
Antes de executar o projeto, certifique-se de ter:
- Python 3.6 ou superior instalado.
- As bibliotecas necessárias instaladas:
  ```bash
  pip install requests python-docx
Uma chave de assinatura válida para a API do Microsoft Translator Text.
Configuração
Obtenha uma chave de assinatura e um endpoint da API no portal do Azure Cognitive Services.
Substitua o valor da variável subscription_key pelo seu código de assinatura.
Substitua o valor da variável endpoint pelo endpoint do seu serviço.

## Como usar

# 1. Traduzir texto

A função translator_text pode ser usada para traduzir strings de texto diretamente. Exemplo:

python
translated_text = translator_text("As He marched up that hill", "pt-br")
print(translated_text)

Saída: 
"Enquanto Ele marchava até aquela colina"

# 2. Traduzir o documento

Para traduzir um arquivo .docx:
Certifique-se de que o documento está no mesmo diretório ou forneça o caminho completo.

Use a função translate_document. Exemplo:

python
input_file = "/caminho/para/seu/documento.docx"
output_file = translate_document(input_file)
print(f"Documento traduzido salvo em: {output_file}")
O arquivo traduzido será salvo no mesmo local com o sufixo do idioma escolhido.

# 3. Idiomas suportados

O idioma de destino é configurado pela variável language_destination. Atualmente, está configurado como português do Brasil (pt-br). Você pode alterar para outros idiomas suportados pela API modificando o código.

Estrutura do Código
translator_text:

Função para tradução de texto simples.
translate_document: 

Processa um documento .docx, traduz parágrafos e cria um novo arquivo traduzido.

Exemplo de Saída
Arquivo original:
As He marched up that hill
Arquivo traduzido:
Enquanto Ele marchava até aquela colina

# Notas

Este projeto utiliza a API do Microsoft Translator Text que pode gerar custos dependendo do volume de requisições.
Certifique-se de não expor sua chave de API em repositórios públicos.

# Contribuições

Sinta-se à vontade para abrir issues ou enviar pull requests para melhorias no projeto.

# Licença

Este projeto está licenciado sob a MIT License.
