# Deep Learning AMI Developer Guide

-----
*****Copyright &copy; 2019 Amazon Web Services, Inc. and/or its affiliates. All rights reserved.*****

-----
Amazon's trademarks and trade dress may not be used in 
     connection with any product or service that is not Amazon's, 
     in any manner that is likely to cause confusion among customers, 
     or in any manner that disparages or discredits Amazon. All other 
     trademarks not owned by Amazon are the property of their respective
     owners, who may or may not be affiliated with, connected to, or 
     sponsored by Amazon.

-----
## Contents
+ [What Is the AWS Deep Learning AMI?](what-is-dlami.md)
   + [Example DLAMI Uses](examples.md)
   + [Features of the DLAMI](features.md)
+ [Getting Started](gs.md)
   + [Choosing Your DLAMI](options.md)
      + [Deep Learning AMI with Conda](overview-conda.md)
      + [Deep Learning Base AMI](overview-base.md)
      + [CUDA Installations and Framework Bindings](overview-cuda.md)
      + [DLAMI Operating System Options](overview-os.md)
   + [Selecting the Instance Type for DLAMI](instance-select.md)
      + [Recommended GPU Instances](gpu.md)
      + [Recommended CPU Instances](cpu.md)
      + [Pricing for the DLAMI](pricing.md)
+ [Launching and Configuring a DLAMI](launch-config.md)
   + [Step 1: Launch a DLAMI](launch.md)
   + [EC2 Console](launch-from-console.md)
   + [Marketplace Search](launch-from-marketplace.md)
   + [Step 2: Connect to the DLAMI](launch-config-connect.md)
   + [Step 3: Secure Your DLAMI Instance](launch-config-secure.md)
   + [Step 4: Test Your DLAMI](launch-config-test.md)
   + [Clean Up](launch-config-cleanup.md)
   + [Set up a Jupyter Notebook Server](setup-jupyter.md)
      + [Secure Your Jupyter Server](setup-jupyter-config.md)
      + [Start the Jupyter notebook server](setup-jupyter-start-server.md)
      + [Configure the Client to Connect to the Jupyter Server](setup-jupyter-configure-client.md)
         + [Configure a Windows Client](setup-jupyter-configure-client-windows.md)
         + [Configure a Linux or macOS Client](setup-jupyter-configure-client-linux.md)
      + [Test by Logging in to the Jupyter notebook server](setup-jupyter-login.md)
+ [Using a DLAMI](using.md)
   + [Using the Deep Learning AMI with Conda](tutorial-conda.md)
   + [Using the Deep Learning Base AMI](tutorial-base.md)
   + [Running Jupyter Notebook Tutorials](tutorial-jupyter.md)
   + [Tutorials](tutorials.md)
      + [10 Minute Tutorials](tutorial-10min.md)
      + [Activating Frameworks](activating.md)
         + [Apache MXNet (incubating)](tutorial-mxnet.md)
         + [Caffe2](tutorial-caffe2.md)
         + [Chainer](activate-chainer.md)
         + [CNTK](tutorial-cntk.md)
         + [Keras](tutorial-keras.md)
         + [PyTorch](tutorial-pytorch.md)
         + [TensorFlow](tutorial-tensorflow.md)
         + [TensorFlow 2](tutorial-tensorflow-2.md)
         + [TensorFlow with Horovod](activate-horovod.md)
         + [TensorFlow 2 with Horovod](activate-horovod-2.md)
         + [Theano](tutorial-theano.md)
      + [Debugging and Visualization](debugging-and-visualization.md)
         + [MXBoard](tutorial-mxboard.md)
         + [TensorBoard](tutorial-tensorboard.md)
      + [Distributed Training](distributed-training.md)
         + [Chainer](tutorial-chainer.md)
         + [Keras with MXNet](keras-mxnet.md)
         + [TensorFlow with Horovod](tutorial-horovod-tensorflow.md)
      + [Elastic Fabric Adapter](tutorial-efa.md)
         + [Launching a AWS Deep Learning AMI Instance With EFA](tutorial-efa-launching.md)
         + [Using EFA on the DLAMI](tutorial-efa-using.md)
      + [GPU Monitoring and Optimization](tutorial-gpu.md)
         + [Monitoring](tutorial-gpu-monitoring.md)
            + [Monitor GPUs with CloudWatch](tutorial-gpu-monitoring-gpumon.md)
         + [Optimization](tutorial-gpu-opt.md)
            + [Preprocessing](tutorial-gpu-opt-preprocessing.md)
            + [Training](tutorial-gpu-opt-training.md)
      + [The AWS Inferentia Chip With DLAMI](tutorial-inferentia.md)
         + [Launching a DLAMI Instance with AWS Neuron](tutorial-inferentia-launching.md)
         + [Using the DLAMI with AWS Neuron](tutorial-inferentia-using.md)
            + [Using TensorFlow-Neuron and the AWS Neuron Compiler](tutorial-inferentia-tf-neuron.md)
            + [Using AWS Neuron TensorFlow Serving](tutorial-inferentia-tf-neuron-serving.md)
            + [Using MXNet-Neuron and the AWS Neuron Compiler](tutorial-inferentia-mxnet-neuron.md)
            + [Using MXNet-Neuron Model Serving](tutorial-inferentia-mxnet-neuron-serving.md)
      + [Inference](tutorial-inference.md)
         + [Use Apache MXNet for Inference with an ONNX Model](tutorial-mxnet-inference-onnx.md)
         + [Use Apache MXNet for Inference with a ResNet 50 Model](tutorial-mxnet-inference-resnet50.md)
         + [Use CNTK for Inference with an ONNX Model](tutorial-cntk-inference-onnx.md)
      + [Using Frameworks with ONNX](onnx.md)
         + [Apache MXNet to ONNX to CNTK Tutorial](tutorial-onnx-mxnet-cntk.md)
         + [Chainer to ONNX to CNTK Tutorial](tutorial-onnx-chainer-cntk.md)
         + [Chainer to ONNX to MXNet Tutorial](tutorial-onnx-chainer-mxnet.md)
         + [PyTorch to ONNX to CNTK Tutorial](tutorial-onnx-pytorch-cntk.md)
         + [PyTorch to ONNX to MXNet Tutorial](tutorial-onnx-pytorch-mxnet.md)
      + [Model Serving](model-serving.md)
         + [Model Server for Apache MXNet (MMS)](tutorial-mms.md)
         + [TensorFlow Serving](tutorial-tfserving.md)
