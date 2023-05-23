## Teste do Módulo RTMP do Nginx

Este guia ajudará você a testar rapidamente o módulo RTMP do Nginx.

### Pré-requisitos

Certifique-se de ter o Docker instalado em seu sistema.

### Instalação

Siga os seguintes passos para configurar e testar o módulo RTMP do Nginx:

1. Clone o repositório:

2. Acesse o diretório do repositório:

3. Construa a imagem do Docker: ``` docker build -t nginx-rtmp-test . ```

4. Execute o contêiner Docker: ``` docker run -d -p 1935:1935 nginx-rtmp-test ```


### Testando

Para testar o servidor RTMP do Nginx, você pode usar o OBS Studio para fazer streaming e o VLC para reprodução.

1. Abra o OBS Studio e vá para **Configurações** > **Stream**.

2. Selecione **Custom** como o **Server**.

3. Insira a URL do RTMP `rtmp://127.0.0.1/live`.

4. Clique em **OK** para salvar as configurações.

5. Para assistir a stream no VLC, abra o player VLC.

6. Vá para **Mídia** > **Rede**.

7. Insira a mesma URL do RTMP `rtmp://127.0.0.1/live`.

8. Clique em **Reproduzir** para iniciar a reprodução do stream.

Certifique-se de que o contêiner Docker esteja em execução e configurado corretamente para que o teste seja bem-sucedido.

Este guia pressupõe que você tenha um entendimento básico do Docker, OBS Studio e VLC.
