# Fake news motif detection

## Data Processing

I used pandas and numpy with jupyter notebook to process the data given by Tina.

### Original Data Format

The original data was given in CSV format, and it looks like this

```
<Parent Node> <Child Node>
```

Specifically, each node is represented as 

```
<ID><# of characters><first letter><last letter>
```

For example, "hello world" sent by bob would be represented as

```
bob5hd
```

### Required data format by FANMOD

The data form required by the application must have the form

```
<Parent Node> <Child Node>
```

Where every node should be given an unique numeric ID

### Processing the Data

To process the data, just use the python script I created for this specific purpose.

```
data_process('Large')
```

This function generates a required txt file for the csv file named "Large".
For more files, it is possible to use a for loop to generate all the files.

## Motif Detection

Once you have the data, you can start to put it into FANMOD, an open source application that supports motif detection.

### Getting started

Enter the "randesu" directory and type the following in your terminal window

```
./randesu <inputFile>
```

To see more configuration options, type the following in the same directory

```
./randesu --help
```

You can easily modify the subgraph size by typing 

```
./randesu <inputFile> -s <subgraph size>
```

### Batch Mode

You can use the batch mode by simply writing a shell script for more data files


## Built With

* [FANMOD] http://theinf1.informatik.uni-jena.de/motifs/


## Authors

* **Bo Ni** - *Initial work* 


## Acknowledgments

* Notre Dame Social Sensing Lab
