## Downloading nltk data

Nltk (Natural language toolkit) is a library for doing some basic text processing. It requires a language-specific data file, which you have to upload separately to the environment. Go to the [NLTK Corpora page](https://www.nltk.org/nltk_data/), download the _Punkt Tokenizer Models_. Unzip the file that downloads, open the PY3 folder inside the unzipped punkt folder. You should see a file called english.pickle -- that's what you'll need to upload to the ProQuest TDM environment.

## Uploading things

- Hit the file-folder-opening icon at the very top of the screen. Click on "Temporary files", then choose "Upload files".
- Navigate to the punkt/PY3 folder and upload the english.pickle file.
- Upload the tdm_wordvectors.ipyb file with the word vectors code, then close the window.
- Back in the ProQuest TDM browser tab, click "Upload" then go to "My Files" then "Temporary Files", then select english.pickle. Hit "upload" to confirm in the browser tab. Do the same for the .ipynb file with the word vector code.

## Setting up the nltk data

- In the ProQuest TDM Jupyter notebook browser tab, go to New > Folder. This will create something called Untitled Folder. Check the checkbox next to it, then hit the "Rename" button in the upper left. Rename it to `nltk_data`.
- Click on the _ntlk_data_ folder and create a new folder inside it. Rename it to `tokenizers`.
- Click on the _tokenizers_ folder and create a new folder inside it. Rename it to `punkt`.
- Click on the _punkt_ folder and create a new folder inside it. Rename it to `PY3` (make sure it's all caps).
- Click on the _PY3_ folder. Click on the upload button in the browser tab, choose _My Files_, then _Temporary Files_, then choose the english.pickle file.

Go back to the main Jupyter Notebook directory by clicking on the _Jupyter_ logo in the upper left.

## Creating an environment

- In the browser, go to New > Terminal
- Type `conda create -n vectors ipykernel nltk gensim pandas lxml bs4`
- Type y when it asks if you want to proceed
- Type `source activate vectors`
- Type `python -m ipykernel install --user --name=vectors`
- You can close or leave the tab with the terminal now

If you shut down the notebook server, you'll have to do this starting with `source activate vectors` when you restart.

## Running the notebook

Click on the tdm_wordvectors.ipynb file. You may see a "Kernel not found" error. From the dropdown, choose "vectors" then "set kernel". Follow the instructions in the notebook (e.g. which values to change to the name of your corpus directory, etc.)
