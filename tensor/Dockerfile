FROM tensorflow/tensorflow:2.0.3-py3-jupyter

RUN apt-get update
RUN apt-get upgrade -y
RUN pip3 install --upgrade pip

COPY ./requirements.txt .
RUN pip3 install -r requirements.txt

RUN pip3 install openpyxl==3.0.9

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

# RUN apt-get install -y chromium unzip crul
# RUN wget -O /tmp/chromedriver.zip http://chromedriver.storage.googleapis.com/`curl -sS chromedriver.storage.googleapis.com/LATEST_RELEASE`/chromedriver_linux64.zip
# RUN unzip /tmp/chromedriver.zip chromedriver -d /usr/local/bin/

CMD ["jupyter", "notebook", "--ip=0.0.0.0", "--NotebookApp.token=", "--NotebookApp.base_url=/jupy2", "--allow-root"]