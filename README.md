# bnn-sdsoc

- This repo is copyed from https://github.com/cornell-zhang/bnn-fpga

```
  @article{zhao-bnn-fpga2017,
    title   = "{Accelerating Binarized Convolutional Neural Networks
              with Software-Programmable FPGAs}",
    author  = {Ritchie Zhao and Weinan Song and Wentao Zhang and Tianwei Xing and
               Jeng-Hau Lin and Mani Srivastava and Rajesh Gupta and Zhiru Zhang},
    journal = {Int'l Symp. on Field-Programmable Gate Arrays (FPGA)},
    month   = {Feb},
    year    = {2017},
  }
```    

***

#### Execution Result

```bash
root@z7_20:/run/media/mmcblk0p1# export CRAFT_BNN_ROOT=`pwd`
root@z7_20:/run/media/mmcblk0p1# ./bnn-fpga.elf 1
* WT_WORDS   = 4682
* KH_WORDS   = 64
## Loading input data ##
## Loading parameters ##
>> (Wt, KH) batch: (10924 256)
>> Final batch: 128
>> (Wt, KH) batch: (256 256)
>> Final batch: 128
>> (Wt, KH) batch: (256 256)
>> Final batch: 256
>> (Wt, KH) batch: (128 256)
>> Final batch: 128
>> (Wt, KH) batch: (128 256)
>> Final batch: 128
>> (Wt, KH) batch: (64 256)
>> Final batch: 64
>> (Wt, KH) bits batch: (36 256)
>> Final bits batch: 32
>> (Wt, KH) bits batch: (292 256)
>> Final bits batch: 256
>> (Wt, KH) bits batch: (292 256)
>> Final bits batch: 10
## Running BNN for 1 images
  Pred/Label:    3/ 3   [ OK ]

Errors: 0 (0.00%)

Total accel runtime =     0.0139 seconds

xl-Conv1            :      1 calls;  0.133 msecs total time
xl-Conv2            :      1 calls;  0.001 secs total time
xl-Conv3            :      1 calls;  0.002 secs total time
xl-Conv4            :      2 calls;  0.002 secs total time
xl-Conv5            :      4 calls;  0.002 secs total time
xl-Conv6            :      8 calls;  0.003 secs total time
xl-FC1              :     32 calls;  0.002 secs total time
xl-FC2              :      4 calls;  0.229 msecs total time
xl-FC3              :      1 calls;  0.065 msecs total time
```
