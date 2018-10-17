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
In Chapter 1, you'll recall we imported the pandas package, which afforded us the functionality to read in and interact with our Excel data in Python.


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

2. Read the first tab of _file.xlsx_, stored as a dataframe


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

2. Read the first tab of _file.xlsx_, stored as a dataframe

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

2. Read the first tab of _file.xlsx_, stored as a dataframe

3. Used a method to look at first 5 rows

4. Used an attribute to look at the data's dimensions


`@script`
...and the .shape attribute to inspect the number of rows and columns present in our data. Remember, an easy way to think about the difference between methods and attributes is that methods are verbs and attributes are nouns. Methods do, and attributes are. This will become more intuitive as we move into Chapter 2.


---
## Two Sheet Picture

```yaml
type: "FullImageSlide"
key: "07447639db"
```

`@part1`
![](http://assets.datacamp.com/production/repositories/3817/datasets/70807d1e8ac6a072a8b02f7a6382cc4a0f66efca/Two%20Tabs.png)


`@script`
So what if you want to work with multiple sheets from your Excel workbook? For instance, here we have roles and departments of different DataCamp employees located on different tabs of our workbook.


---
## pd.ExcelFile()

```yaml
type: "FullCodeSlide"
key: "a55c97e56a"
```

`@part1`
```
import pandas as pd

workbook = pd.ExcelFile('file.xlsx')
```


`@script`
Fortunately, pandas has us covered. The pd.ExcelFile() function reads the entire workbook into Python as an ExcelFile object. Here, we are storing the object in a variable called 'workbook'. 

You can think of the 'workbook' variable as a representation of the entire Excel workbook in Python. This gives us the freedom to now turn each tab of the Excel workbook into separate DataFrames. Note, we have not done this yet.


---
## pd.ExcelFile() vs. pd.read_excel()

```yaml
type: "TwoColumns"
key: "9379711499"
center_content: false
```

`@part1`
## Workbook Object

```
workbook = pd.ExcelFile('file.xlsx')
```

- Reads entire workbook into memory
- Creates **workbook object**
- Has **NOT** created any dataframes


`@part2`
## Single DataFrame

```
df = pd.read_excel('file.xlsx')
```

- Reads first tab of workbook
- Turns tab into a **dataframe**


`@script`
To reiterate, pd.ExcelFile() reads the entire Excel workbook into Python, while pd.read_excel() only reads in the first tab of an Excel workbook. Additionally, while pd.read_excel() creates a dataframe, pd.ExcelFile() does not. Because dataframes are our desired format for working with data in Python, we'll have to work with the output of pd.ExcelFile() a bit more.


---
## Sheet Names

```yaml
type: "FullCodeSlide"
key: "a7c90acb49"
```

`@part1`
```
import pandas as pd

workbook = pd.ExcelFile('file.xlsx')

workbook.sheet_names
```


`@script`
Firstly, our workbook variable has a very useful attribute, called 'sheet_names', which - intuitively - tells us the names of each sheet in our workbook. With this knowledge, we can move on to turning each sheet into a dataframe.


---
## Parse

```yaml
type: "FullCodeSlide"
key: "ab8fe5972f"
```

`@part1`
```
import pandas as pd

workbook = pd.ExcelFile('file.xlsx')

workbook.sheet_names

df_one = workbook.parse('Roles')
df_two = workbook.parse('Departments')

```


`@script`



---
## Fin

```yaml
type: "FinalSlide"
key: "962cce4835"
```

`@script`


