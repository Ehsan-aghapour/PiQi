# PiQi Framework: Partially Quantizatied Inference

This is an integrated framework, for partially quantized DNN inference on HMPSoCs with CPU clusters, GPU and NPU (Deep learning accelerators).

It concludes several repositories as sobmodules for implementing and running.

## ARM-COUP
This sobmodule is for mapping DNN layers into desired processors among, CPU big cluster, CPU little cluster, GPU and NPU (Neural Processing Unit). This framework provides running the partial quantization with desired configuration (mapping and other configurations), and profile the execution time and power consumption at the granularity of DNN layers. 

##YoloV3-QE