+ [What Are AWS Deep Learning Containers?](deep-learning-containers.md)
   + [AWS Deep Learning Containers on Amazon EC2](deep-learning-containers-ec2.md)
      + [Setup](deep-learning-containers-ec2-setup.md)
      + [Tutorials](deep-learning-containers-ec2-tutorials.md)
         + [Training](deep-learning-containers-ec2-tutorials-training.md)
         + [Inference](deep-learning-containers-ec2-tutorials-inference.md)
         + [Custom Entrypoints](deep-learning-containers-ec2-tutorials-custom-entry.md)
   + [AWS Deep Learning Containers on Amazon ECS](deep-learning-containers-ecs.md)
      + [Setup](deep-learning-containers-ecs-setup.md)
         + [Prerequisites](deep-learning-containers-ecs-setup-prerequisites.md)
         + [Setting Up Amazon ECS for AWS Deep Learning Containers](deep-learning-containers-ecs-setting-up-ecs.md)
      + [Tutorials](deep-learning-containers-ecs-tutorials.md)
         + [Training](deep-learning-containers-ecs-tutorials-training.md)
         + [Inference](deep-learning-containers-ecs-tutorials-inference.md)
         + [Custom Entrypoints](deep-learning-containers-ecs-tutorials-custom-entry.md)
   + [AWS Deep Learning Containers on Amazon EKS](deep-learning-containers-eks.md)
      + [Setup](deep-learning-containers-eks-setup.md)
      + [Tutorials](deep-learning-containers-eks-tutorials.md)
         + [Training](deep-learning-containers-eks-tutorials-training.md)
            + [CPU Training](deep-learning-containers-eks-tutorials-cpu-training.md)
            + [GPU Training](deep-learning-containers-eks-tutorials-gpu-training.md)
            + [Distributed GPU Training](deep-learning-containers-eks-tutorials-distributed-gpu-training.md)
         + [Inference](deep-learning-containers-eks-tutorials-inference.md)
            + [CPU Inference](deep-learning-containers-eks-tutorials-cpu-inference.md)
            + [GPU Inference](deep-learning-containers-eks-tutorials-gpu-inference.md)
         + [Custom Entrypoints](deep-learning-containers-eks-tutorials-custom-entry.md)
      + [Troubleshooting AWS Deep Learning Containers on EKS](deep-learning-containers-eks-troubleshooting.md)
      + [AWS Deep Learning Containers on EKS Glossary](deep-learning-containers-eks-glossary.md)
   + [AWS Deep Learning Containers on Amazon SageMaker](deep-learning-containers-sagemaker.md)
   + [Appendix](deep-learning-containers-appendix.md)
      + [Deep Learning Containers Images](deep-learning-containers-images.md)
      + [AWS Deep Learning Containers Custom Images](deep-learning-containers-custom-images.md)
      + [AWS Deep Learning Containers MKL Recommendations](deep-learning-containers-mkl.md)
+ [Upgrading Your DLAMI](upgrading.md)
   + [Upgrading to a New DLAMI Version](upgrading-dlami.md)
   + [Tips for Software Updates](updating-software.md)
