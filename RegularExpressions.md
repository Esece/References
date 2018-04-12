## Regular Expressions 
###### (Tested in C#)

|Type|Expression|Examples|Results|
|-----|-----|-----|-----|
|CSS Color Code|#((\d\|[a-fA-F]){6}\|(\d\|[a-fA-F]){3})|color:#85e6a9, color:#fff|#85e6a9, #fff|
|Inner HTML (td)|(\<td>)(.*?)(\</td>)|\<td>$12.4\</td>|$12.4|
|Zipcode with optional 4 digits|^\d{5}(\|-\d{4})$|30014, 97201-4512|true, true|
