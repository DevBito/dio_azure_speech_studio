# dio_azure_speech_studio

Ok, aqui documento o precesso de transcrição de audio, a principio serei simples e prático para explicar como funciona a ferramenta, após isso irei usar o output do arquivo de aúdio utilizado, para explicar o que ocorre após a transcrição.
## 1 Utilizei o seguinte recurso
![Captura de tela 2024-04-11 191709](https://github.com/DevBito/dio_azure_speech_studio/assets/141591990/c79adfb0-9d34-4e87-9f71-6770f2f5451c)

## 2 Foi solicitado algum arquivo de aúdio para realizar a transcrição do aúdio, logo upei o "WhatAICanDo.W4a"
![image](https://github.com/DevBito/dio_azure_speech_studio/assets/141591990/69f3aa6b-982f-40c7-b14d-631a548bc4ce)

## 3 Obtive o seguinte texto: "AI enables us to build amazing software that can improve healthcare, enable people to overcome physical disadvantages. Empower smart infrastructure, create incredible entertainment experiences, and even save the planet.".  E foi gerado um arquivo JSON, que especifica em qual momento cada palavra será encaixada no contexto do áudio. Muito útil para o Spotify, pois algumas músicas não possuem legendas e algumas que possuem, não há sicronização com a letra...
![image](https://github.com/DevBito/dio_azure_speech_studio/assets/141591990/77ab3a5d-68c7-4e5b-a3cc-165ad05f4828)


# Breve análise
![image](https://github.com/DevBito/dio_azure_speech_studio/assets/141591990/232a6cfc-db18-4451-b110-2f5626d81e08)
- Id: É o identificador único da transcrição.
- Channel: Indica o canal de áudio se houver mais de um canal. Um valor de 0 geralmente significa o primeiro canal.
- Confidence: Indica a precisão da transcrição. Valor mais alto indica maior confiança.
- Lexical: Esta é a transcrição textual exata sem considerar a pronúncia.
- ITN (Interpretation): É uma transcrição interpretada, muitas vezes ajustada para torná-la mais compreensível ou gramaticalmente correta.
- MaskedITN (Masked Interpretation): Esta transcrição pode ser mascarada, o que significa que algumas partes podem ter sido removidas ou mascaradas por razões de privacidade ou confidencialidade.
- DisplayText: É o texto da transcrição que foi gerado pelo sistema de reconhecimento de fala.


- Words: A palavra transcrita.
- RecognitionStatus: Indica o status da transcrição, se o valor for igual a "zero" 0 signifca que a transcrição foi um sucesso.
- Offset: Infica em qual momento em milissegundo a transcrição da palavra começa.
- Duration: É a duração da transcrição em milissegundos.

