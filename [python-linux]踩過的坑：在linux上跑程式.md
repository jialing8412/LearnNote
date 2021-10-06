# 套件安裝不了

### 因為 sever 是 python 2.7，但套件是新的版本(3.6)，安裝套件會失敗。

```python
conda deactivate # 先跳出(base)的狀態
wget https://docs.conda.io/en/latest/miniconda.html#linux-installers -> 3.7 64-bit
conda create -n py37 python==3.7
conda activate py37 # 創一個虛擬機
pip install -r requirements.txt # 安裝套件
pip install git+https://github.com/gregorias/samplerate.git

```

之後使用 conda activate py37 就能進去虛擬環境跑程式了。

* 參考資料：

  https://blog.csdn.net/hardhard123/article/details/113251805

----------

# 錯誤訊息

### SyntaxError: Non-UTF-8 code starting with '\xe5' in file PEP 263 -- Defining Python Source Code Encodings https://www.python.org/dev/peps/pep-0263/
* 解決方法：
  
  在各個python檔案最前面加上
  ```python
  #!/usr/bin/env python3
  # -*- coding: utf-8 -*- 
  ```


* 解決參考資料：

  https://www.python.org/dev/peps/pep-0263/

  http://ccfml.blogspot.com/2016/05/python.html

  https://www.itread01.com/content/1541743766.html

----------

### /usr/bin/env: ‘python2.7\r’: No such file or directory
* 解決方法：
  
  將程式以Nopade++開啟，在【檢視】->【特殊字元】->【顯示EOL】
  
  會發現換行部分全部都是CRLF
  
  ![image](https://user-images.githubusercontent.com/46884089/133062013-e9b24cc2-8900-4f4c-8e5b-4aba11083974.png)
  
  用取代的方式將\n\r取代為\n
  
  ![image](https://user-images.githubusercontent.com/46884089/133062268-62daee7e-75c0-4aa6-8171-5c1840d316d2.png)

  就會發現全部都改為LF，儲存檔案。
  
  ![image](https://user-images.githubusercontent.com/46884089/133062486-6d9a177b-ae9a-4a52-a38f-2ca7234d3260.png)




* 解決參考資料：

  https://ephrain.net/python-%E5%9F%B7%E8%A1%8C-python-%E6%AA%94%E6%A1%88%E5%87%BA%E7%8F%BE%E5%A5%87%E6%80%AA%E7%9A%84-env-pythonr-no-such-file-or-directory-%E8%A8%8A%E6%81%AF/
  
  http://sql313.com/index.php/43-main-blogs/maincat-dba/62-using-notepad-to-change-end-of-line-characters
  
  https://blog.csdn.net/NiYintang/article/details/86124338

