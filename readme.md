Code is available after the publication

## Overall video PPG processing methods:
1. Directly, Pooling the spatial sequence i.e. frames, obtain R -> RGBYUV
2. Learnable, 3D CNN processing the frames, but time-cosuming and redundant
3. Inspired by optical-flow with 2D CNN, Two-stream
## Reconstruct PPG
1.  R channel -> R,G,B,Y,U,V channels -> The limitation of simply apply meaning operation to fingertip video.
2.	Must temporal and spatial combination -> Inspired from optical flowing (1D LSTM) + 2D CNN (Frequency) ->
3.	channel squeeze (CHZ-Net)

Do not consider the time-consuming.
Optical flow or feature vector or RGB difference (using HOG?).

## Model
3.  Add LSTM gate like for Two-Stream -> connection like U-net
4.  Complete One Stream, How to  add the optical wave stream ?

7.  Autoformer 引入信号相关求seasonal相关性,算成score的形式，衡量Mask的ratio大小（自适应）
9.  或者用transformer token合并方式做特征融合
Temporal Fusion Transformers 分成3段， 按照backbone的高低频+一个辅助段落做 supervised contrastive learning, 阈值判断怎么插入(用方差) RNN Gate
