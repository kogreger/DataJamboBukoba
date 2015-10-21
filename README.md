# DataJamboBukoba
Contains the data for the data dive

Access the data in R for example via

  library(RCurl)
  x <- getURL("https://raw.githubusercontent.com/ChristopherCosler/DataJamboBukoba/master/SchoolLevel.csv")
  y <- read.csv(text = x)
