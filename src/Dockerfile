from python:3

RUN mkdir -p /tmp
ADD requirements.txt /tmp
RUN pip install -r /tmp/requirements.txt

RUN mkdir -p /srv
ADD main.py /srv

WORKDIR /srv

CMD python main.py
