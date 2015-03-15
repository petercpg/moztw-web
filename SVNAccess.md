# 什麼是 SVN? #

請看 [Wikipedia](http://zh.wikipedia.org/w/index.php?title=SVN&variant=zh-tw)

# SVN 在 MozTW 裡用來幹嘛？ #

更新網站資料。所有 MozTW 的網站資料都在 https://opensvn.csie.org/moztw_web/ 公開，裡頭目錄比較重要的只有3個：
  * forum/ (討論區程式碼)
  * htdocs/ (moztw.org 網頁)
  * wiki/ (wiki 程式碼)

所以，你可以從 SVN 裡找到 moztw.org 網站原始碼。好比 http://moztw.org/events/firefox3party/ 這頁，實際上就位於 /htdocs/events/firefox3party/index.shtml

因此，若要協助修改，從 SVN 上抓檔案下來修最好了！

# 我怎麼幫忙？ #

這邊不會說明怎麼使用 SVN，你可以參考的的文件有：
  * [請加上連結](http://example.com)

通常最需要幫忙的是網頁更新，我們以 Firefox 例行更新時的版本資訊為例。在你沒有 SVN 寫入權時、假設現在要增加 3.0.3 版的版本資訊，步驟應如下：

  1. 如果你還沒有 checkout https://opensvn.csie.org/moztw_web/，那麼快動手吧
  1. 修改 htdocs/firefox/releases/index.shtml，比對更動內容修改 HTML 網頁。
  1. 如果可以，請 diff 原檔與新檔，方便得知你改了哪些地方
  1. 將 diff 檔 (或原檔) 上傳至 Google Code，等待管理員協助。

若你已經有寫入權，則步驟改為：
  1. 如果你還沒有 checkout https://opensvn.csie.org/moztw_web/，那麼快動手吧
  1. 接著在 htdocs/firefox/releases/ 下新開一個 3.0.3 的目錄
  1. 修改 htdocs/firefox/releases/index.shtml，比對更動內容修改 HTML 網頁。
  1. 儲存後，複製一份到 3.0.3 的目錄
  1. commit 進去時，記得將方才新增、修改的檔案都存進去
  1. auto\_update.php，執行後可以休息了

# 我怎麼將改好的網頁存進 SVN? #

請在 issue 裡開一個相對的 issue，說明你改了什麼、為何要改，接著上傳你要修改的檔案，然後等系統管理員協助你「上稿」。若有其他問題，也會在那個 issue 裡一併討論。

從修改到正式上稿或許會經過幾次來回修改。

若您長期協助 MozTW 修網頁、也贏得大家一定的信任。可以考慮申請 SVN 直接寫入權。

# 我怎麼申請 SVN 寫入權？ (commit) #

由於使用的工具問題，政策上 MozTW 將僅開放一小部份的人擁有寫入權限，所以並不是您申請了就可以寫入。如您有需要，請開一個新的 issue，並附上你貢獻的其他說明。