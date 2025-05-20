# Instruções para Deploy no Streamlit Cloud - Versão API

## O que é o Streamlit Cloud?

O Streamlit Cloud é uma plataforma gratuita que permite hospedar aplicativos Streamlit na nuvem sem necessidade de conhecimentos avançados de programação ou infraestrutura.

## Pré-requisitos

1. Uma conta GitHub (gratuita)
2. Uma conta no Streamlit Cloud (gratuita)
3. Uma chave API da OpenAI (necessária para usar o serviço de transcrição)

## Como obter uma chave API da OpenAI

1. Acesse [platform.openai.com](https://platform.openai.com/)
2. Crie uma conta ou faça login
3. Vá para "API Keys" no menu
4. Clique em "Create new secret key"
5. Dê um nome para sua chave e clique em "Create"
6. Copie a chave (você precisará dela para usar o aplicativo)

**Nota**: A OpenAI oferece créditos gratuitos para novos usuários, mas depois disso, o serviço é pago. Consulte a [página de preços](https://openai.com/pricing) para mais informações.

## Passo a Passo para Deploy

### 1. Criar uma conta no GitHub

Se você ainda não tem uma conta no GitHub:
1. Acesse [github.com](https://github.com)
2. Clique em "Sign up" e siga as instruções para criar uma conta gratuita

### 2. Criar um novo repositório no GitHub

1. Após fazer login no GitHub, clique no botão "+" no canto superior direito
2. Selecione "New repository"
3. Dê um nome ao repositório (ex: "app-transcricao-videos")
4. Deixe o repositório como "Public"
5. Clique em "Create repository"

### 3. Fazer upload dos arquivos para o GitHub

1. No seu novo repositório, clique no link "uploading an existing file"
2. Arraste os arquivos do aplicativo ou clique para selecionar:
   - `app.py`
   - `requirements.txt`
3. Clique em "Commit changes"

### 4. Criar uma conta no Streamlit Cloud

1. Acesse [streamlit.io/cloud](https://streamlit.io/cloud)
2. Clique em "Sign up" e siga as instruções
3. Recomendamos fazer login com sua conta GitHub para facilitar a integração

### 5. Deploy do aplicativo

1. Após fazer login no Streamlit Cloud, clique em "New app"
2. Selecione o repositório que você acabou de criar
3. Na seção "Main file path", digite: `app.py`
4. Clique em "Deploy!"

O Streamlit Cloud irá automaticamente:
- Detectar o arquivo requirements.txt
- Instalar todas as dependências necessárias
- Iniciar o aplicativo

### 6. Acessar e configurar o aplicativo

1. Após o deploy ser concluído, você receberá um URL público para o seu aplicativo
2. Acesse o aplicativo através desse URL
3. Vá para a aba "Configurações"
4. Insira sua chave API da OpenAI no campo apropriado
5. Clique em "Salvar Chave API"
6. Volte para a aba "Upload de Arquivo" para começar a usar o aplicativo

## Como usar o aplicativo

1. Faça upload de um arquivo de áudio ou vídeo
2. Selecione o idioma (opcional)
3. Clique em "Transcrever Arquivo"
4. Aguarde o processamento
5. O texto transcrito será exibido na tela
6. Use o botão "Download TXT" para baixar o texto transcrito

## Observações Importantes

1. **Recursos Gratuitos**: O plano gratuito do Streamlit Cloud tem algumas limitações:
   - O aplicativo "adormece" após inatividade
   - Recursos computacionais limitados

2. **Chave API da OpenAI**: 
   - Sua chave API é armazenada apenas na sessão do navegador
   - Você precisará inseri-la novamente se limpar os cookies ou usar outro navegador
   - Mantenha sua chave API segura e não a compartilhe

3. **Tamanho de Arquivos**:
   - O Streamlit Cloud limita o tamanho de upload a aproximadamente 200MB
   - Arquivos muito grandes podem ser rejeitados

4. **Para vídeos do YouTube/Instagram**:
   - Baixe os vídeos manualmente usando sites como y2mate.com ou savefrom.net
   - Faça upload do arquivo baixado no aplicativo

## Suporte

Se você encontrar problemas durante o deploy:
1. Verifique os logs de erro no Streamlit Cloud
2. Consulte a [documentação oficial do Streamlit](https://docs.streamlit.io/)
3. Busque ajuda na [comunidade do Streamlit](https://discuss.streamlit.io/)
