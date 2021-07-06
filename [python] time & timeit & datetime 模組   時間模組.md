# time 模組
藉由程式碼執行前後的時間戳記，就可以計算程式執行的時間。

取得目前的時間戳記
time.time()

    # 引入 time 模組
    import time

    # 開始測量
    start = time.time()

    # 要測量的程式碼
    for i in range(10000):
      "-".join(str(n) for n in range(100))

    # 結束測量
    end = time.time() 

    # 輸出結果
    print("執行時間：%f 秒" % (end - start)) 

***
# timeit 模組
專門用來測量 Python 程式碼執行效率的模組，通常會拿來快速比較不同 Python 寫法的效率差異。

    # 引入 time 模組
    import time

    # 開始測量
    start = time.process_time()

    # 要測量的程式碼
    for i in range(10000):
        "-".join(str(n) for n in range(100))

    # 結束測量
    end = time.process_time()

    # 輸出結果
    print("執行時間：%f 秒" % (end - start))

***
# datetime 模組

    # 引入 datetime 模組
    import datetime

    # 開始測量
    start = datetime.datetime.now()

    # 要測量的程式碼
    for i in range(10000):
        "-".join(str(n) for n in range(100))

    # 結束測量
    end = datetime.datetime.now()

    # 輸出結果
    print("執行時間：", end - start)

***
# 參考資料
* Python 測量程式碼執行時間教學與範例
  > https://officeguide.cc/python-measure-execution-time-tutorial-examples/
