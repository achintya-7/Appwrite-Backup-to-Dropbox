# Appwrite-Backup-to-Dropbox

# 📁 Database Collection Backup using the Dropbox API
A sample Python Cloud Function that leverages Dropbox to create backups of all the collection of a database made using Appwrite.

## 📝 Environment Variables
Add the following environment variables in your Cloud Function settings.

* **APPWRITE_API_KEY** - Create a key from the Appwrite console with the following scope (`files.read`. 'files.write')
* **APPWRITE_ENDPOINT** - Your Appwrite Endpoint
* **DROPBOX_KEY** - OAuth token from [Dropbox](https://blogs.dropbox.com/developers/2014/05/generate-an-access-token-for-your-own-account) 
* **COLLECTION_ID** - Your collection ID for which you want the .csv file to be created

## 🛠 Building and Packaging

To package this example as a cloud function, follow these steps.

```bash
$ cd PATH/WHERE/YOU/DOWNLOADED/THE/REPO/Appwrite-Backup-to-Dropbox  
$ PIP_TARGET=./.appwrite pip install -r ./requirements.txt --upgrade --ignore-installed
```

* Ensure that your folder structure looks like this 
```
.
├── .appwrite/
├── main.py
└── requirements.txt
```

* Create a tarfile

```bash
$ cd ..
$ tar -zcvf code.tar.gz collection-backup
```

* Upload the tarfile to your Appwrite Console and use the following entrypoint command

```bash
python main.py
```

## 🎯 Trigger

Head over to your function in the Appwrite console and just press the excecute button.
