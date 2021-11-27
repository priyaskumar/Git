_Search and find_
==

To get the details of all logs after a certain date,
```
git log --after =[date]
```

To get the details of all logs between a certain period,
```
git log --after=[date] --before=[date]
```

To search for a commit,
```
git log --grep=[commit_msg]
```

To find all the commits by a certain author,
```
git log --author=[author_name]
```

To find all the commits of a particular file,
```
git log -- [file_name]
```
