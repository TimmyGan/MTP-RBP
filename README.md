# MTP-RBP

MTP-RBP aims to determine whether an RNA can have a binding site with a certain protein. Similar to BERT, it learns the Integrated sequence-structure-function characteristics of RNA simultaneously by pre-training.

First, MTP-RBP  incorporates an additional binding function prediction task on top of the MLM task, allowing it to capture the binding properties of RNA sequences while learning their deep contextual representations through pre-training on the in-task dataset.  Second, we also design a secondary structure construction task to guide the model in self-learning structural information, rather than inputting it as a separate branch. By simultaneously engaging in these pre-training tasks, the Encoder can integrate RNA sequence and structural features more effectively. Furthermore, through extended sequence modeling, MTP-RBP is able to better capture semantic information and sequence patterns.

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

For RNA secondary structure prediction, we use FocusFold to implement the prediction of RNA secondary structure. The predicted secondary structure is represented in a dot-bracket format, where each symbol corresponds to a base site in the sequence. Following the principle of base complementary pairing yields a secondary structure pairing tree diagram. 

You can choose the same tool or other RNA secondary structure prediction tools.<br><br>
Contact: Lin Gan (ganlin228@stu.scu.edu.cn)
