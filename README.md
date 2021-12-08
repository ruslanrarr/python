# python
Заметки для Python
import pandas as pd
import glob

files = [item for item in glob.glob(r'/Users/ruslanrahimzanov/Desktop/test/*{}'.format('.xlsx'))]
files

comb = pd.DataFrame()
for file in files:
    file = pd.read_excel(file, skiprows = 3)
    comb = pd.concat([comb,file])
    
    comb.to_csv(r'/Users/ruslanrahimzanov/Desktop/test/comb.csv', encoding = 'utf-8-sig')
    
    comb
