FROM tensorflow/tensorflow:2.0.3-py3-jupyter

COPY ./requirements.txt .
RUN pip3 install -r requirements.txt

RUN pip3 install openpyxl==3.0.9

RUN apt-get update
RUN apt-get install git -y
RUN pip3 install git+https://github.com/ssut/py-hanspell.git

RUN pip3 install konlpy==0.6.0
RUN pip3 install git+https://github.com/lovit/customized_konlpy.git
RUN apt install default-jdk -y

RUN pip3 install nltk==3.6.7

RUN apt-get install -y unzip curl wget
RUN pip3 install selenium==3.14.1
RUN curl -sS -o - https://dl-ssl.google.com/linux/linux_signing_key.pub | apt-key add 
RUN echo "deb [arch=amd64] http://dl.google.com/linux/chrome/deb/ stable main" >> /etc/apt/sources.list.d/google-chrome.list 
RUN apt-get -y update

RUN apt install fonts-nanum-coding -y

RUN pip3 install google-cloud-vision==2.6.3

# COPY ./service-account.json /tf/

RUN pip3 install google-api-python-client==2.39.0
RUN pip3 install google-auth-httplib2==0.1.0
RUN pip3 install google-auth-oauthlib==0.5.0

CMD ["jupyter", "notebook", "--ip=0.0.0.0", "--NotebookApp.base_url=/jupy2", "--allow-root"]