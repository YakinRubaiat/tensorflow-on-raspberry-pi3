## Install Tensorflow on raspberry pi 3 

Thanks for contribution : Gunjan Yadav,zulfikar ali zehan

>Today i am going to show you how to install tensorflow on raspberry pi 3b :

>My System details :

```sh
$ sudo cat /proc/cpuinfo
```

>Operating system: Noobs.

>processor	: 0

>model name	: ARMv7 Processor rev 4 (v7l)

>BogoMIPS	: 38.40

>Features	: half thumb fastmult vfp edsp neon vfpv3 tls vfpv4 idiva idivt vfpd32 lpae evtstrm crc32 

>CPU implementer	: 0x41

>CPU architecture: 7

>CPU variant	: 0x0

>CPU part	: 0xd03

>CPU revision	: 4

>processor	: 1

>model name	: ARMv7 Processor rev 4 (v7l)

>BogoMIPS	: 38.40

>Features	: half thumb fastmult vfp edsp neon vfpv3 tls vfpv4 idiva idivt vfpd32 lpae evtstrm crc32

>CPU implementer	: 0x41

>CPU architecture: 7

>CPU variant	: 0x0

>CPU part	: 0xd03

>CPU revision	: 4

>processor	: 2

>model name	: ARMv7 Processor rev 4 (v7l)

>BogoMIPS	: 38.40

>Features	: half thumb fastmult vfp edsp neon vfpv3 tls vfpv4 idiva idivt vfpd32 lpae evtstrm crc32 

>CPU implementer	: 0x41

>CPU architecture: 7

>CPU variant	: 0x0

>CPU part	: 0xd03

>CPU revision	: 4


>processor	: 3

>model name	: ARMv7 Processor rev 4 (v7l)

>BogoMIPS	: 38.40

>Features	: half thumb fastmult vfp edsp neon vfpv3 tls vfpv4 idiva idivt vfpd32 lpae evtstrm crc32 

>CPU implementer	: 0x41

>CPU architecture: 7

>CPU variant	: 0x0

>CPU part	: 0xd03

>CPU revision	: 4


>Hardware	: BCM2709

>Revision	: a22082

>Serial		: 00000000c120845a



# If you want to install lower version of tensorflow(v 0.9.0):  

>Follow this : 

>https://medium.com/@paroskwan/layman-installation-guide-for-keras-and-tensorflow-on-rpi-3-38b84f3e59dc


```sh
$ sudo easy_install pip3
$ sudo easy_install --upgrade six
```

# For python 2 :
```sh
$ export TF_BINARY_URL=https://storage.googleapis.com/tensorflow/mac/tensorflow-0.9.0-py2-none-any.whl
$ sudo pip install --upgrade $TF_BINARY_URL
```

# For Python 3:

```sh
$ export TF_BINARY_URL=https://storage.googleapis.com/tensorflow/mac/tensorflow-0.9.0-py3-none-any.whl
$ sudo pip3 install --upgrade $TF_BINARY_URL
```

>if this doesn't work

```sh
$install brew
$brew install python
$export TF_BINARY_URL=https://storage.googleapis.com/tensorflow/mac/tensorflow-0.9.0-py2-none-any.whl
$sudo pip install --upgrade $TF_BINARY_URL
```

# If you want to install tensorflow(v 1.1.0) :

>Follow this :

>https://github.com/samjabrahams/tensorflow-on-raspberry-pi

# If you want to install higher version tensorflow( version >= v1.2): 

>First we install python lastest version on pi from:

>http://bohdan-danishevsky.blogspot.com/2017/01/building-python-360-on-raspberry-pi-3.html

>Then use project nightly-pi-python3.

>Download lastest tensorflow from here:

>http://ci.tensorflow.org/view/Nightly/job/nightly-pi-python3/

>You can find different version here :

>https://github.com/lhelontra/tensorflow-on-arm/releases

>After that run command  : 

```sh
$sudo pip3 install tensorflow-1.6.0rc1-cp36-none-any.whl
```
>Common error : 

>tensorflow-1.6.0rc1-cp36-none-any.whl is not a supported wheel on this platform.   

>Then cheak your python version by press python3, if your version is like 3.5, Change the file name like that: tensorflow-1.6.0rc1-cp35-none-any.whl

>                                                                          ^^                                            	

>Then run a simple tensorflow program like this :
    ```sh
              $python3 
              >>>import tensorflow as tf
              >>>hello = tf.constant('Hello, TensorFlow!')
              >>>sess = tf.Session()							
              >>>print(sess.run(hello))
     ```         

>Output : Hello, TensorFlow!

>Cheak the version by this : python3 -c 'import tensorflow as tf; print(tf.__version__)'

>Reference :

         https://gist.github.com/elBradford/5e0c999b6d2ab8fcf5331c5ac177a486
				 
         https://github.com/samjabrahams/tensorflow-on-raspberry-pi/issues/104
				 
         https://nikhilraghava.wordpress.com/2017/08/05/installing-keras-on-raspberry-pi-3/
				 
         https://github.com/tensorflow/tensorflow/issues/5478
				 
         https://github.com/samjabrahams/tensorflow-on-raspberry-pi/releases/
				 
         https://www.tensorflow.org/install/install_linux
				 
         https://codelabs.developers.google.com/codelabs/tensorflow-for-poets/
