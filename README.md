# environments
Conda Environments for different tasks exported to YAML files

### Creating an environment from an environment.yml file

conda env create -f environment.yml

### for installing keras_contrib

sudo pip install git+https://www.github.com/keras-team/keras-contrib.git

### port forwarding for jupyter notebooks

ssh -N -f -L localhost:8889:localhost:8889 username@ip

jupyter notebook --no-browser --port=8888 notebook_name.ipnb

### Sync the fork with the parent repo
https://help.github.com/articles/syncing-a-fork/
https://help.github.com/articles/configuring-a-remote-for-a-fork/

### get name of layers in a pretrained tensorflow model
Graph(https://www.tensorflow.org/programmers_guide/graphs)
sess.graph.get_operations() gives you a list of operations. For an op, op.name gives you the name and op.values() gives you a list of tensors it produces (in the inception-v3 model, all tensor names are the op name with a ":0" appended to it, so pool_3:0 is the tensor produced by the final pooling op.)