+ [Resources and Support](resources.md)
+ [Appendix](appendix.md)
   + [AMI Options](ami-options.md)
      + [Deep Learning AMI with Conda Options](conda.md)
      + [Deep Learning Base AMI Options](base.md)
      + [Deep Learning AMI with CUDA 10.1 Options](cuda10-1.md)
      + [Deep Learning AMI with CUDA 10 Options](cuda10.md)
      + [Deep Learning AMI with CUDA 9 Options](cuda9.md)
      + [Deep Learning AMI with CUDA 8 Options](cuda8.md)
      + [AWS Deep Learning AMI, Ubuntu 18.04 Options](ubuntu18-04.md)
      + [AWS Deep Learning AMI, Ubuntu 16.04 Options](ubuntu.md)
      + [AWS Deep Learning AMI Amazon Linux Options](al.md)
      + [AWS Deep Learning AMI Amazon Linux 2 Options](al2.md)
      + [AWS Deep Learning AMI, Windows Options](win.md)
   + [DLAMI: Release Notes](appendix-ami-release-notes.md)
      + [AWS Deep Learning AMI Release Archive](dlami-release-archive.md)
         + [AWS Deep Learning AMI Base Release Archive](dlami-release-archive-base.md)
            + [Release Note Details for Deep Learning Base AMI (Amazon Linux) Version 2.0](dlami-base-amazon-linux-latest.md)
            + [Release Note Details for Version 2.0](dlami-base-ubuntu-latest.md)
            + [Release Note Details for Deep Learning Base AMI (Amazon Linux) Version 1.0](BASE_AML1.md)
            + [Release Note Details for Version 1.0](BASE_UBUNTU1.md)
         + [AWS Deep Learning AMI Conda Release Archive](dlami-release-archive-conda.md)
            + [Release Note Details for Deep Learning AMI (Amazon Linux) Version 2.0](dlami-conda-amazon-linux-latest.md)
            + [Release Note Details for Version 2.0](dlami-conda-ubuntu-latest.md)
            + [Release Note Details for Deep Learning AMI (Amazon Linux) Version 1.0](CONDA_AML1.md)
            + [Release Note Details for Version 1.0](CONDA_UBUNTU1.md)
         + [AWS Deep Learning AMI Source Release Archive](dlami-release-archive-source.md)
            + [Version: 2.0](dlami-source-ubuntu-latest.md)
            + [Deep Learning AMI Ubuntu Version: 2.4_Oct2017](Ubuntu2.4_Oct2017.md)
            + [Ubuntu DLAMI Release Archive](dlami-release-archive-ubuntu.md)
               + [Deep Learning CUDA 9 AMI Ubuntu Version: 1.0](CUDA9_Ubuntu1.md)
               + [Deep Learning AMI Ubuntu Version: 2.3_Sep2017](Ubuntu2.3_Sep2017.md)
               + [Deep Learning AMI Ubuntu Version: 2.2_August2017](Ubuntu2_2_August2017.md)
               + [Deep Learning AMI Ubuntu Version: 1.5_June2017](Ubuntu1_5_June2017.md)
               + [Deep Learning AMI Ubuntu Version: 1.4_June2017](Ubuntu1_4_June2017.md)
               + [Deep Learning AMI Ubuntu Version: 1.3_Apr2017](Ubuntu1_3_Apr2017.md)
               + [Deep Learning AMI Ubuntu Version: 1.2](Ubuntu1_2.md)
               + [Deep Learning AMI Ubuntu Version: 1.1](Ubuntu1_1.md)
               + [Deep Learning AMI Ubuntu Version: 1.0](Ubuntu1_0.md)
            + [Amazon Linux DLAMI Release Archive](dlami-release-archive-al.md)
               + [Version: 2.0](dlami-source-amazon-linux-latest.md)
               + [Deep Learning AMI Amazon Linux Version: 3.3_Oct2017](AML3.3_Oct2017.md)
               + [Deep Learning CUDA 9 AMI Amazon Linux Version: 1.0](CUDA9_AML1.md)
               + [Deep Learning AMI Amazon Linux Version: 3.1_Sep2017](AML3.1_Sep2017.md)
               + [Deep Learning AMI Amazon Linux Version: 2.3_June2017](AML2_3_June2017.md)
               + [Deep Learning AMI Amazon Linux Version: 2.2_June2017](AML2_2_June2017.md)
               + [Deep Learning AMI Amazon Linux Version: 2.1_Apr2017](AML2_1_Apr2017.md)
               + [Deep Learning AMI Amazon Linux Version: 2.0](AML2_0.md)
               + [Deep Learning AMI Amazon Linux Version: 1.5](AML1_5.md)
         + [AWS Deep Learning AMI Windows Release Archive](dlami-release-archive-windows.md)
            + [Release Note Details for Deep Learning AMI (Windows 2016) Version 1.0](WIN_2016.md)
            + [Release Note Details for Deep Learning AMI (Windows 2012 R2) Version 1.0](WIN_2012.md)
+ [Document History for AWS Deep Learning AMI Developer Guide](doc-history.md)
+ [AWS Glossary](glossary.md)