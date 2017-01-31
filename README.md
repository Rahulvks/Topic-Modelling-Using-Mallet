# Topic-Modelling-Using-Mallet
Topic Modelling Using Mallet 


Wikipedia dataset - Cricket,Football,Elecion




Download Mallet 
http://mallet.cs.umass.edu/index.php


Prerequisites
sudo apt-get update; sudo apt-get upgrade -y
sudo apt-get install ant mercurial openjdk-7-jdk -y


Steps 

hg clone http://hg-iesl.cs.umass.edu/hg/mallet
cd mallet
ant

Goto mallet folder


Step1:
./bin/mallet import-dir --input /users/username/database/ --output mydata.mallet --keep-sequence --remove-stopwords


Step2:Topic Modelling
bin\mallet train-topics  --input mydata.mallet


Step2:
bin\mallet train-topics  --input mydata.mallet --num-topics 3 --output.gz --tutorial_keys.txt --tutorial_compostion.txt 

NOTE:
1) outputs every word in your corpus of materials and the topic it belongs to into a compressed file (output.gz)
2) outputs a text document showing you what the top key words are for each topic (tutorial_keys.txt)
3) outputs a text file indicating the breakdown, by percentage, of each topic within each original text file you imported     (tutorial_composition.txt)
