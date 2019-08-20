## Attention Mechanism의 등장 배경

Attention이 나오기 전에 Sequence data를 처리하는 모델은 대부분 Recurrent model(순환 구조)이었습니다. <br/>
Recurrent model은 스스로를 반복하면서 이전에 얻은 정보가 지속되도록 해서, <br/>
자연스럽게 문장의 순차적인 특성이 유지되게 했습니다. <br/><br/>

<img src="https://github.com/hwk06023/Attention/blob/master/images/Recurrent%20model.png" width="30%"></img>

하지만 Recurrent model은 태생적으로 기울기 소실(Vanishing Gradient) 문제를 지니고 있기 때문에, <br/>
초기의 RNN에서부터 long-term dependency(장기 의존성)에 취약하다는 단점을 가지고 있었고, <br/>
이를 보완하기 위해 LSTM 등의 좋은 시도가 있었습니다. 물론 이러한 시도들을 통해, 성능은 개선되었지만 <br/>
여전히 long-term dependency problem은 큰 단점으로 작용했습니다. 이러한 다양한 시도는 계속 되었고, <br/>
Attention mechanism만을 사용했는데, Input과 Output의 의존성을 발견하게 됩니다. <br/> <br/>

위의 내용을 정리하면, Seqeunce to sequence를 처음으로 도입한 조경현 교수님의 <br/>
Learning Phrase Representations using RNN Encoder–Decoder for Statistical Machine Translation의 <br/>
문제점들을 해결하기 위해 다양한 시도 중에, Attention mechanism을 발견하게 된 것 입니다. <br/> <br/>

그렇게 Attention mechanism은 조경현 교수님의 Seqeunce to seqeunce with attetion으로도 유명한 <br/>
Neural Machine Translation by Jointly Learning to Align and Translate 논문에서 처음 소개 되었습니다.

<img src="https://github.com/hwk06023/Attention/blob/master/images/Neural%20Machine%20Translation%20by%20Jointly%20Learning%20to%20Align%20and%20Translate.png" width="350" height="500">

( Neural Machine Translation by Jointly Learning to Align and Translate ) <br/>

## Attention Mechanism

Attention mechanism의 등장 배경에서 Attention mechanism은 Sequence data를 처리하는 <br/>
Seq2Seq 모델(번역 모델)에 처음 쓰이기 시작했다는 것을 알 수 있었습니다. <br/>

Seq2Seq 모델은 기본적으로 Encoder-Decoder의 형태를 가지고 있습니다. [Seq2Seq 참고](https://github.com/hwk06023/Seq2Seq)

그렇다면 Seq2Seq에 쓰이는 Attention mechanism은 무엇일까요? <br/>
Seq2Seq에 쓰이는 Attention mechanism은, Decoder의 매 time-step마다 Encoder의 모든 <br/>
time-step의 output을 참고하는데, Encoder의 모든 time-step의 output을 전부 다 동일한 비율로 참고하지 않고, <br/>
해당 Decoder의 time-step에서 연관이 있는 부분을 좀 더 집중(Attention)해서 참고합니다. <br/>





