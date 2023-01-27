# Fasttext-model

This repo contains the binary file for english language of the fasttext pretrained language model. The model asigns to each word a vector of dimension 300. It was dowloaded from [fasttext website](https://fasttext.cc/docs/en/pretrained-vectors.html) and its date of creation is 19/10/2017. 

## Downloading the model

In order to donwload the parts of the model, we will use the <em><strong> wget </strong></em> software package. In order to install it (on macOs) we can run the following command> 

<pre><code> brew install </pre></code>

Once this is done, to dowloand the different parts of the model, we just have to past the following command in the computer's terminal, in the directory where we have stored the repo. 

<pre><code> wget https://github.com/NEASQC-WP61/fasttext-model/releases/download/fasttext_model/fasttext_model_a https://github.com/NEASQC-WP61/fasttext-model/releases/download/fasttext_model/fasttext_model_b https://github.com/NEASQC-WP61/fasttext-model/releases/download/fasttext_model/fasttext_model_c https://github.com/NEASQC-WP61/fasttext-model/releases/download/fasttext_model/fasttext_model_d https://github.com/NEASQC-WP61/fasttext-model/releases/download/fasttext_model/fasttext_model_e </pre></code>

## Joining the parts of the model 

Once we have downloaded the different parts of the model, we must join them. To do so, we must run the following command on <em><strong> computer's terminal </strong></em> inside the directory where we have downloaded the parts of the model. 

<pre><code> cat fasttext_model* > wiki.en.bin </pre></code> 

(It is important to note here that if the command is runned in an IDE rather than in computer's terminal, results may vary). This will output a binary file called 'wiki.en.bin' that we can use to encode words of the english dictionary into numeric vectors. 

## Checking the SHA-2 hash of the file

Once we have downloaded and joined the model, we can check its SHA-2 hash to verify that we have the correct file. To do so we will run the following command in the terminal, in the same directory where we have the model 'wiki.en.bin' and the hash file 'hash_wiki.txt'. 

<pre><code> shasum -a 256 -c hash_wiki.txt </pre></code>

This command will check the SHA-256 hash of the model file to check that we have donwloaded the correct file. If this is the case, we should be seeing the following message on terminal : 


<pre><code> wiki.en.bin: OK </pre></code>

