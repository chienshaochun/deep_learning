# 第一題:

首先嘗試使用 CNN 的 model，但效率奇差，改成使用 DNN。接著嘗試 hot-one 編碼、調整 `learning_rate`、`batch_size`、`loss_function`、`accuracy_function`。但都無法表現出太好的 accuracy，
所以嘗試使用 VGG 來進行實作，accuracy 很高，但是 VGG16 本身有點大所以進行一次訓練要跑很久，所以改成嘗試使用 ResNet，在同樣的條件之下 ResNet 表現出比 DNN 的 model 好很多的 accuracy。
其中最麻煩的部分有兩個，第一是如何調整模型，第二是因為我是使用 colab 進行訓練所以偶爾會有 disconnect 的情況發生，
所以折衷的方式是使用 checkpoint 紀錄 accuracy 最高的模型，下次直接從這個模型開始訓練這樣起碼 Epoch 數量可以少一點。


# 第二題:

爬山演算法還算簡單，基本上只要在網路上找到相對應的程式碼就可以套上，基因演算法則複雜許多，需要理解一下其中的人口還有突變所代表的含意，但基本上也是可以套用程式碼。

