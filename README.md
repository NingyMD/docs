# Stationeers Modding Documentation

https://stationeerslaunchpad.github.io/docs

## Local development

Install `mkdocs`
```
pip install -r requirements.txt
```
Verify `mkdocs` install
```
python -m mkdocs --version
```

Run server
```
mkdocs serve
```

Open local site in browser (may be different. use link output by `mkdocs serve`)
```
http://127.0.0.1:8000/
```

Edit markdown files in docs folder


<details>
<summary><h1>Troubleshooting</h1></summary>
## Windows
If `mkdocs` was not found and game a message like <ins>The term 'mkdocs' is not recognized as the name of a cmdlet, function, script file, or operable program.</ins>

Then run this command in your powershell terminal and copy the result.
```
python -c "import sys; print(sys.executable)"
```
You should get something like this `C:\Users\MyUserName\AppData\Local\Python\pythoncore-3.14-64\python.exe`. Left Click to copy it.

Then press `windows + s` and write `Enviroment Variables` then click `enter`. 
Find <ins>User variables for **Username**</ins> and under the **Variable** look for `Path` and edit.
Add **New**, and pase what you copied earlyer. Now change `python.exe` to `Scripts` (Case Sensitive)

Save the file (OK button)

run the following command and try `mkdocs serve` again.

```
$env:Path = [System.Environment]::GetEnvironmentVariable("Path","Machine") + ";" + [System.Environment]::GetEnvironmentVariable("Path","User")
```

</details>