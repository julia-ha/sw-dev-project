# JSTOR Labs software developer project - Chronicling America

## Overview

The project assignment is to develop a [Jupyter Notebook](https://jupyter.org/) that harvests, transforms and analyzes data from the [Library of Congress's Chronicling America API](https://chroniclingamerica.loc.gov/about/api/).

Chronicling America provides access to historical digitized newspapers. The newspapers are arranged by [title](https://chroniclingamerica.loc.gov/newspapers/) and [issue](https://chroniclingamerica.loc.gov/lccn/sn84021940/1908-09-03/ed-1/) on the Chronicling America website.

The LCCN identifier included on the details page for an individual newspaper can be used to make calls to the Chronicling America API to find information about individual newspapers.

### Harvest

Using the Chronicling America API, harvest 100 or more newspaper issues from two or more newspapers.

The sample functions in the [provided notebook](chronicling-america-example.ipynb) provide examples of calling the API via Python.

### Transform

Transform each harvested issue from its source format to the metadata schema described below. Save the harvested data to a file using the [JSON Lines](http://jsonlines.org/) format where each line is a valid JSON object.

#### Metadata schema

Each harvested issue of a newspaper should follow this metadata schema. You can add additional attributes if you wish, but the following are required. The `text` element is an array of strings where each element in the array is a string that represents the OCR text (Optical Character Recognition) of a page.

* Source data: https://chroniclingamerica.loc.gov/lccn/sn98060264/1917-11-20/ed-1.json
* Sample OCR page: https://chroniclingamerica.loc.gov/lccn/sn98060264/1917-11-20/ed-1/seq-1/ocr.txt

```json
{
    "source": "https://chroniclingamerica.loc.gov/lccn/sn98060264/1917-11-20/ed-1.json",
    "title": "Valdez daily prospector 1917-11-20",
    "isPartOf": "Valdez daily prospector",
    "datePublished": "1917-11-20",
    "volume": "14",
    "number": "49",
    "text": [
        "page 1.....",
        "page 2.....",
        "page 3.....",
        "page 4....."
    ]
}
```

### Analyze

Once the issues have been harvested and mapped to the provided schema, create a Jupyter Notebook that analyzes the harvested data in some way. This could be as simple as identifying the most common words in your dataset, plotting issues by region, topic modeling. Feel free to install additional Python libraries by adding them to your repositories `requirements.txt` file.

The [Chronicling America API](https://chroniclingamerica.loc.gov/about/api/) provides access to additional file formats (pdf, jpeg) for the dataset that could also be used as part of your analysis.
