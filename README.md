
# Steganography com Criptografia e Hashing

Este projeto implementa um sistema de esteganografia para embutir e recuperar mensagens ocultas em imagens. Além disso, inclui funcionalidades para encriptação/descrição de mensagens com chaves públicas e privadas, e geração de hash das imagens. O sistema utiliza a biblioteca `PIL` para manipulação de imagens e `cryptography` para as operações de criptografia.

## Funcionalidades

1. **Embutir Texto na Imagem (Steganography)**: 
   Embute um texto em uma imagem modificando o último bit do valor do canal vermelho (R) de cada pixel da imagem.
   
2. **Recuperar Texto de uma Imagem Alterada**: 
   Recupera o texto oculto de uma imagem alterada através da esteganografia, extraindo o último bit de cada pixel.

3. **Gerar Hash de Imagens**:
   Gera o hash SHA-256 de uma imagem, permitindo verificar se a imagem foi modificada ao comparar o hash da imagem original com o da imagem alterada.

4. **Encriptar Texto com Chave Pública**:
   Encripta uma mensagem usando a criptografia RSA com a chave pública gerada automaticamente.

5. **Decriptar Texto com Chave Privada**:
   Descriptografa o texto encriptado usando a chave privada correspondente.

6. **Upload de Arquivos no Google Colab**:
   As funções de upload de imagem permitem fazer upload de imagens diretamente no Google Colab, usando a biblioteca `files` do `google.colab`.

## Como Usar

### Instalar Dependências

Certifique-se de instalar as bibliotecas necessárias:

```bash
pip install pillow cryptography
```

### Executando o Programa

1. **Iniciar o Menu**: O programa exibe um menu de opções, permitindo selecionar uma das funcionalidades mencionadas.

2. **Embutir Texto em Imagem**: Você será solicitado a fazer upload de uma imagem e fornecer um texto a ser embutido. A imagem será salva com o texto oculto.

3. **Recuperar Texto de Imagem**: Faça upload de uma imagem com texto embutido e o texto será recuperado e exibido.

4. **Gerar Hash de Imagens**: Faça upload de duas imagens (original e alterada) para comparar os hashes e verificar se houve alteração nos pixels.

5. **Encriptar Texto**: Digite a mensagem a ser encriptada e escolha a imagem onde o texto encriptado será embutido.

6. **Decriptar Texto**: Faça upload de uma imagem contendo texto encriptado e a mensagem será decriptada.

### Estrutura do Código

- **Função `embutir_texto(imagem, texto)`**: Embute o texto na imagem utilizando esteganografia, modificando o último bit de cada valor RGB de cada pixel.
  
- **Função `recuperar_texto(imagem)`**: Recupera o texto oculto em uma imagem alterada, extraindo o último bit do valor RGB de cada pixel.

- **Função `gerar_hash(imagem)`**: Gera e exibe o hash SHA-256 da imagem fornecida.

- **Função `encriptar_texto(mensagem)`**: Encripta o texto usando criptografia RSA com a chave pública.

- **Função `decriptar_texto(texto_encriptado)`**: Decripta o texto usando a chave privada.

- **Função `upload_imagem()`**: Realiza o upload de uma imagem no Google Colab.

- **Função `menu()`**: Exibe o menu interativo com as opções de uso do sistema.

## Exemplos de Uso

1. **Embutir Texto**:
   - Escolha a opção 1 e faça o upload de uma imagem.
   - Digite o texto a ser embutido e o sistema criará uma nova imagem com o texto oculto.

2. **Recuperar Texto**:
   - Escolha a opção 2 e faça o upload da imagem com texto oculto.
   - O sistema recuperará e exibirá o texto escondido na imagem.

3. **Gerar Hash**:
   - Escolha a opção 3 e faça o upload das imagens original e alterada.
   - O sistema comparará os hashes das imagens e indicará se houve alteração.

4. **Encriptar e Embutir Texto**:
   - Escolha a opção 4, encripte uma mensagem e embuta o texto encriptado em uma imagem.

5. **Decriptar Texto**:
   - Escolha a opção 5 e faça o upload da imagem com texto encriptado para descriptografá-lo.
