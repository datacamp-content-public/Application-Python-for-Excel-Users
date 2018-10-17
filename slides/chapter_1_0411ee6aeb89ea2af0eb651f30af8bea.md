---
title: Insert title here
key: 0411ee6aeb89ea2af0eb651f30af8bea

---
## Reading Multiple Sheets from a Workbook

```yaml
type: "TitleSlide"
key: "171605d3a9"
```

`@lower_third`

name: Chris Cardillo
title: DataCamp Instructor (omg is this real life)


`@script`



---
## Previously...

```yaml
type: "TwoColumns"
key: "6ffa34f81f"
center_content: false
disable_transition: false
```

`@part1`
```
#1
import pandas as pd

```


`@part2`
1. Imported pandas package


`@script`
In Chapter 1, you'll recall we imported the pandas package, which afforded us the functionality to read in and interact with our Excel workbook in Python.


---
## Previously...

```yaml
type: "TwoColumns"
key: "ab71d614f8"
```

`@part1`
```
#1
import pandas as pd

#2
df = pd.read_excel('file.xlsx')
```


`@part2`
1. Imported pandas package

2. Read the first sheet of _file.xlsx_, stored as a dataframe


`@script`
When we used the pd.read_excel() function to read in our file, it automatically turned the first tab of our Excel workbook into a pandas dataframe object, which we immediately stored in the variable 'df'.


---
## Previously...

```yaml
type: "TwoColumns"
key: "a632d88f1c"
```

`@part1`
```
#1
import pandas as pd

#2
df = pd.read_excel('file.xlsx')




#3
df.head()

```


`@part2`
1. Imported pandas package

2. Read the first sheet of _file.xlsx_, stored as a dataframe

3. Used a method to look at first 5 rows


`@script`
We then used the .head() method to inspect the first 5 rows of our dataframe...


---
## Previously...

```yaml
type: "TwoColumns"
key: "54c300f0e7"
```

`@part1`
```
#1
import pandas as pd

#2
df = pd.read_excel('file.xlsx')




#3
df.head()



#4
df.shape
```


`@part2`
1. Imported pandas package

2. Read the first sheet of _file.xlsx_, stored as a dataframe

3. Used a method to look at first 5 rows

4. Used an attribute to look at the data's dimensions


`@script`
...and the .shape attribute to inspect the number of rows and columns present in our data. Remember, an easy way to think about the difference between methods and attributes is that methods are verbs and attributes are nouns. Methods do, and attributes are. This will become more intuitive as we move into Chapter 2.


---
## Final Slide

```yaml
type: "FinalSlide"
key: "962cce4835"
```

`@script`


