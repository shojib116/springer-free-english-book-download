## Python script to download all English Springer books released for free during the 2020 COVID-19 quarantine(To download free German Books follow the link in the courtesy)

###Courtesy

This code repo was downloaded from this link: https://bit.ly/2YWKxHa

which was for German books. This repo was downloaded and modified accordingly to download English books.

### Usage

Must have python installed and download this repo to a folder where you want to download the books. Then open cmd and run the following commands in the folder where you have downloaded the repo

If you want just one or two specific books, get the excel file from the folowing link and download just those: https://resource-cms.springernature.com/springer-cms/rest/v1/content/17858272/data/v4


### Usage in a virtual environment:

```bash
python3 -m venv .venv
. .venv/bin/activate
pip install -r requirements.txt
python3 main.py
```

### On Windows:

```
python -m venv .venv
cd .venv/Scripts
activate.bat
cd ../..
pip install -r requirements.txt
python main.py
```

### Source:
* https://group.springernature.com/gp/group/media/press-releases/freely-accessible-textbook-initiative-for-educators-and-students/17858180?utm_medium=social&utm_content=organic&utm_source=facebook&utm_campaign=SpringerNature_&sf232256230=1
* https://www.springernature.com/gp/librarians/news-events/all-news-articles/industry-news-initiatives/free-access-to-textbooks-for-institutions-affected-by-coronaviru/17855960
* https://resource-cms.springernature.com/springer-cms/rest/v1/content/17858272/data/v4

Thanks Springer!

## Docker container to do all the work

Considering you cloned the repo in a folder, as:
```bash
cd \home\[user]\workspace`
git clone https://github.com/alexgv99/springer_free_books.git
cd springer_free_books
mkdir downloads
```
You can run the scripts like that:

```bash
docker build . -t springer-image
docker run --rm -v [local_download_folder]:/app/downloads springer-image
```

and the downloads will be at [local_download_folder]

