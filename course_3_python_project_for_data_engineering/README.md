# Python Project for Data Engineering

## Extract, Transform, Load(ETL)

- A type of batch processing(collect data from multiple source and combine to become a single source of information).
- It is the process of extracting large amount of data from multiple sources and formats, then transforming into one format before loading to a database or target file.

**Composite functions**:

```python
import glob

list_csv = glob.glob('*.csv')
print(list_csv) # Output: ['source1.csv', 'source2.csv']

list_json = glob.glob('*.json')
print(list_json) # Output: ['source1.json', 'source2.json', 'source3.json']
```

**Extract(E)**:

```python
def extract_from_csv(file_to_process):
    dataframe = pd.read_csv(file_to_process)
    return dataframe

def extract_from_json(file_to_process):
    dataframe = pd.read_json(file_to_process)
    return dataframe

def extract():
    # Declare empty dataframe to store extracted data
    extracted_data = pd.DataFrame(columns=['name', 'height', 'weight'])

    # Process all csv files
    for csvfile in glob.glob('*.csv'):
         extracted_data = extracted_data.append(extract_from_csv(csvfile), ignore_index=True)

    # Process all json files
    for jsonfile in glob.glob('*.json'):
         extracted_data = extracted_data.append(extract_from_json(jsonfile), ignore_index=True)
    
    return extracted_data
```

**Transform(T)**:

```python
def transform(data):
    # Convert height to meter from inches
    data['height'] = round(data.height * 0.0254, 2)

    # Convert height to kilogram from pounds
    data['weight'] = round(data.weight * 0.45359237, 2)

    return data
```

**Load(L)**:

```python
def load(target_file, data_to_load):
    data_to_load.to_csv(target_file)

target_file = "transformed_data.csv"
```

**Logging**:

```python
from datetime import datetime

def log(message):
    timestamp_format = '%Y-%h-%d-%H:%M:%S'
    now = datetime.now
    timestamp = now.sfrtime(timestamp_format)
    with open("logfile.txt", "a") as f:
        f.write(timestamp + ': ' + messge + '\n')
```

**Joining ETL components**:

```python
log("ETL Job Started")

log("Running Extract Phase...")
extracted_data = extract()
log("Complted Extract Phase")

log("Running Transform Phase...")
transformed_data = transform(extracted_data)
log("Complted Transform Phase")

log("Running Load Phase...")
load(target_file, transformed_data)
log("Complted Load Phase")

log("ETL Job Ended")
```

**Hands-on Lab**: [ETL](labs/1-ETL.ipynb)

<hr style="border:2px solid gray">

## Final Project

**Hands-on Lab**: [Web Scrapping](labs/2-Project_Webscraping.ipynb)


<hr style="border:2px solid gray">
