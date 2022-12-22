# Fasttext-model

This repo contains the binary file for english language of the fasttext pretrained language model. The model asigns to each word a vector of dimension 300. It was dowloaded from [fasttext website](https://fasttext.cc/docs/en/pretrained-vectors.html) and its date of creation is 19/10/2017. 

## Downloading the model

These are the steps needed for downloading the model : 

<ol>
    <li> Open the model repository in your browser. </li>
    <li> Click on the 'tag' button to select <em><strong> fasttext_model </strong></em> tag. </li>
    <li> Inside the assets click on the files 'fasttext_model_*' to download the five parts in which we have divided the model to store it on a git repository. </li> 
</ol>

## Joining the parts of the model 

Once we have downloaded the different parts of the model, we must join them. To do so, we must run the following command on terminal inside the directory where we have downloaded the parts of the model. 

<pre><code> cat fasttext_model* > wiki.en.bin </pre></code> 

This will output a binary file called 'wiki.en.bin' that we can use to encode words of the english dictionary into numeric vectors. 