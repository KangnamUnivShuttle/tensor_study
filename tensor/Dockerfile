FROM tensorflow/tensorflow:2.0.3-py3-jupyter

RUN pip3 install keras==2.3
RUN pip3 install pandas==1.1.5
RUN pip3 install matplotlib==3.3.4
RUN pip3 install seaborn==0.11.2
RUN pip3 install scikit-learn==0.24.2

CMD ["jupyter", "notebook", "--ip=0.0.0.0", "--NotebookApp.token=", "--allow-root"]