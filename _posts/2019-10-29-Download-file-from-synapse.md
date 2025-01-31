---
Title: Synapse Download
Date: {}
Language: Python
published: true
---

***PYTHON Code***

1. import synapseclient  
2. import synapseutils  
3. syn = synapseclient.Synapse()  
4. syn.login('username','password')  
Welcome, username!

**Bulk download**

syn5580964 is the parent folder. This command will download all
subfolders in syn5580964

5. files = synapseutils.syncFromSynapse(syn, entity = 'syn5580964',
path='./mayo_RNASeq')

**single file download**

6. file = syn.get("syn5580982")

[Please read Synapse documents for
detail](https://docs.synapse.org/articles/downloading\_data.html)

This method will download several uncessary folders under syn5580964.

The structure is, for example,  
--syn5580964  
--> subfolder 765  
-->subfoder 7313768  
--> real RNA\_seq file like "1785276561_B.FCD1LUUACXX_L1_ICGATGT.snap.bam"

So a more practical method is to

1. use the "copy id" function on synapse web to copy all synapse ids
you want to download under syn5580964.

2. use [This website](https://delim.co/#) to convert ids to strings (add double quote)
and comma separated. You can setup converting methods.

3. Then you can copy and paste the ids to a list in jupiter notebook.

![jupyter notebook](/images/image3.png)

You mays also use Excel to format ids. Format column with \\\"@\\\",
in TYPE field.
