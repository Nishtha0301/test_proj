# test_proj_nishtha
import csv
import os
# Reverse
from itertools import izip
with open('/home/nishtha/Desktop/test.csv', 'r') as textfile:
    for row in reversed(list(csv.reader(textfile))):
       print ','.join(row)

# # SwapCase 
with open('/home/nishtha/Desktop/test.csv', 'r') as textfile:
   for column in (csv.reader(textfile)):
       column[0]=column[0].swapcase()
       column[1]=column[1].swapcase()
       column[2]=column[2].swapcase()
       column[3]=column[3].swapcase()
       column[4]=column[4].swapcase()
       column[5]=column[5].swapcase()
       column[6]=column[6].swapcase()
       column[7]=column[7].swapcase()
       column[8]=column[8].swapcase()
       column[9]=column[9].swapcase()
       column[10]=column[10].swapcase()
       column[11]=column[11].swapcase()
       column[12]=column[12].swapcase()
       column[13]=column[13].swapcase()
       column[14]=column[14].swapcase()    
    #    for items in column:
    #        import pdb; pdb.set_trace()
    #        column = items.swapcase()
       print ', '.join(column) 

# replacing
ifile = open('/home/nishtha/Desktop/test.csv', 'rb')
reader = csv.reader(ifile,delimiter='\t')
findL = ['-', 'A']
replaceL = ['_', '@']

rep = dict(zip(findL, replaceL))

def findReplace(find, replace):
    s = ifile.read()
    for item, replacement in zip(findL, replaceL):
        s = s.replace(item, replacement)
        print(s)
    # ofile.write(s)

#date formatting
f = open('/home/nishtha/Desktop/test.csv')
csv_f = csv.reader(f)
for column in csv_f:
    if "First Added" in column: continue
    parts = column[1]
    split('/')
    data = "{}/{}/{}".format(parts[2],parts[1],parts[0])
print (data)
