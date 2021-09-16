FROM tensorflow/tensorflow:2.0.3-py3-jupyter

RUN pip3 install keras==2.3

CMD ["jupyter", "notebook", "--ip=0.0.0.0", "--NotebookApp.token=", "--allow-root"]