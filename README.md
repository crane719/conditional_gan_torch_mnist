# conditional_gan_torch_mnist
mnistを学習するconditional GAN. pytorchを用いている.  

## usage
### training
1. pythonのinstall  
2. packageのinstall  
```
pip install -r requirements.txt
```
3. training  
```
python train.py
```
4. 結果の確認  
学習終了後, ディレクトリ内にresultフォルダが作成されているため確認

### attention
mnistが存在しない場合, downloadを行うため, ネット環境が必要  

## abstract
### GAN
GAN(Generative Adversarial network)は生成モデルと識別モデルから成る.  
- Disctiminator(識別モデル)  
入力されるサンプルが生成モデルの分布から来たものか, 実際のデータ分布から来たものかを識別できるように学習する.  
- Generator(生成モデル)  
識別モデルに贋作と見破られないサンプルを生成するように学習を行う. 乱数からサンプルを生成する.  

### conditional GAN
conditional GANは学習する際に, サンプルにラベルを与える(mnistであれば, サンプルの数字がなんであるか与える).  
与え方はいくつかある. 今回はone-hotでサンプルにcatしている.  
![conditional](https://user-images.githubusercontent.com/54930418/74590954-c1612480-5056-11ea-96b3-9fe6a28f8917.png)

## training result example
### 学習過程
- 1epoch  
![1](https://user-images.githubusercontent.com/54930418/74590957-caea8c80-5056-11ea-8033-5fcb871f3e11.png)

- 10epoch  
![10](https://user-images.githubusercontent.com/54930418/74590959-d1790400-5056-11ea-9e9c-7449d95f3dbf.png)

- 50epoch  
![50](https://user-images.githubusercontent.com/54930418/74590961-d50c8b00-5056-11ea-852f-80455373e7e5.png)

![index1](https://user-images.githubusercontent.com/54930418/74591023-84e1f880-5057-11ea-8628-472c9ed76a5d.gif)
