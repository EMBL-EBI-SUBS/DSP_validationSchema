This is a collection of [meta]data standards used in the EBI Data submission portal. 

_Updated on 18/05/2020_

DSP have two endpoints for querying those standards, the __[checklists](https://submission.ebi.ac.uk/api/checklists?size=100)__ endpoint and the  __[validationSchema](https://submission.ebi.ac.uk/api/validationSchemas?size=100)__ endpoint. 

DSP __[checklists](https://submission.ebi.ac.uk/api/checklists?size=100)__ include both `spreadsheetTemplate` and `validationSchema` for the [meta]data standards. The `spreadsheetTemplate` is designed for non-programatic users and implemented in the DSP UI. The `validationSchema` is the JSON implementation of the standard. It is used in the DSP API for data validation
.
DSP __[validationSchema](https://submission.ebi.ac.uk/api/validationSchemas?size=100)__ is a subset of DSP __[checklists](https://submission.ebi.ac.uk/api/checklists?size=100)__. Not all DSP checklists have corresponding validation schemas. 

It's recommended to use the DSP __[checklists](https://submission.ebi.ac.uk/api/checklists?size=100)__ endpoint to get a overview of DSP standards, and use the __[validationSchema](https://submission.ebi.ac.uk/api/validationSchemas?size=100)__ endpoint for data validation.

#### Get all DSP standards.
```sh
#checklists
curl "https://submission-test.ebi.ac.uk/api/checklists?size=100 " > DSP_checklists.json

#validation schemas
curl "https://submission-test.ebi.ac.uk/api/validationSchemas?size=100 " > DSP_schema.json
```

#### A summary of all validationschemas and checklists

[A small script](get_DSP_checklists.py) to extract all DSP validation schemas into seperate JSON files, and generate [a validation schema summary file](validationSchema_summary.tsv) and a [checklist summary file](checklists_summary.tsv) .


