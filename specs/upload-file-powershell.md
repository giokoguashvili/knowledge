# Upload file over Powershell

### Posts:
- [PowerShell V3 Multipart/formdata example with REST-API (Invoke-RestMethod)](https://www.snip2code.com/Snippet/396726/PowerShell-V3-Multipart-formdata-example)
- [Multipart/form-data Support for Invoke-WebRequest and Invoke-RestMethod in PowerShell Core](https://get-powershellblog.blogspot.com/2017/09/multipartform-data-support-for-invoke.html)

```powershell
$fileName="README.md"
$uri = "http://www.markdowntopdf.com/app/upload"
$currentPath = Convert-Path .
$filePath="$currentPath\$fileName"
$fileBin = [System.IO.File]::ReadAlltext($filePath)
$boundary = [System.Guid]::NewGuid().ToString()
$LF = "`r`n"
$bodyLines = (
    "--$boundary",
    "Content-Disposition: form-data; name=`"file`"; filename=`"$fileName`"",
    "Content-Type: application/octet-stream$LF",
    $fileBin,
    "--$boundary--$LF"
) -join $LF
Invoke-RestMethod -Uri $uri -Method Post -ContentType "multipart/form-data; boundary=`"$boundary`"" -Body $bodyLines
```
