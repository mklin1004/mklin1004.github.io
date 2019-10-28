---
Date:2019-10-28
Title:Synapse
---

import synapseclient
import synapseutils

syn = synapseclient.Synapse()

syn.login('username','password')
__Welcome, username!__

**Bulk download**
files = synapseutils.syncFromSynapse(syn, entity = 'syn5580964', path='./mayo_RNASeq')

**single file download**

file = syn.get("syn5580982", version=1)

Please read Synapse documents for detail
https://docs.synapse.org/articles/downloading_data.html
