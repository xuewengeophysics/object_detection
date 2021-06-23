# Dynamic Head Unifying Object Detection Heads with Attentions笔记





improves the representation ability of object detection heads



what

+ dynamic head framework to unify object detection heads with attentions, unify scale-awareness, spatial-awareness, and task-awareness all together



how

+ deploy attention mechanisms separately on each particular dimension of features, i.e., level-wise, spatial-wise, and channel-wise
  + level-wise: scale-aware attention. It learns the relative importance of various semantic levels to enhance the feature at a proper level for an individual object based on its scale.
  + spatial-wise: spatial-awareness attention. It learns coherently discriminative representations in spatial locations.
  + channel-wise: task-aware attention. It directs different feature channels to favor different tasks separately (e.g., classification, box regression,
    and center/key-point learning.) based on different convolutional kernel responses from objects.



future work

+ how to make the full attention model easy to learn and efficient to compute
+ how to systematically consider more modalities of attentions into the head designing for better performance