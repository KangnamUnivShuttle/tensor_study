FROM tensorflow/tensorflow:2.0.3-py3-jupyter

RUN pip3 install keras==2.3
RUN pip3 install pandas==1.1.5
RUN pip3 install matplotlib==3.3.4
RUN pip3 install seaborn==0.11.2
RUN pip3 install scikit-learn==0.24.2
RUN pip3 install opendatasets==0.1.20
RUN pip3 install Korpora==0.2.0
RUN pip3 install tokenizers==0.11.0
RUN pip3 install transformers==4.15.0

CMD ["jupyter", "notebook", "--ip=0.0.0.0", "--NotebookApp.base_url=/jupy2", "--allow-root"]