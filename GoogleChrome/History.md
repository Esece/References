## Browsing History

Location
```
C:\Users\[USER]\AppData\Local\Google\Chrome\User Data\Default\History
```
 
Sample Code for Extracting the URL's
``` csharp
public static string[] GetHistory()
{
    var urls = new HashSet<string>();
    var path = Environment.GetFolderPath(Environment.SpecialFolder.LocalApplicationData) + @"\Google\Chrome\User Data\Default\History";
    var data = ReadOnlyFile.Read(path);

    var matches = Regex.Matches(data, "https?://");

    foreach (Match match in matches)
    {
        int i = match.Index + 1;

        for (; i < data.Length; i++)
        {
            if (data[i] <= 32 || 126 < data[i])
            {
                break;
            }
        }

        int length = i - match.Index;

        if (length > 0)
        {
            var url = data.Substring(match.Index, i - match.Index);
            urls.Add(url);
        }
    }

    return urls.ToArray();
}
```
