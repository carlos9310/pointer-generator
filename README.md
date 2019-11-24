# pointer-generator

## DataSet
参考[https://github.com/abisee/cnn-dailymail](https://github.com/abisee/cnn-dailymail)

raw corpus 

- [cnn_stories.tgz](https://pan.baidu.com/s/13SDS_UwoRKP6jF1NjRlUCg)

- [dailymail_stories.tgz](https://pan.baidu.com/s/1bJTG90Wr_KUmZa4d_GeAeA)


command for data preprocessing
```
python data/make_datafiles.py /path/to/unzipped/cnn_stories.tgz /path/to/unzipped/dailymail_stories.tgz
```


## Code with python3
参考[https://github.com/abisee/pointer-generator](https://github.com/abisee/pointer-generator)

### Run training

```
python run_summarization.py --mode=train --data_path=/path/to/chunked/train_* --vocab_path=/path/to/vocab --log_root=/path/to/a/log/directory --exp_name=myexperiment
```

### Run eval

```
python run_summarization.py --mode=eval --data_path=/path/to/chunked/val_* --vocab_path=/path/to/vocab --log_root=/path/to/a/log/directory --exp_name=myexperiment
```

### Run beam search decoding

```
python run_summarization.py --mode=decode --data_path=/path/to/chunked/val_* --vocab_path=/path/to/vocab --log_root=/path/to/a/log/directory --exp_name=myexperiment
```
