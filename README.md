# Neural Machine Translation for Hindi

This is an implementation that builds a customised Hindi translation model following the tutorial from https://github.com/tensorflow/nmt

The dataset is obtained from HindiEnCorp 1.0 from http://www.statmt.org/wmt14/ and formatted to input data format to the nmt model.

To run the model, simple download the database and use the commands:
python -m nmt.nmt \
    --src=hi --tgt=en \
    --vocab_prefix=./data_hi/vocab \
    --train_prefix=./data_hi/train \
    --dev_prefix=./data_hi/dev  \
    --test_prefix=./data_hi/test \
    --out_dir=./tmp/nmt_model_hi \
    --num_train_steps=12000 \
    --steps_per_stats=100 \
    --num_layers=2 \
    --num_units=128 \
    --dropout=0.2 \
    --metrics=bleu

This naive training can get Bleu score of 10, further tuning is needed.