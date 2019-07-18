## Attention이 나오기 전

Attention이 나오기 전에 시퀀스 데이터를 처리하는 모델은 대부분 Recurrent model(순환 구조)이었습니다. <br/>
Recurrent model은 스스로를 반복하면서 이전에 얻은 정보가 지속되도록 해서, 자연스럽게 문장의 순차적인 특성이 유지되게 했습니다. <br/>

하지만 Recurrent model은 초기의 RNN에서부터 long-term dependency(장기 의존성)에 취약하다는 단점을 가지고 있었고, <br/>
이를 보완하기 위해 LSTM 등의 좋은 시도가 있었습니다. 물론 이러한 시도들을 통해, 성능은 개선되었지만 <br/>
여전히 long-term dependency problem은 큰 단점으로 작용했습니다. 이러한 다양한 시도는 계속 되었고, <br/>
Attention mechanism만을 사용했는데, Input과 Output의 의존성을 발견하게 됩니다! <br/>
