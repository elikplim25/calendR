# calendR R package
Ready to print monthly and yearly calendars made with ggplot2


## Installation

``` r
# Install the development version from GitHub:
# install.packages("devtools")
devtools::install_github("R-CoderDotCom/calendR")
```


## Yearly calendar

``` r
library(calendR)
calendR() # Defaults to the current year
```

![Calendar_2020](https://user-images.githubusercontent.com/67192157/90884872-db3a4600-e3b0-11ea-8259-31f9c373fc74.png)


## Monthly calendar

``` r
calendR(year = 2028, month = 1)
```
![Calendar_enero_2028](https://user-images.githubusercontent.com/67192157/90624619-82d04080-e218-11ea-8570-a2c3b0ccab6d.png)

``` r
calendR(month = 7, year = 2022, 
        special.days = c(1, 5, 12, 28),       # Color days of the month
        text = "Visit\nhttps://r-coder.com/", # Add some text
        text.at = c(1, 5, 12, 28))            # Where to add the text
```

![Calendar_julio_2022](https://user-images.githubusercontent.com/67192157/90627714-a301fe80-e21c-11ea-84ad-e1038d1b1282.png)


## Start of the week (Monday or Sunday)

``` r
# calendR(month = 1, start = "S") # Week starts on Sunday (default)
calendR(month = 1, start = "M")   # Week starts on Monday
```

![Calendar_enero_2020](https://user-images.githubusercontent.com/67192157/90624910-02f6a600-e219-11ea-8b8e-4b9a00aa7f06.png)


## Orientation ("landscape" or "portrait")

``` r
# calendR(year = 2021, orientation = "landscape") # Default
calendR(year = 2021, orientation = "portrait")
```

![Calendar_2021](https://user-images.githubusercontent.com/67192157/90625001-291c4600-e219-11ea-9478-7c65accc259a.png)


## Gradient

``` r
calendR(year = 2021, special.days = 1:365, gradient = TRUE, special.col = rgb(1, 0, 0, alpha = 0.6))
```

![Calendar_2021_GRADIENT](https://user-images.githubusercontent.com/67192157/90626971-ce381e00-e21b-11ea-919a-b5265c415110.png)


## Save as PDF (as A4 paper size)

``` r
calendR(year = 2021, orientation = "portrait", pdf = TRUE)
```

## Further customization

``` r

calendR( year = 2020,                                      # Year
         month = 10,                                       # Month
         title = "My calendar",                            # Change the title
         subtitle = "Have a nice day",                     # Add a subtitle (or motivational phrase)
         subtitle.col = 3,                                 # Color of the subtitle
         weeknames = c("S", "M", "T", "W", "T", "F", "S"), # Change week day names
         special.days = "weekend",                         # Colorize the weekends (you can also set a vector of days)
         special.col = rgb(0, 0, 1, 0.15),                 # Color of the special days
         text = "Running",                                 # Add text (only for monthly calendars)
         text.pos = c(7, 14, 25))                          # Days of the month where to put the texts       

# See all the arguments of the function for full customization of the colors, text size and style.
```

![Calendar_octubre_2020](https://user-images.githubusercontent.com/67192157/90625501-f6bf1880-e219-11ea-8c57-e10512d790b6.png)
