# Troubleshooting FAQs 

#### Why does the website I've added using `page://url` show up in "Preview" mode as "refused to connect"?
The creators of the website have likely set iFrame restrictions for where the website content can be embedded. There's not much you can do (unless you have access to changing the settings for this website), so we suggest just finding an alternative website to use. 

---

#### Why can't the Youtube video I've added be played?
  1. Please check that your video url is in the correct format, e.g. https://www.youtube.com/watch?v=VIDEOID. Other formats such as  https://youtu.be/VIDEOID and https://www.youtube.com/shorts/VIDEOID will not be displayed normally. 
  2. Some YouTube videos (especially those from verfied official channels) have embedding restrictions. You'll have to find another video to use.

---

#### Why has the layout of my board (added to a jBoard on Dock Builder) changed? My content has disappeared in "Preview" mode. 
  This problem is expected if your board contains page://slider or page://chart. These app panel types are currently still being fixed.

---

#### Why does my jBoard display content that I haven't added? It looks entirely different from what I've been working on. 
  The jBoard QName has likely been used by someone else. https://git.page/jj/board?qname=XXX or https://jboard.ypcloud.com/?q=XXX will show the most recently updated/saved version of jBoards with the QName `XXX`. It's good practice to avoid using general names or ones you know have already been used. 

Extra info: 
QName isn't the only ID for your jBoard. In addition to https://git.page/jj/board?qname=XXX, your board can also be viewed using its Qcode via the url https://git.page/jj/board?qcode=ZZZ. The qcode of your jBoard can be found on the Board List. 

