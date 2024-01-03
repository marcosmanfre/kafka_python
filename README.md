# YouTube API para Notificações Reativas

Este repositório contém uma solução que utiliza Python, Kafka, ksqlDB e Telegram para criar notificações ao vivo a partir de uma fonte de dados estática, demonstrando especificamente a transformação da API REST do YouTube em um sistema reativo.

## Visão Geral

Neste episódio do Coding in Motion, Kris Jenkins demonstra como transformar uma fonte de dados estática, como a API REST do YouTube, em um sistema reativo que fornece notificações ao vivo. A solução aborda os seguintes passos:

- Utilização do Python para buscar e processar dados da API REST do YouTube.
- Transmissão ao vivo dos dados obtidos, do Python para um tópico do Kafka.
- Processamento dos dados recebidos usando o ksqlDB, observando mudanças importantes.
- Envio de notificações personalizadas ao vivo via Telegram com base nos dados processados.

## Funcionalidades

- **Busca de Dados com Python**: Busca dados na API REST do YouTube.
- **Integração com o Kafka**: Transmite dados para tópicos do Kafka para processamento em tempo real.
- **Processamento com ksqlDB**: Analisa os dados recebidos em busca de mudanças significativas.
- **Notificações via Telegram**: Envia notificações ao vivo com base nas mudanças dos dados processados.

## Configuração e Uso

### Requisitos

- Python 3.x
- Kafka
- ksqlDB
- Chave de API do bot do Telegram

### Instalação:
Clone este repositório.

### Configuração:
Configure as chaves de API necessárias para o YouTube e o Telegram no arquivo de configuração.

config = {
    "google_api_key": "*****",
    "youtube_playlist_id": "*****",
      "kafka": {
            "bootstrap.servers": "*****",
            "security.protocol": "sasl_ssl",
            "sasl.mechanism": "PLAIN",
            "sasl.username": "*****",
            "sasl.password": "*****",
        },
        "schema_registry": {
            "url": "*****",
            "basic.auth.user.info": "*****",
        }
    }

### Execução da Solução:
Execute os scripts Python para buscar dados e transmiti-los para o Kafka.
Configure o ksqlDB para processar os dados recebidos e acionar notificações.
Execute o bot do Telegram para receber notificações ao vivo.
