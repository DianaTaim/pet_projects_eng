Test case No1:
We extracted data from GCP. The dataset contains 4 million rows, but we were only able to
extract them in small portions, about 40,000 rows in CSV format. In total, we ended up with
110 files. The files are named as follows:
data_000000000001.csv
data_000000000002.csv
.....
data_000000000010.csv
data_000000000011.csv
......
data_000000000100.csv
data_000000000101.csv
....
data_000000000110.csv
Please suggest a method for uploading all these 110 files using Jupyter Notebook (or
another) and merging them into a single dataset for further processing.


Answer: To my mind we could put in all names of the files into list like:
filenames = [‘data_000000000001.csv’, ‘data_000000000002.csv’ ... ]
Then we can use  “for”, after it we can use function “concat’ for
merging all dataset in one, if they are equal
for x in filenames():
df = pd.read_csv(x)
df0 = pd.concat([df0, df])
