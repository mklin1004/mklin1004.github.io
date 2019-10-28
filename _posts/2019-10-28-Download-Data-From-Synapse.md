---
Title: Synapse Download 
Date: 2019-10-28
Language: Python

---
***PYTHON***

1. import synapseclient
2. import synapseutils
3. syn = synapseclient.Synapse()
4. syn.login('username','password')  
==>*Welcome, username!*

**Bulk download**  
syn5580964 is the parent folder. This command will download all subfolders in syn5580964  

5. files = synapseutils.syncFromSynapse(syn, entity = 'syn5580964', path='./mayo_RNASeq')

**single file download**

6. file = syn.get("syn5580982")

[Please read Synapse documents for detail](https://docs.synapse.org/articles/downloading_data.html)
