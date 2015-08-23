# gettngCleaningData
## Pregunta 1. Quizz 3
> x <- getURL(URL)  ### leer el archivo CSV
> out <- getURL(URL)
> out  <- read.csv(textConnection(x))
> head(out[1:6])

## Convertirlo a dplyr
library(dplyr)

tbl_df(out)
### Generar el data.frame

quest1 <- filter(out, ACR > 10, ADJUST >= 10000)
quest1
## Crear el vector logico agricultureLocal

agricultureLogical <- quest1
which(agricultureLogical, arr.ind = FALSE)
