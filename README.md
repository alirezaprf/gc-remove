# gc-remove
Simple Commands to make life easy and remove branches with no origin

```powershell
git remote prune origin
```
### remove unused branches
```powershell
git branch -vv | Select-String -Pattern "gone" | ForEach-Object { $_ -split '\s+' | Select-Object -First 2 } | ForEach-Object { git branch -D $_  }
```

### cleanup
```powershell
git gc
```

