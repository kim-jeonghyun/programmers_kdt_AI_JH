Word2Vec을 사용해 subword 임베딩을 학습해 보는 과제입니다.
단어가 아닌 subword 단위라는 것에 주의하시기 바랍니다.
그리고 Skip-gram 모델을 사용하도록 합니다.
말뭉치는 다음 파일을 사용합니다. https://storage.googleapis.com/download.tensorflow.org/data/shakespeare.txt

Subword tokenization은 따로 구현하지 말고 SentencePiece(https://github.com/google/sentencepiece)에 포함된 BPE를 사용하세요.

다음 두 가지 경우를 따로 학습해 보세요.
Negative sampling을 사용해서 임베딩을 학습합니다. 단, 단어 단위가 아닌 subword에 대한 임베딩을 학습하세요. 일반적인 구현은 다음을 참조하세요. https://www.tensorflow.org/tutorials/text/word2vec

Negative sampling을 사용하지 말고, skip-gram을 Cross entropy loss(https://www.tensorflow.org/api_docs/python/tf/keras/losses/SparseCategoricalCrossentropy)를 사용하여 multi-class classification문제로 풀어보세요. 필요하다면(모델학습이 매우 느린 경우에) SentencePiece에서 모델을 학습시 vocabulary size를 제한할 수 있습니다.
