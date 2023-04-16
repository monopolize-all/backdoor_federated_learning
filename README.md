Forked from: https://github.com/ebagdasa/backdoor_federated_learning

# backdoor_federated_learning

Updates made via fork:
1) Code now runs in Python 3.7 and Pytorch 1.7.1+cu110
2) folder saved_models contains BASE, which is a model trained for Image Classification task for 10,000 epochs. This is in relation to the paper, which requires such a trained model on which backdoor attacks are conducted.
3) utils/img_class_continue.yaml has been made to allow model poisoning from saved_models/BASE.


# Steps to run code:
1) Clone repository
```
git clone https://github.com/monopolize-all/backdoor_federated_learning.git
cd backdoor_federated_learning
```
2) Make a new venv and activate it
```
python3.7 -m venv venv
source venv/bin/activate
```
3) Start visdom server and specify port
```
visdom -port 8097
```
4) Run poisoning on pretrained model (Requires new terminal window with venv activated as visdom needs to be kept running.)
```
visdom -port 8097
```

To run posioning:
```
python training.py --params utils/img_class_continue.yaml
```


# Credits
Credits go to eugene@cs.cornell.edu as code has been originally provided by him. All I did was make it compatible with newer pytorch versions and also provide a pretrained model for Backdoor attacks on Image Classification.

This code includes experiments for paper "How to Backdoor Federated Learning" (https://arxiv.org/abs/1807.00459)
