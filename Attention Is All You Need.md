# Attention Is All You Need

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
