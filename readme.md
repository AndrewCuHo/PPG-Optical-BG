Code is available after the publication

## Overall video PPG processing methods:
1. Directly, Pooling the spatial sequence i.e. frames, obtain R -> RGBYUV
2. Learnable, 3D CNN processing the frames, but time-cosuming and redundant
3. Inspired by optical-flow with 2D CNN, Two-stream
## Reconstruct PPG
1.  R channel -> R,G,B,Y,U,V channels -> The limitation of simply apply meaning operation to fingertip video.
2.	Must temporal and spatial combination -> Inspired from optical flowing (1D LSTM) + 2D CNN (Frequency) ->
3.	channel squeeze (CHZ-Net)

