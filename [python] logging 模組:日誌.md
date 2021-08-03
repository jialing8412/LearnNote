開發 Python 時，很常使用 print() 來輸出變數以方便 debug，

但要部署時，不需要這些訊息，需要自己手動去註解或刪除那些放在各處的 print()。

Python 內建提供 logging 模組可用來取代 print()，logging 除了可以輸出訊息，也可以將訊息儲存至日誌檔保存。

    import logging

    FORMAT = '%(asctime)s %(levelname)s: %(message)s'
    logging.basicConfig(level=logging.DEBUG, filename='myLog.log', filemode='w', format=FORMAT)

    logging.debug('debug message')
    logging.info('info message')
    logging.warning('warning message')
    logging.error('error message')
    logging.critical('critical message')

***

# 參考資料
* Python - 日誌 (logging) 模組
  > https://titangene.github.io/article/python-logging.html
