## Chức năng 1:

* 1 dòng lệch duy nhất tạo thư mục:
``` 
'docs', 'scripts', 'data', 'backup' | ForEach-Object {New-Item -p "smartfarm-system\$_" -ItemType Directory -Force }
 ```
* dùng đường dẫn tuyệt đối tạo file .env:
```
  New-Item -p "..\.env" -ItemType File -Value "DB_PASSWORD=demo_123456" -Force
```
* đặt thuộc tính Hidden cho file .env:
```
 Set-ItemProperty -Path "..\.env" -Name Attributes -Value "Hidden"
```
