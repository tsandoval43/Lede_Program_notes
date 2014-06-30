## Sharing files from server to local machine (my laptop, in common parlance)

First, I fire up my terminal and go to my directory where my key is. My key is in the Key_Pair folder on my desktop. ```cd Key_Pair``` 

There are a few other things I could do, such as use ```chmod``` to modify my permissions, I then go ahead and get connected to my amazon server: 

```
 ssh -vi ColumbiaLedeProgram.pem admin@54.88.194.100
```
ssh is a cryptographic network protocol for secure data transmission, remote command line login and other network services. It connects over a secure channel   over an insecure network.. 

so we start with ```ssh```

```-vi``` asks me for more information, tells me that it is looking for a key. we then write the public key that we were given. we can sign in as admin@ out IP address. 

After I run this I will be connected to the server. I can run ```ls``` and see what is in the server that I am in. 

This produces this 	```master.zip  notebooks  notebooks.tar.gz```

I already have a zip file with my notebookfiles as I have uploaded this onto my local machine. 
If I want to reproduce that I can run this ```tar -zcvf notebooks2.tar.gz notebooks/```

tar is what will compress my file. I am asking for tar to compress the notebook folder. I am calling the file notesbooks2.tar.gz as I already have notebooks.tar.gz saved to my computer. 

I then logout of my server. and then get back to my Key_Pair folder. When I do this:

```
scp -i ColumbiaLedeProgram.pem admin@54.88.79.36:notebooks.tar.gz .
```

In this I will use my public key and download the notes bookes compressed file from my server. 









