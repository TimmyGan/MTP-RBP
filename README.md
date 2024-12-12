# MTP-RBP

MTP-RBP aims to determine whether an RNA can have a binding site with a certain protein. Similar to BERT, it learns the Integrated sequence-structure-function characteristics of RNA simultaneously by pre-training.


![PPT自己的13](https://github.com/user-attachments/assets/386a1816-7b33-40bf-af33-203e78639e24)




# Dependency <br>

python 3.8.8 <br>NumPy v1.20.1 <br>tensorflow v2.7.0 <br>keras v2.7.0 <br>sklearn v0.24.1 <br> 

# Content <br>

./datasets: The training and testing dataset with sequence and label indicating it is binding sites or not<br>
./model: The MTP-RBP model code, which consists of a total of 6 parts :

- Part1：Pre-training mask data processing
- Part2：Model Building Functions
- Part3：Pre-training Step 1: Train  MLM and BFP pre-training tasks
- Part4：Pre-training Step 2: Train MLM, BFP and SSC pre-training tasks
- Part5：Fine tuning
- Part6：Evaluation of fine-tuning results

./structBEP: BEP Representation of Structures Used to Guide Secondary Structure Construction Tasks<br>

# NOTE

For RNA secondary structure prediction, we use RNAfold to implement the prediction of RNA secondary structure. The predicted secondary structure is represented in a dot-bracket format, where each symbol corresponds to a base site in the sequence. Following the principle of base complementary pairing yields a secondary structure pairing tree diagram. 

You can use RNAfold to make predictions about RNA secondary structure in the following ways

` “ Bash 
conda install -c bioconda viennarna <br> RNAfold --noPS < input.fa > output.fa
` “

You can choose the same tool or other RNA secondary structure prediction tools.<br><br>
Contact: Lin Gan (ganlin228@stu.scu.edu.cn)
