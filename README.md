# Fin_Text_Analysis_ML
Train the financial words with BERT or Transformer
Source Code: https://github.com/sinjorjob/chABSA-dataset

1. Environment Setting
1.1 summary
MacOS
Anaconda3
Python 3.6.13 |Anaconda, Inc.| (default, Feb 23 2021, 12:58:59) [GCC Clang 10.0.0 ] on darwin
pytorch-pretrained-BERT (Kyoto University: https://nlp.ist.i.kyoto-u.ac.jp/index.php?ku_bert_japanese)
Juman++ v2.0.0-rc2 
Pytorch


1.2 operation instrument

1.2.1 virtual environment

terminal --> 
if your conda hasn't been added to base, please try: echo 'export PATH="/Users/anaconda3/bin:$PATH"' >> ~/.zshrc 
[other conda command you could see from: https://github.com/Cyndi-Tokyotech/conda-env/blob/main/command)]
check: conda --version 
build a virtual environment: conda create -n pytorch python=3.6 
use the new environment: conda activate pytorch
setteing the pytorch environment:
conda install pytorch=0.4 torchvision -c pytorch
conda install pytorch=0.4 torchvision cudatoolkit -c pytorch
conda install pandas jupyter matplotlib scipy scikit-learn pillow tqdm cython

1.2.2 Juman++
#MacOS
$ brew install jumanpp
$ jumanpp -v  # 確認
JUMAN++ 1.02
pip install pyknp
#Ubuntu Linux
# jumanpp-2.0.0-rc3 download
wget https://github.com/ku-nlp/jumanpp/releases/download/v2.0.0-rc3/jumanpp-2.0.0-rc3.tar.xz
# unzip a file
tar xvf jumanpp-2.0.0-rc3.tar.xz
cd jumanpp-2.0.0-rc3/
mkdir build
cd build/
cmake .. -DCMAKE_BUILD_TYPE=Release -DCMAKE_INSTALL_PREFIX=/usr/local
make
sudo make install

To check if it is ready, you can try: echo すももももももももももも | jumanpp

1.2.3 BERT_Pretrained
download from: http://nlp.ist.i.kyoto-u.ac.jp/index.php?BERT%E6%97%A5%E6%9C%AC%E8%AA%9EPretrained%E3%83%A2%E3%83%87%E3%83%AB
bert_config.json: setting the parameter
pytorch_model.bin: pytorch pretrained BERT model
vocab.txt: BERT vocabary
