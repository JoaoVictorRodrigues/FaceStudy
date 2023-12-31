# Face Study
Projeto de visão computacional pra reconhecer emoções, estimar idade, genero e raça em tempo real de uma forma fácil e simples.

## Feito por: 
- Gabriela Choichit Giosa
- Guilherme Augusto Chaves de Carvalho
- João Victor Rodrigues Silva

## Descrição do projeto 


### Setup
Antes de tudo é preciso instalar a biblioteca [DeepFace](https://github.com/serengil/deepface), para isso, execute o comando a seguir:

```sheel
$ pip install -r requirements.txt
```
### Usage
Para utilizar a biblioteca FaceStudy basta fazer o import
```python 
from faceStudy import FaceStudy, AsyncFaceStudy
```

Abaixo você pode encontrar um exemplo de como utilizar a biblioteca
```python
import asyncio
from FaceStudy import AsyncFaceStudy, SyncFaceStudy

if __name__ == "__main__":
    #anlyze_type: pode receber um dos quatro tipos de análise:
    #'emotion', 'age', 'gender' or 'race'
    sync_face_study = SyncFaceStudy(analyze_type='emotion' window='Sync Face Study')
    
    sync_face_study.run()
```

Na pasta [/test](./test/) você encontra exemplos de uso sincronos e assincronos. 

### Output
A função pode retornar quatro tipos de de informação: Emotion, Age, Gender, Race.
A saida no terminal tem o seguinte aspecto:

```shell
Action: emotion: 100%|████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████| 1/1 [00:00<00:00, 19.60it/s]
Dominant emotion: neutral

Action: emotion: 100%|████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████| 1/1 [00:00<00:00, 19.23it/s]
Dominant emotion: neutral
```
Ao executar o programa, a seguinte janela será exibida com o tipo de analise requerida, no caso do teste, Emotion


![](https://github.com/JoaoVictorRodrigues/FaceStudy/blob/main/images/demo.gif)
<img src="https://joaovictorrodrigues.github.io/FaceStudy/images/demo.gif" alt="zigzag" />

Para encerrar a janela de análise, basta apretar `q` ou fechar a janela.
