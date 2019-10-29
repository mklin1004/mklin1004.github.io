\-\--

Title: Synapse Download

Date: 2019-10-28

Language: Python

\-\--

\*\*\*PYTHON\*\*\*

1\. import synapseclient

2\. import synapseutils

3\. syn = synapseclient.Synapse()

4\. syn.login(\'username\',\'password\')

==\>\*Welcome, username!\*

\*\*Bulk download\*\*

syn5580964 is the parent folder. This command will download all
subfolders in syn5580964

5\. files = synapseutils.syncFromSynapse(syn, entity = \'syn5580964\',
path=\'./mayo\_RNASeq\')

\*\*single file download\*\*

6\. file = syn.get(\"syn5580982\")

\[Please read Synapse documents for
detail\](https://docs.synapse.org/articles/downloading\_data.html)

This method will download several uncessary folders under syn5580964.

The structure is syn5580964

\--\> 765

\--\>7313768

\--\> real RNA\_seq file like
\"1785276561\_B.FCD1LUUACXX\_L1\_ICGATGT.snap.bam\"

So a more practical method is to

1\. use the \"copy id\" function on synapse web to copy all synapse ids
you want to download under syn5580964.

2\. use \[This website\](https://delim.co/\#) to convert ids to strings
and comma separated.

3\. Then you can copy and paste the ids to a list in jupiter notebook.

{% highlight python %}

ids = \[\"syn5580982\", \"syn5584053\", \"syn5584054\", \"syn5584062\",
\"syn5584075\", \"syn5584077\", \"syn5584078\", \"syn5584081\",

\"syn5584094\", \"syn5584647\", \"syn5584653\", \"syn5584657\",
\"syn5584660\", \"syn5584663\", \"syn5584667\", \"syn5584671\",

\"syn5584800\", \"syn5584803\", \"syn5584806\", \"syn5584810\",
\"syn5584818\", \"syn5584830\", \"syn5584843\", \"syn5584851\",

\"syn5584855\", \"syn5584865\", \"syn5584866\", \"syn5584870\",
\"syn5585211\", \"syn5585223\", \"syn5585706\", \"syn5585709\",

\"syn5585710\", \"syn5585712\", \"syn5585713\", \"syn5585715\",
\"syn5585717\", \"syn5585718\", \"syn5585720\", \"syn5585723\",

\"syn5585747\", \"syn5585753\", \"syn5585754\", \"syn5585755\",
\"syn5585757\", \"syn5585777\", \"syn5585784\", \"syn5585787\",

\"syn5585790\", \"syn5585792\", \"syn5585794\", \"syn5585795\",
\"syn5585797\", \"syn5585803\", \"syn5585806\", \"syn5585813\",

\"syn5585829\", \"syn5585848\", \"syn5585900\", \"syn5585940\",
\"syn5585995\", \"syn5586047\", \"syn5586069\", \"syn5586089\",

\"syn5586091\", \"syn5586095\", \"syn5586097\", \"syn5586101\",
\"syn5586107\", \"syn5586108\", \"syn5586112\", \"syn5586114\",

\"syn5586119\", \"syn5586124\", \"syn5586147\", \"syn5586149\",
\"syn5586150\", \"syn5586151\", \"syn5586160\", \"syn5586187\",

\"syn5586196\", \"syn5586223\", \"syn5586246\", \"syn5586267\",
\"syn5586268\", \"syn5586271\", \"syn5586272\", \"syn5586302\",

\"syn5586316\", \"syn5586325\", \"syn5586376\", \"syn5586415\",
\"syn5586420\", \"syn5586421\", \"syn5586422\", \"syn5586424\"\]

for row in ids:

files = syn.get(row, downloadLocation=\"./mayo\_RNAseq\")

{% Endhighlight python %}

You mays also use Excel to format ids. Format column with TYPE \\\"@\\,
in TYPE field.
