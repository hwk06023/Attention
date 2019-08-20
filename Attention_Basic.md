## Attention Mechanism의 등장 배경

Attention이 나오기 전에 Sequence data를 처리하는 모델은 대부분 Recurrent model(순환 구조)이었습니다. <br/>
Recurrent model은 스스로를 반복하면서 이전에 얻은 정보가 지속되도록 해서, <br/>
자연스럽게 문장의 순차적인 특성이 유지되게 했습니다. <br/><br/>

<img src="https://github.com/hwk06023/Attention/blob/master/images/Recurrent%20model.png" width="30%"></img>

하지만 Recurrent model은 태생적으로 기울기 소실(Vanishing Gradient) 문제를 지니고 있기 때문에, <br/>
초기의 RNN에서부터 long-term dependency(장기 의존성)에 취약하다는 단점을 가지고 있었고, <br/>
이를 보완하기 위해 LSTM 등의 좋은 시도가 있었습니다. 물론 이러한 시도들을 통해, 성능은 개선되었지만 <br/>
여전히 long-term dependency problem은 큰 단점으로 작용했습니다. 이러한 다양한 시도는 계속 되었고, <br/>
Attention mechanism만을 사용했는데, Input과 Output의 의존성을 발견하게 됩니다. <br/>


그렇게 Attention mechanism은 조경현 교수님의 Seqeunce to seqeunce with attetion으로도 유명한

<img src="https://github.com/hwk06023/Attention/blob/master/images/Neural%20Machine%20Translation%20by%20Jointly%20Learning%20to%20Align%20and%20Translate.png" width="350" height="500">

Neural Machine Translation by Jointly Learning to Align and Translate 논문에서 처음 소개 되었습니다.<br/><br/>

## Attention Mechanism

Attention mechanism의 등장 배경에서 Attention mechanism은 Sequence data를 처리하는 
Seq2Seq 모델(번역 모델)에 처음 쓰이기 시작했다는 것을 알 수 있었습니다.

현재 Attention은 




## Attention Is All You Need

Attention Is All You Need는 2017년 6월 12일 구글 브레인, 구글 리서치 팀에서 발표한 <br/>
신경망을 이용한 기계 번역(NMT: Neural Machine Translation)에 대한 논문입니다. <br/>
Attention mechanism은 이름처럼 모델로 하여금 중요한 부분만 집중하게 만드는 것이 핵심입니다. <br/>
Recurrent, Convolution을 사용하지 않고 이러한 Attention mechanism만을 사용하는 간단한 신경망 구조를 통해 <br/>
기계 번역 분야에서 최고의 성능을 얻음과 동시에 연산 비용(Computation cost)을 줄인 것이 이 논문의 큰 특징입니다. <br/>
이를 간단하게 설명 해보자면, Encoder 부분은 각 부분에 Attention을 더해주고, Decoder 부분은 Masking 기법을 통해 <br/>
출력을 생성할 때에 각 단계별로 입력 시퀀스의 각기 다른 부분을 집중(병렬 처리) 할 수 있게 해줍니다. <br/>
##### (Encoder, Decoder의 구조 및 Masking 기법에 관해서는 밑에 Transformer의 전체적인 구조를 설명하면서 함께 설명하도록 하겠습니다.) <br/>

<img src="https://github.com/hwk06023/Attention/blob/master/images/AttentionIsAllYouNeed_The%20Transformer.png" width="500" height="700">


논문에서 The Transformer 이라고 불리는 이 모델의 구조는 
