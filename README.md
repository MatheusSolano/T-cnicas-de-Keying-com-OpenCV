# Técnicas de Keying com OpenCV: Criação de Cenários Virtuais

Esse programa usa Técnicas de Keying e a biblioteca OpenCV, para trocar o fundo verde de um vídeo por qualquer outro vídeo ou imagem.

<p align="center">
  <img src="Fundo_Verde_GIF.gif" style="width: 700px; height: 400px;">
</p>

## Estrutura do Projeto

A estrutura do projeto é a seguinte:
```
.
├── data
│   ├── praia.mp4
│   └── webcam.mp4
├── projeto_01.py
└── requirements.txt
```

## Descrição dos arquivos:

* `praia.mp4`: fundo da praia que sera usado no projeto.
* `webcam.mp4`: video com uma pessoa e um fundo verde. 
* `projeto_01.py`: código fonte do projeto.  
* `requirements.txt`: arquivo que lista as dependências necessárias para executar o programa.

## Pré-requisitos
Para executar este projeto, você precisa ter o Python instalado em seu sistema, eu estou usando a versão *3.8.5*. As dependências do projeto são listadas no arquivo requirements.txt e podem ser instaladas com o seguinte comando:

```
pip install -r requirements.txt
```
## Execução do Projeto

Para executar o projeto, basta executar o código na IDE de sua preferencia.

Este comando irá iniciar o programa que exibirá o vídeo com o fundo alterado na tela e salvará o output na pasta do projeto.

## Detalhes do Projeto

Este programa altera o fundo de um vídeo com fundo verde. O processo ocorre nas seguintes etapas:

1. Captação do fluxo de vídeo em tempo real através da webcam.
2. Define os limites da cor verde em RGB.
3. Cria uma máscara com os pixels que estão dentro da faixa de cor verde.
4. Usa a máscara para extrair os pixels da praia que correspondem ao fundo verde da webcam.
5. Inverte a máscara para obter os pixels que não estão na faixa de cor verde
6. Usa a máscara invertida para extrair os pixels da webcam que não são verdes.
7. Escreve os quadros nos arquivos de vídeo correspondentes.
