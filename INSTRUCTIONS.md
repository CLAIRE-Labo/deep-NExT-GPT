# Instructions
This file contains extra instructions on how to interact with the code as there are some adjustments we had to make in 
order to make the file/code interactable and functioning.

## TLDR
As far as we are aware, the model does not correctly work and hence `running app.sh` and `demo_app.py` is not an option.
Therefore, we have created various different environments so that we cna interact with different components on their 
own.

### How to interact with the weights in the file?
If you would like to run a simple inference on the weights that are available you can do that by using the `fastchat` 
api.
Important environmental adjustment to use the fastchat is to upgrade the accelerate library to the latest version.

Afterwards you can run inference on the weights through a simple _Command Line Interface_:
```python
python -m fastchat.serve.cli --model-path /path/to/model/weights/
```

### How to "compile" original files
If you would like to run the original python files you will have to adjust your environment. For instance the 
accelerate library must be downgraded to the recommended 0.19.0 version.