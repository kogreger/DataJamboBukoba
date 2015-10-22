# DataJamboBukoba
Written by ChristopherCosler

This folder contains the Jambo Bukoba data for DSSG data dive. Note that two of the datasets  are CSV and one is a zipped csv due to its size.

## Access CSV
If you want to access the data directly with R, for http this usually works.

```R
df <- read.csv("http://raw.githubusercontent.com/ChristopherCosler/DataJamboBukoba/master/SchoolLevel.csv", sep=";")
```

Sometimes https causes trouble, then do

```R
library(RCurl)
  x <- getURL("https://raw.githubusercontent.com/ChristopherCosler/DataJamboBukoba/master/SchoolLevel.csv")
  y <- read.csv(text = x, sep=";")
```

## Access ZIP
```R
If you want to access the csv in the zip file directly with R, do this.
temp <- tempfile()
download.file("https://github.com/ChristopherCosler/DataJamboBukoba/raw/master/StudentLevel.zip",temp)
data <- read.csv(unz(temp, "StudentLevel.csv"), sep=";")
unlink(temp)
```  
