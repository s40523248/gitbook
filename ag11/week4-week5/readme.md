# WEEK 4
老師開始要求每一分組成員必須在各自的分組倉儲中至少提供一則 mp4 簡報或操作流程示範影片, 說明該週的工作內容、進度與心得報告, 並且將紙本筆記的內容整理到各組的 gitbook 線上報告中

介紹 lua 網頁程式

下載課程所需軟體kmol_level2並將模組升級為 5.7 final然後解開壓縮檔案, 換掉 Python36/Lib/site-packages 目錄中的 leo 目錄

V-rep 升級為 V-REP PRO EDU V3.5.0 rev3

在課堂利用空餘時間搜尋lua教學 並學習如何使用lua基本語法 lua 迴圈 lua函式

參考文獻 :https://cwchen.tw/lua-prog/intro/

http://www2.kimicat.com/lua%E6%95%99%E5%AD%B8--%E5%87%BD%E5%BC%8F

影片https://youtu.be/ypWIlswYNe8

# week5

第一節進行點名
缺課名單

W7a第一節點名時未到者：
40523105

40523109

40523112

40523115

我還在睡

母湯

40523121

40523125

40523131

40523140

40523142

40523144

40523148

利用Python3找出缺席名單

with open("cd_w7a.txt", "r", encoding="utf-8") as fh:
   
   # 逐行讀出檔案資料, 並放入數列中

    lines = fh.readlines()

    raw_data = lines[1:]

    #print(raw_data)

    # 設法用迴圈逐數列內容取出字串

    # k 為集合所有檔案中的學號字串, 先設為空字串

    k = []

    for i in range(len(raw_data)):

        # 利用 strip() 去除各行字串最末端的跳行符號

        raw_line = raw_data[i].strip()

        # 利用 split() 將以 \t 區隔的字串資料分離後納入 groups 字串

        groups = raw_line.split("\t")

        #print(groups)

        # 逐一進入各行中的各字串去除空字串

        for j in range(len(groups)):

            if groups[j] != "":

                # 除了空字串外, 其餘字串放入 k 數列中

                k.append(groups[j])

      absent = [x for x in k if k.count(x) == 1]

      print(absent)

結果如下：
['40523105'，'40523109'，'40523112'，'40523115'，'40523121'，'40523125'，'40523131'，'40523140'，'40523142'，'40523144'，'40523148']
