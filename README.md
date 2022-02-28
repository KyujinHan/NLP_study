# NLP_study
Transformer부터 BERT 활용 그리고 2021년 가장 뛰어난 언어 인공지능이라 평가받는 GPT까지 논문과 교재를 활용하여 코드 실습  


# Transformer
트랜스포머. NLP 분야를 점령해버린 엄청난 결과물. 갠적으로 트랜스포머를 공부하면서 많이 놀라움을 감추지 못했다. Encoder와 Decoder를 활용한 기술. 그리고 그 안에 들어가 있는 Self-attention과 Multi-head-attention    
그리고 Encoder-Decoder Attetion(Multi-head-attention) 까지 공부할께 너무나도 많았다.    
  
그리고 Selt-attetnion을 구성하는 Query, Key, Value에 대한 특징을 공부하는 것도 쉽지 않았고 attention의 원리도 이해하는 것도 흥미로웠지만 꽤 시간을 들인 것 같다.    
  
NLP 분야에 이용되던 RNN을 버리고 오직 Attention만을 이용해서 구현한다는 것은 획기적이다...  
(Positional Embedding vector를 추가하는 것이 매우 좋은 아이디어 같다. 근데 이 포지션 벡터가 효과가 없다는 의견도 종종 있다.)  
  
꼭 논문을 통해 공부하는 것을 추천한다.    

- Attention Is All You Nedd: https://arxiv.org/abs/1706.03762 



# BERT
- Bidirectional Transformers for Language Understanding  
이 논문의 제목에 집중할 키워드는 Bidrectional Transformers와 Pre-trained  


Transformer의 Encdoer를 이용한 NLP Taks!!   
이는 Transformer를 활용하는데 Pre-trained과 Fine-tuning을 적극적으로 활용한 Task이다.    
NSP와 MLM Taks을 이용해서 BERT를 학습하고, NLP 안에 있는 수많은 분야에 적용하기 위해 약간의 Fine-tuning을 접목시키면서 NLP 분야에 혁신을 일으켰다고 할 수 있다.   
  
아마 이 논문을 기점으로 Fine-tuning에 대한 중요성과 이목이 훨씬 더 집중되지 않았나 싶기도 하다.  
  
WordPiece Embedding을 이용하였다.  

- BERT: Pre-training of Deep Bidirectional Transformers for Language Understanding: https://arxiv.org/pdf/1810.04805.pdf   
 (BERT에서 파생된 모델들은 MLM, NSP TASK들의 단점을 보완하여 각기 다른 방법으로 Trained을 진행하였다. 이 점을 보고 Fine-tuning과 Pre-trained의 엄청난 기능을 느꼈던 것 같다..)  

# GPT
- Generative Pre-Training  
NLP분야에서 큰 파장을 불러일으킨 GPT...  
GPT-2는 Open AI측에서 너무나 성능이 뛰어나 공개하지 않겠다 말을 했을 정도고, 최근에 나온 GPT-3는 유료 API를 제공해 이용할 수 있도록 한다고 한다.  
  
BERT와는 다르게 Transformer의 Decoder부분의 일부를 가져와 사용한다.  
확실히 Decoder를 이용하니 BERT에 비해 단어 문장 예측을 잘하고, 챗봇에 많이 이용된다.  
  
Unsupervised pre-training 한 후 Supervised fine-tuning 으로 이루어진다.  
  
라벨링된 데이터가 있다해도 비용이 많이 들고, 그러한 데이터가 대용량으로 구하기 힘들뿐더러, 100% 좋은 성능을 제공해준다고도 장담할 수 없기 때문에 라벨링이 없는 corpus token을 가져오고  
그 이후 각 Task 목적에 맞게 Supervised Fine-tuning을 한다.  
  
BPE을 이용하였다.  
  
(논문 일부 발췌: Fine-tuning에서 업데이트 되는 파라미터 언급 ==> Overall, the only extra parameters we require during fine-tuning are Wy, and embeddings for delimiter tokens)    
(GPT 코드 구현코드를 타 GITHUB를 참고해 STUDY를 했는데.. 기억이 나질 않는다. 추후에 찾으면 출처를 밝히도록 하겠다.)  
  
# 기타 논문
1) 단어 Encoding(Tokenizer)하는 여러 Task 논문  
Efficient Estimation of Word Representations in Vector Space(word2vec): https://arxiv.org/pdf/1301.3781.pdf%C3%AC%E2%80%94%20%C3%AC%E2%80%9E%C5%93  
Neural Machine Translation of Rare Words with Subword Units(BPE): https://arxiv.org/pdf/1508.07909.pdf  
  
(가장 기본적인 논문만 올렸고, BBPE나 WordPiece 등등도 시간되면 공부하는 것을 추천한다.)  


# 
추후 기회가 된다면 GAN과 VIT도 정리해서 올려보겠다.  
