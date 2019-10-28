---
Title: Synapse Download 
Date: 2019-10-28
Language: Python

---

import synapseclient

import synapseutils

syn = synapseclient.Synapse()

syn.login('username','password')  
==>*Welcome, username!*

#**Bulk download**  
syn5580964 is the parent folder. This command will download all subfolders in syn5580964  

files = synapseutils.syncFromSynapse(syn, entity = 'syn5580964', path='./mayo_RNASeq')

#**single file download**

file = syn.get("syn5580982", version=1)

Please read Synapse documents for detail
https://docs.synapse.org/articles/downloading_data.html
