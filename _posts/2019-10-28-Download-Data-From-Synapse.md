---
'0': D
'1': a
'2': t
'3': e
'4': ':'
'5': '2'
'6': '0'
'7': '1'
'8': '9'
'9': '-'
'10': '1'
'11': '0'
'12': '-'
'13': '2'
'14': '8'
'15': ' '
'16': T
'17': i
'18': t
'19': l
'20': e
'21': ':'
'22': S
'23': 'y'
'24': 'n'
'25': a
'26': p
'27': s
'28': e
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
