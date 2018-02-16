# environments
Conda Environments for different tasks exported to YAML files

### Creating an environment from an environment.yml file

conda env create -f environment.yml

### for installing keras_contrib

sudo pip install git+https://www.github.com/keras-team/keras-contrib.git

### port forwarding for jupyter notebooks

ssh -N -f -L localhost:8889:localhost:8889 username@ip

jupyter notebook --no-browser port=8888 notebook_name.ipnb







