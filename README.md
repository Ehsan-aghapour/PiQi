# PiQi Framework: Partially Quantized Inference

PiQi is an integrated framework designed for partially quantized Deep Neural Network (DNN) inference on Heterogeneous Multi-Processor Systems on Chip (HMPSoCs) featuring CPU clusters, GPU, and NPU (Deep Learning Accelerators). This framework incorporates several submodules, each providing specific functionalities to implement and run partially quantized DNNs effectively.

## Submodules

### ARM-COUP
The **ARM-COUP** submodule is responsible for mapping DNN layers onto various processors, including the CPU (big and little clusters), GPU, and NPU (Neural Processing Unit). This submodule facilitates partial quantization with user-defined configurations, allowing you to map layers and set other parameters. Additionally, it profiles the execution time and power consumption at the granularity of individual DNN layers.

### CO-UP-Profiling
The **CO-UP-Profiling** submodule enables profiling of execution time, power consumption, and energy consumption for DNNs. Profiling can be conducted on each processor individually or according to a user-specified configuration, such as mapping specific layers to designated processors. This submodule also contains a multi-objective Genetic Algorithm (GA) for design space exploration. The search algorithm evaluates configurations through profiling, either via real execution on a development board or through modeling based on profiling data.

### YoloV3-QE
The **YoloV3-QE** submodule is focused on the YoloV3 model, with two primary components: Quantization and Evaluation. The Quantization component allows for the partial quantization of selected layers and saves the model using TensorFlow and Keras. The Evaluation component assesses the accuracy of the saved partially quantized model using either GPU or multi-threaded CPU on the COCO dataset. This submodule also includes models for predicting the accuracy of a given partial quantization configuration.
