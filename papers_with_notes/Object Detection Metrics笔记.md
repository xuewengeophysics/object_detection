# Object Detection Metrics笔记

+ Code: [rafaelpadilla/Object-Detection-Metrics](rafaelpadilla/Object-Detection-Metrics)
+ Code: [rafaelpadilla/review_object_detection_metrics](rafaelpadilla/review_object_detection_metrics)
+ Blog: [目标检测中的mAP是什么含义？](https://www.zhihu.com/question/53405779)

## Important definitions

### Intersection Over Union (IOU)

+ 交并比

### True Positive, False Positive, False Negative and True Negative

+ **True Positive (TP)**: A correct detection. Detection with IOU ≥ *threshold*
+ **False Positive (FP)**: A wrong detection. Detection with IOU < *threshold*
+ **False Negative (FN)**: A ground truth not detected
+ **True Negative (TN)**: Does not apply. It would represent a corrected misdetection. In the object detection task there are many possible bounding boxes that should not be detected within an image. Thus, TN would be all possible bounding boxes that were corrrectly not detected (so many possible boxes within an image). That's why it is not used by the metrics.

### Precision

+ Precision is the ability of a model to identify **only** the relevant objects: `TP / (TP + FP) = TP / all detections`.

### Recall

+ Recall is the ability of a model to find all the relevant cases (all ground truth bounding boxes): `TP / (TP + FN) = TP / all ground truths`.

## Metrics

### Precision x Recall curve

+ good detector: precision stays high as recall increases,

### AP

+ 计算某一类 P-R 曲线下的面积

### mAP

+ 计算所有类别 P-R 曲线下面积的平均值

