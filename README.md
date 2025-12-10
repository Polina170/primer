Get-ChildItem -Path "C:\Windows" -Directory | 
    Where-Object { $_.Name -match '[st]$' } |
    Sort-Object Name |
    Format-Table Name, LastWriteTime

Get-ChildItem -Path "C:\Windows" -Directory | 
    Where-Object { $_.Name -match '[st]$' } |
    Sort-Object Name |
    Select-Object Name, FullName, LastWriteTime |
    Out-File -FilePath "D:\осст3лаб\1.txt"

Write-Host "done"
