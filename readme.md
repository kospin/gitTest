# 測試

每次都為了readme commit好多次  
想要刪除上一次或多次的commit  
可是一直無法在command llist中直接找到想要的方法  
最後在好的commit id新增branch 設成defaut接著幹  
再刪掉不要的那條branch  
可這樣branch name 就一直改,很煩  
而其實...

> git reset --hard [commit id]  
git push origin [branch name] --force

就可以把[branch name]還原回[commit id]狀態  
但中間的commit都會不見,使用還是要小心一點  
hard reset 應該是把工作區還原到 commit id 時  
然後 push --force 會比對有無沖突,沒的話就把branch定到commit id  
試著復原提交,修改完,暫存,再push --force 也是可以的

---

怎麼說呢,我覺得應該用聊天室或論壇來看待git  
而不是預期的檔案快照方式  
每個commit就是一個訊息送出  
每個branch就是一組聊天室記錄  
想改以前的留言..用rebase 從某個留言點開始參考留言記錄送出新的留言  
或用reset 回到某個留言時間後再發新的留言  
而push --force 就是告訴遠端,別想太多,用我的聊天室記錄就對了  
這樣想想,之前開新的branch接著幹才不會破壞本來的聊天室記錄,其實也是好的
