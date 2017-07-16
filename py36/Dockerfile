FROM python:3.6

RUN apt-get update \
    && apt-get install python3-dev python3-pip \
        python3-cffi libcairo2 libpango1.0-0 \
        libgdk-pixbuf2.0-0 libffi-dev shared-mime-info \
        default-jre unzip wget -y \
    && pip3 install --upgrade setuptools \
    && pip3 install pandas cython spacy nltk scikit-learn scipy \
    && python3 -c "import spacy; spacy.cli.download('en')" \
    && python3 -c "import nltk; nltk.download('stopwords'); nltk.download('punkt')"

CMD ["python3"]
