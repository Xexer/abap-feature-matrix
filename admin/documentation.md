# Documentation

## Structure
The following directories you will find in the project.

- **config** - Configuration files
- **content** - ABAP content
- **wiki** - Wiki pages for more Informations
- **admin** - Administrative files for the project

## Control files
There are some control files that are used to build the structure and contain context information.

### files.json
The file contains a list of all relevant files with content to build the overall list. A sequence for the output can be created using “Order”. The title is relevant for delimiting the file and displaying value help before the content is loaded.

```JSON
{
    "Title": "ABAP Statements",
    "FilePath": "https://raw.githubusercontent.com/Xexer/abap-feature-matrix/main/content/abap-statements.json",
    "Order": 1
},
```

### releases.json
Contains technical information about the release, as well as the title for the edition. The “Order” field is used to put the releases in the correct order when output.

```JSON
{
    "ReleaseId": "7402",
    "Description": "7.40 (SP02)",
    "Order": 10
},
```

### status.json
Defines the available states of the objects, along with the title and icon for output.

```JSON
{           
    "IconId": "x",
    "Description": "Available",
    "GitIcon" : ":white_check_mark:",
    "RawIcon" : "✅"
},
```

## Content files
The content files contain the name (heading) and a description in the upper area, which is displayed above the table. The individual objects that are documented are listed in the Content area. The "Text" reflects the object and further information, the "GitLink" leads to documentation in the wiki and is generated as a link in the output. Within "Help" you can find the official link to the documentation on SAP Help. The "Release" array contains information about the status of the object (see status.json). If a status is set, it is valid until a new status is set. Basically the initial status at the beginning is "-".

```JSON
{
    "Name": "Objects - Class",
    "Description": "",
    "Content": [
        {
            "Text": "CL_ABAP_PARALLEL (*)",
            "GitLink": "https://github.com/Xexer/abap-feature-matrix/blob/main/wiki/objects.md#cl_abap_parallel",
            "Help": "",
            "Release": {
                "1511": "d",
                "1909": "x"
            }
        }
    ]
}
```

## Wiki files
The files contain further information on the individual subject areas. This includes official documentation, SAP blogs, external blogs and code examples.