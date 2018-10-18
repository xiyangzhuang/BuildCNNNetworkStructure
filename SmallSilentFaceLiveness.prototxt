
name: "SmallSilentFaceLiveness"
#####ap_6_bn_net#####
layer {  
  name: "data"  
  type: "Data"  
  top: "data"  
  top: "label"  
  data_param {  
    source: "./"  
    backend: LMDB  
    batch_size: 16
  }  
  transform_param {  
    scale: 0.00390625  
  }  
  include: { phase: TRAIN }  
}  
layer {  
  name: "data"  
  type: "Data"  
  top: "data"  
  top: "label"  
  data_param {  
    source: "./"
    backend: LMDB  
    batch_size: 8  
  }  
  transform_param {  
    scale: 0.00390625  
  }  
  include: { phase: TEST }  
}
###################
  
layer {  
  name: "conv1"  
  type: "Convolution"  
  bottom: "data"  
  top: "conv1"  
  param {  
    lr_mult: 1  
  }  
  param {  
    lr_mult: 2
  }  
  convolution_param {  
    num_output: 32  
    kernel_size: 3  
    stride: 1  
    weight_filler {  
      type: "xavier"  
    }  
    bias_filler {  
      type: "constant"  
    }  
  }  
}
  
layer {  
  bottom: "conv1"  
  top: "conv1"  
  name: "bn_conv1"  
  type: "BatchNorm"  
  param {  
    lr_mult: 0  
    decay_mult: 0  
  }   
  param {  
    lr_mult: 0  
    decay_mult: 0  
  }  
  param {  
    lr_mult: 0  
    decay_mult: 0  
  }  
}  
layer {  
  bottom: "conv1"  
  top: "conv1"  
  name: "scale_conv1"  
  type: "Scale"  
  scale_param {  
    bias_term: true  
  }  
}
layer {
  bottom: "conv1"
  top: "conv1"
  name: "relu1"
  type: "ReLU"
}

layer {  
  name: "conv2"  
  type: "Convolution"  
  bottom: "conv1"  
  top: "conv2"  
  param {  
    lr_mult: 1  
  }  
  param {  
    lr_mult: 2
  }  
  convolution_param {  
    num_output: 12  
    kernel_size: 3  
    stride: 1  
    weight_filler {  
      type: "xavier"  
    }  
    bias_filler {  
      type: "constant"  
    }  
  }  
}  
layer {  
  bottom: "conv2"  
  top: "conv2"  
  name: "bn_conv2"  
  type: "BatchNorm"  
  param {  
    lr_mult: 0  
    decay_mult: 0  
  }   
  param {  
    lr_mult: 0  
    decay_mult: 0  
  }  
  param {  
    lr_mult: 0  
    decay_mult: 0  
  }  
}  
layer {  
  bottom: "conv2"  
  top: "conv2"  
  name: "scale_conv2"  
  type: "Scale"  
  scale_param {  
    bias_term: true  
  }  
}

layer {
  bottom: "conv2"
  top: "conv2"
  name: "relu2"
  type: "ReLU"
}

layer {  
  name: "pool1"  
  type: "Pooling"  
  bottom: "conv2"  
  top: "pool1"  
  pooling_param {  
    pool: MAX  
    kernel_size: 2  
    stride: 2  
  }  
}   

################

layer {  
  name: "conv3"  
  type: "Convolution"  
  bottom: "pool1"  
  top: "conv3"  
  param {  
    lr_mult: 1  
  }  
  param {  
    lr_mult: 2
  }  
  convolution_param {  
    num_output: 24
    kernel_size: 3  
    stride: 1  
    weight_filler {  
      type: "xavier"  
    }  
    bias_filler {  
      type: "constant"  
    }  
  }  
}
  
layer {  
  bottom: "conv3"  
  top: "conv3"  
  name: "bn_conv3"  
  type: "BatchNorm"  
  param {  
    lr_mult: 0  
    decay_mult: 0  
  }   
  param {  
    lr_mult: 0  
    decay_mult: 0  
  }  
  param {  
    lr_mult: 0  
    decay_mult: 0  
  }  
}  
layer {  
  bottom: "conv3"  
  top: "conv3"  
  name: "scale_conv3"  
  type: "Scale"  
  scale_param {  
    bias_term: true  
  }  
}
layer {
  bottom: "conv3"
  top: "conv3"
  name: "relu3"
  type: "ReLU"
}

