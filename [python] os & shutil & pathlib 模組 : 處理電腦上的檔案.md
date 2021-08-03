# os 模組
* 刪除一個檔案
  > os.remove('檔案名')
* 修改一個檔案名稱A命名為B
  > os.rename('檔案名A', '檔案名B')

***

# shutil 模組
* 單純複製檔案
  > shutil.copy("此檔案位置" , "目標檔案位置")
* 把一個檔從一個資料夾移動到另一個資料夾，並同時重命名(先剪下再貼上)
  > shutil.move('原資料夾/原檔案名','目的檔案夾/目的檔案名')

### 批次處理檔案樹
* 複製目錄內的所有檔案
  > shutil.copytree("此目錄" , "目標位置")
* 刪除該目錄內的所有檔案
  > shutil.rmtree("此目錄位置")

### 進階shutil
複製檔案的各種參數，不複製內容
* 目標檔案需存在，複製內容：複製參數不複製權限
  > shutil.copymode("此檔案位置" , "目標檔案位置")
* 目標檔案需存在，複製內容：複製參數與權限
  > shutil.copystat("此檔案位置" , "目標檔案位置")
* 目標檔案可不存在，複製內容：複製參數與權限
  > shutil.copy2("此檔案位置" , "目標檔案位置")

***

# pathlib 模組
* 引入 pathlib 模組
  > from pathlib import Path
* 檔案或目錄路徑
  > file = Path("檔案或目錄路徑")
* 檢查路徑是否存在
  > file.exists()
* 檢查路徑是否為檔案
  > file.is_file()
* 檢查路徑是否為目錄
  > file.is_dir()

***
# 參考資料：
* 【python內建模組- os/shutil】用python大量處理電腦上的檔案
  > https://ithelp.ithome.com.tw/articles/10229950
* Python清空指定文件夹下所有文件的方法
  > https://blog.csdn.net/qysh123/article/details/51923606
* [D29] 檔案批次處理 & shutil
  > https://ithelp.ithome.com.tw/articles/10226284
* Python中shutil模組的學習筆記教程
  > https://codertw.com/%E7%A8%8B%E5%BC%8F%E8%AA%9E%E8%A8%80/366324/
* Python 如何檢查檔案或目錄是否已經存在？
  > https://blog.gtwang.org/programming/python-howto-check-whether-file-folder-exists/
* pathlib --- 面向对象的文件系统路径
  > https://docs.python.org/zh-cn/3/library/pathlib.html
