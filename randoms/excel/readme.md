# Microsoft Excel

_Microsoft Excel for Mac, version 16.21.1_

Excel was chosen as a widely available, off-the-shelf option for generator variety.

The basic cell function of `=randbetween([bottom],[top])` was used configured per respective category requirements. The specs of the internal MS Excel random number generator is TBD... 

## CSV Schema

The data is recorded in CSV files and organized in the following column schema (with headers):

| **1** _(row)_     | bat _(batch ID)_ | of12 _(choices)_ | of16 _(choices)_ | of24 _(choices)_ |
| ----------------- | :--------------: | :--------------: | :--------------: | :--------------: |
| **2**             |       'b1'       |    int 1 to 12   |    int 1 to 16   |    int 0 to 23   |
| **3**             |       'b1'       |    int 1 to 12   |    int 1 to 16   |    int 0 to 23   |
| **4**             |       'b1'       |    int 1 to 12   |    int 1 to 16   |    int 0 to 23   |
| more rows...      |        ...       |        ...       |        ...       |        ...       |
| **333358**        |       'b2'       |    int 1 to 12   |    int 1 to 16   |    int 0 to 23   |
| **333359**        |       'b2'       |    int 1 to 12   |    int 1 to 16   |    int 0 to 23   |
| even more rows... |        ...       |        ...       |        ...       |        ...       |
| **416103**        |       'b6'       |    int 1 to 12   |    int 1 to 16   |    int 0 to 23   |