layer {  
  name: "conv4"  
  type: "Convolution"  
  bottom: "conv3"  
  top: "conv4"  
  param {  
    lr_mult: 1  
  }  
  param {  
    lr_mult: 2
  }  
  convolution_param {  
    num_output: 24
    kernel_size: 3  
    stride: 1  
    weight_filler {  
      type: "xavier"  
    }  
    bias_filler {  
      type: "constant"  
    }  
  }  
}  
layer {  
  bottom: "conv4"  
  top: "conv4"  
  name: "bn_conv4"  
  type: "BatchNorm"  
  param {  
    lr_mult: 0  
    decay_mult: 0  
  }   
  param {  
    lr_mult: 0  
    decay_mult: 0  
  }  
  param {  
    lr_mult: 0  
    decay_mult: 0  
  }  
}  
layer {  
  bottom: "conv4"  
  top: "conv4"  
  name: "scale_conv4"  
  type: "Scale"  
  scale_param {  
    bias_term: true  
  }  
}

layer {
  bottom: "conv4"
  top: "conv4"
  name: "relu4"
  type: "ReLU"
}

layer {  
  name: "pool2"  
  type: "Pooling"  
  bottom: "conv4"  
  top: "pool2"  
  pooling_param {  
    pool: MAX  
    kernel_size: 2  
    stride: 2  
  }  
}   
################

layer {  
  name: "conv5"  
  type: "Convolution"  
  bottom: "pool2"  
  top: "conv5"  
  param {  
    lr_mult: 1  
  }  
  param {  
    lr_mult: 2
  }  
  convolution_param {  
    num_output: 48  
    kernel_size: 3  
    stride: 1  
    weight_filler {  
      type: "xavier"  
    }  
    bias_filler {  
      type: "constant"  
    }  
  }  
}
  
layer {  
  bottom: "conv5"  
  top: "conv5"  
  name: "bn_conv5"  
  type: "BatchNorm"  
  param {  
    lr_mult: 0  
    decay_mult: 0  
  }   
  param {  
    lr_mult: 0  
    decay_mult: 0  
  }  
  param {  
    lr_mult: 0  
    decay_mult: 0  
  }  
}  
layer {  
  bottom: "conv5"  
  top: "conv5"  
  name: "scale_conv5"  
  type: "Scale"  
  scale_param {  
    bias_term: true  
  }  
}
layer {
  bottom: "conv5"
  top: "conv5"
  name: "relu5"
  type: "ReLU"
}

layer {  
  name: "conv6"  
  type: "Convolution"  
  bottom: "conv5"  
  top: "conv6"  
  param {  
    lr_mult: 1  
  }  
  param {  
    lr_mult: 2
  }  
  convolution_param {  
    num_output: 48  
    kernel_size: 3  
    stride: 1  
    weight_filler {  
      type: "xavier"  
    }  
    bias_filler {  
      type: "constant"  
    }  
  }  
}  
layer {  
  bottom: "conv6"  
  top: "conv6"  
  name: "bn_conv6"  
  type: "BatchNorm"  
  param {  
    lr_mult: 0  
    decay_mult: 0  
  }   
  param {  
    lr_mult: 0  
    decay_mult: 0  
  }  
  param {  
    lr_mult: 0  
    decay_mult: 0  
  }  
}  
layer {  
  bottom: "conv6"  
  top: "conv6"  
  name: "scale_conv6"  
  type: "Scale"  
  scale_param {  
    bias_term: true  
  }  
}

layer {
  bottom: "conv6"
  top: "conv6"
  name: "relu6"
  type: "ReLU"
}

layer {  
  name: "pool3"  
  type: "Pooling"  
  bottom: "conv6"  
  top: "pool3"  
  pooling_param {  
    pool: MAX  
    kernel_size: 2  
    stride: 2  
  }  
}
   
################


layer {
  name: "pool4"
  type: "Pooling"
  bottom: "pool3"
  top: "pool4"
  pooling_param {
    pool: AVE
    kernel_size: 2
    stride: 2
  }
}  

layer {  
  name: "ip2"  
  type: "InnerProduct"  
  bottom: "pool4"  
  top: "ip2"  
  param {  
    lr_mult: 1  
  }  
  param {  
    lr_mult: 2  
  }  
  inner_product_param {  
    num_output: 2  
    weight_filler {  
      type: "xavier"  
    }  
    bias_filler {  
      type: "constant"  
    }  
  }  
}  
layer {  
  name: "accuracy"  
  type: "Accuracy"  
  bottom: "ip2"  
  bottom: "label"  
  top: "accuracy"  
  include {  
    phase: TEST  
  }  
}  
layer {  
  name: "loss"  
  type: "SoftmaxWithLoss"  
  bottom: "ip2"  
  bottom: "label"  
  top: "loss"  
}  
