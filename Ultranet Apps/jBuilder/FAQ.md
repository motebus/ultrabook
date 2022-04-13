# 常見問題

-> [English Version](#FAQs)

---

## Q 為什麼我使用 page://url 加上的網站在“Preview”模式只能顯示“拒絕連線”？
該網站的創建者可能設置了 iFrame 嵌入位置限制，建議您找別網站使用

---

## Q 為什麼我的 Youtube 影片無法播放？
請檢查您的視頻網址格式是否正確，如 https://www.youtube.com/watch?v=VIDEOID。 其他格式 https://youtu.be/VIDEOID 和 https://www.youtube.com/shorts/VIDEOID 將無法正常顯示。<br>
有些 YouTube 影片（尤其是來經過官方驗證頻道的視頻）有嵌入限制，建議您找別的影片使用

---

## Q 為什麼我的 board 加到 Dock Builder 上的 jBoard後，在“預覽”模式下格式變了？
如果 board 中使用 page://slider 或 page://chart 會出現這個問題。bug 仍在修復中~ 

---

## Q 為什麼我的 jBoard 顯示的內容看起來與我製作編輯的的完全不同。
jBoard QName 可能已被其他人使用。 https://git.page/jj/board?qname=XXX 或 https://jboard.ypcloud.com/?q=XXX  將顯示的版本會是最新更新儲存的 QName=XXX 的 jBoard。建議避免使用您知道已經被用過的名稱或常見的"test","demo"等QName。

註：除了 QName, jBoard 也有 QCode 的ID可使用。 可以使用 https://git.page/jj/board?qname=XXX 或 https://git.page/jj/board?qcode=ZZZ 的 URL 查看您的 jBoard。 Qcode 可以在 Board List 中查詢。

---

# FAQs
## Q Why does the website I've added using `page://url` show up in "Preview" mode as "refused to connect"?
The creators of the website have likely set iFrame restrictions for where the website content can be embedded. There's not much you can do (unless you have access to changing the settings for this website), so we suggest just finding an alternative website to use. 

---

## Q Why can't the Youtube video I've added be played?
  1. Please check that your video url is in the correct format, e.g. https://www.youtube.com/watch?v=VIDEOID. Other formats such as  https://youtu.be/VIDEOID and https://www.youtube.com/shorts/VIDEOID will not be displayed normally. 
  2. Some YouTube videos (especially those from verfied official channels) have embedding restrictions. You'll have to find another video to use.

---

## Q Why  the layout of my board (added to a jBoard on Dock Builder) changed? My content has disappeared in "Preview" mode. 
  This problem is expected if your board contains page://slider or page://chart. These app panel types are currently still being fixed.

---

## Q Why does my jBoard display content that I haven't added? It looks entirely different from what I've been working on. 
  The jBoard QName has likely been used by someone else. https://git.page/jj/board?qname=XXX or https://jboard.ypcloud.com/?q=XXX will show the most recently updated/saved version of jBoards with the QName `XXX`. It's good practice to avoid using general names or ones you know have already been used. 

Extra info: 
QName isn't the only ID for your jBoard. In addition to https://git.page/jj/board?qname=XXX, your board can also be viewed using its Qcode via the url https://git.page/jj/board?qcode=ZZZ. The qcode of your jBoard can be found on the Board List. 
