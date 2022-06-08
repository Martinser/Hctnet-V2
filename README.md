# Hctnet-V2: Deeper integration of Convs and MSAs

Hctnet忽略Convs和MSAs不同模块连接处的处理，并且Convs的感受野通常是固定且较小，很难为MSAs提供更大感受野的特征图,同时融合后的特征图需要在多维度上进行自适应调整和特征交互。
在Hctnet的基础上，提出了在更深层次上融合Convs和MSAs的混合网络Hctnet V2。它把Convs和MSAs做并行处理，同时对Convs进行重参数化来获得更大的感受野，然后输入至注意力模块中在多维度上对不同特征图连接后的结果进行自适应调整，最后把所得特征图输入到混合MLP模块中，对不同的channel和tokens进行特征交互，使得肺炎图像检测准确率从95.35%提升到了97.12%。

## Catalog
- [ ] Fine-tuning Code
- [ ] Fine-tune on Chest X-Ray Images with Weights
