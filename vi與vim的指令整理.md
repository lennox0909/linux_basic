# vi 與 vim 的指令整理

vi 是 unix 家族下最功能強大的文字編輯器，讓用戶只要使用一個鍵盤就可以完成所有的編輯。而 <a href="http://www.vim.org/" target="_blank">vim</a> 則是 vi 的加強版，甚至在 <a href="http://www.vim.org/download.php#pc" target="_blank">Windows</a> 上也找得到 vim 的芳蹤。但 vi/vim 眾多的指令卻經常令初學者卻步，它的指令還有分大小寫，以下就是我所整理出來那些令人卻步的指令:
<p>(每一列前面若有 * 表示為常用的指令)<br />
<span id="more-234"></span></p>
<h3>編輯模式</h3>
<table border="1">
<tbody>
<tr>
<th></th>
<th>指令</th>
<th>說明</th>
</tr>
<tr>
<td>*</td>
<td>i</td>
<td>在游標位置進入編輯模式</td>
</tr>
<tr>
<td></td>
<td>I</td>
<td>在游標行的第一個非空白字元進入編輯模式</td>
</tr>
<tr>
<td>*</td>
<td>a</td>
<td>在游標位置後進入編輯模式</td>
</tr>
<tr>
<td>*</td>
<td>A</td>
<td>在游標行的最後一個字元進入編輯模式</td>
</tr>
<tr>
<td>*</td>
<td>o</td>
<td>向下新增一行，並進入編輯模式</td>
</tr>
<tr>
<td></td>
<td>O</td>
<td>向上新增一行，並進入編輯模式</td>
</tr>
<tr>
<td></td>
<td>cc</td>
<td>刪除游標行，並進入編輯模式</td>
</tr>
<tr>
<td>*</td>
<td><kbd>ESC</kbd></td>
<td>取消指令或退出編輯模式</td>
</tr>
</tbody>
</table>
<h3>游標移動</h3>
<table border="1">
<tbody>
<tr>
<th></th>
<th>指令</th>
<th>說明</th>
</tr>
<tr>
<td>*</td>
<td>gg</td>
<td>移到第一行</td>
</tr>
<tr>
<td>*</td>
<td>G</td>
<td>移到最後一行</td>
</tr>
<tr>
<td>*</td>
<td><em>行數</em> → G</td>
<td>移動到第 n 行</td>
</tr>
<tr>
<td></td>
<td>0</td>
<td>移動到該行最前面</td>
</tr>
<tr>
<td></td>
<td>$</td>
<td>移動到該行最後面</td>
</tr>
<tr>
<td></td>
<td><em>字數</em> → <kbd>Space</kbd></td>
<td>向右移動 n 個字元</td>
</tr>
<tr>
<td>*</td>
<td><em>行數</em> → <kbd>Enter</kbd></td>
<td>向下移動 n 行</td>
</tr>
</tbody>
</table>
<h3>標記與複製</h3>
<table border="1">
<tbody>
<tr>
<th></th>
<th>指令</th>
<th>說明</th>
</tr>
<tr>
<td>*</td>
<td>v</td>
<td>開始字串標記</td>
</tr>
<tr>
<td>*</td>
<td>V</td>
<td>開始行標記</td>
</tr>
<tr>
<td>*</td>
<td>v → <kbd>Ctrl</kbd> + <kbd>V</kbd></td>
<td>開始區塊標記</td>
</tr>
<tr>
<td>*</td>
<td>d</td>
<td>刪除標記的內容</td>
</tr>
<tr>
<td>*</td>
<td>y</td>
<td>複製標記的內容</td>
</tr>
<tr>
<td>*</td>
<td>yy</td>
<td>複製游標行</td>
</tr>
<tr>
<td></td>
<td>yG</td>
<td>複製游標行到最後一行</td>
</tr>
<tr>
<td></td>
<td>y1G</td>
<td>複製游標行到第一行</td>
</tr>
<tr>
<td></td>
<td>y$</td>
<td>複製游標處到最後一個字元</td>
</tr>
<tr>
<td></td>
<td>y0</td>
<td>複製游標處到第一個字元</td>
</tr>
<tr>
<td>*</td>
<td>p</td>
<td>在下一行貼上複製或刪除的內容</td>
</tr>
<tr>
<td></td>
<td>P</td>
<td>在上一行貼上複製或刪除的內容</td>
</tr>
<tr>
<td>*</td>
<td><kbd>Ctrl</kbd> + <kbd>R</kbd> → 0</td>
<td>在下一行貼上複製或刪除的內容，適用於編輯模式及指令行</td>
</tr>
</tbody>
</table>
<h3>搜尋與取代</h3>
<table border="1">
<tbody>
<tr>
<th></th>
<th>指令</th>
<th>說明</th>
</tr>
<tr>
<td>*</td>
<td>/<em>搜尋字串</em></td>
<td>向下搜尋字串</td>
</tr>
<tr>
<td></td>
<td>/\c<em>搜尋字串</em></td>
<td>向下搜尋字串，不分大小寫</td>
</tr>
<tr>
<td>*</td>
<td>*</td>
<td>將游標移到字串上，直接按 "*" 也可以做向下搜尋</td>
</tr>
<tr>
<td></td>
<td>?<em>搜尋字串</em></td>
<td>向上搜尋字串</td>
</tr>
<tr>
<td></td>
<td>?\c<em>搜尋字串</em></td>
<td>向上搜尋字串，不分大小寫</td>
</tr>
<tr>
<td>*</td>
<td>:set ic</td>
<td>搜尋時不分大小寫</td>
</tr>
<tr>
<td>*</td>
<td>:set noic</td>
<td>搜尋時要分大小寫</td>
</tr>
<tr>
<td>*</td>
<td>n</td>
<td>繼續下一個搜尋結果</td>
</tr>
<tr>
<td>*</td>
<td>N</td>
<td>繼續上一個搜尋結果</td>
</tr>
<tr>
<td>*</td>
<td>:<em>起始行</em>,<em>終止行</em>s/<em>搜尋字串</em>/<em>取代字串</em>/gic</td>
<td>從第 n 行到第 n 行取代字串 (後面的 g: 整行全部 i: 不分大小寫 c: 詢問)</td>
</tr>
<tr>
<td>*</td>
<td>:1,$s/<em>搜尋字串</em>/<em>取代字串</em>/gic</td>
<td>全部取代字串 (後面的 g: 整行全部 i: 不分大小寫 c: 詢問)</td>
</tr>
</tbody>
</table>
<h3>刪除</h3>
<table border="1">
<tbody>
<tr>
<th></th>
<th>指令</th>
<th>說明</th>
</tr>
<tr>
<td>*</td>
<td>dd</td>
<td>刪除游標行</td>
</tr>
<tr>
<td>*</td>
<td><em>行數</em> → dd</td>
<td>刪除 n 行</td>
</tr>
<tr>
<td>*</td>
<td>dG</td>
<td>刪除游標行到最後一行</td>
</tr>
<tr>
<td></td>
<td>d1G</td>
<td>刪除游標行到第一行</td>
</tr>
<tr>
<td>*</td>
<td>d$</td>
<td>刪除游標處到最後一個字元</td>
</tr>
<tr>
<td></td>
<td>d0</td>
<td>刪除游標處到第一個字元</td>
</tr>
</tbody>
</table>
<h3>檔案功能</h3>
<table border="1">
<tbody>
<tr>
<th></th>
<th>指令</th>
<th>說明</th>
</tr>
<tr>
<td>*</td>
<td>:w</td>
<td>存檔 (加 ! 表示強制存檔)</td>
</tr>
<tr>
<td>*</td>
<td>:w <em>檔案名稱</em></td>
<td>另存新檔</td>
</tr>
<tr>
<td>*</td>
<td>:q</td>
<td>退出 vi (加 ! 表示不存檔強制退出)</td>
</tr>
<tr>
<td>*</td>
<td>:wq</td>
<td>存檔並退出 vi</td>
</tr>
<tr>
<td>*</td>
<td>:<span id="x">x</span></td>
<td>存檔並退出 vi</td>
</tr>
<tr>
<td></td>
<td>:w !sudo tee %</td>
<td>當你編輯好檔案要存檔時，卻發現沒有寫入檔案的權限! 用這會指令可以讓你直接以 root 的權限存檔</td>
</tr>
<tr>
<td>*</td>
<td>:e <em>檔案名稱</em></td>
<td>編輯其它檔案</td>
</tr>
<tr>
<td>*</td>
<td>:e!</td>
<td>還原至檔案編修前的狀態</td>
</tr>
<tr>
<td></td>
<td>:r <em>檔案名稱</em></td>
<td>讀入檔案內容，並加到游標行的後面</td>
</tr>
<tr>
<td>*</td>
<td>:n</td>
<td>切換到下一個開啟的檔案</td>
</tr>
<tr>
<td>*</td>
<td>:N</td>
<td>切換到上一個開啟的檔案</td>
</tr>
<tr>
<td>*</td>
<td>:set nu</td>
<td>顯示行號</td>
</tr>
<tr>
<td>*</td>
<td>:set nonu</td>
<td>取消行號顯示</td>
</tr>
<tr>
<td>*</td>
<td>:files</td>
<td>列出所有開啟的檔案</td>
</tr>
<tr>
<td>*</td>
<td>:Ex</td>
<td>開啟檔案瀏覽器</td>
</tr>
<tr>
<td>*</td>
<td>:Ex <em>路徑</em></td>
<td>於指定路徑開啟檔案瀏覽器</td>
</tr>
<tr>
<td></td>
<td>:Hex</td>
<td>分割水平視窗後，再開啟檔案瀏覽器</td>
</tr>
<tr>
<td></td>
<td>:Vex</td>
<td>分割垂直視窗後，再開啟檔案瀏覽器</td>
</tr>
<tr>
<td></td>
<td>:Tex</td>
<td>新增頁籤後，再開啟檔案瀏覽器</td>
</tr>
<tr>
<td></td>
<td>:Hex <em>路徑</em></td>
<td>分割水平視窗後，再於指定路徑開啟檔案瀏覽器</td>
</tr>
<tr>
<td></td>
<td>:Vex <em>路徑</em></td>
<td>分割垂直視窗後，再於指定路徑開啟檔案瀏覽器</td>
</tr>
<tr>
<td></td>
<td>:Tex <em>路徑</em></td>
<td>新增頁籤後，再於指定路徑開啟檔案瀏覽器</td>
</tr>
</tbody>
</table>
<h3>視窗分割</h3>
<table border="1">
<tbody>
<tr>
<th></th>
<th>指令</th>
<th>說明</th>
</tr>
<tr>
<td>*</td>
<td>:new</td>
<td>新增水平分割視窗</td>
</tr>
<tr>
<td>*</td>
<td>:new <em>檔案名稱</em></td>
<td>新增水平分割視窗，並在新增的視窗載入檔案</td>
</tr>
<tr>
<td>*</td>
<td>:vnew</td>
<td>新增垂直分割視窗</td>
</tr>
<tr>
<td>*</td>
<td>:vnew <em>檔案名稱</em></td>
<td>新增垂直分割視窗，並在新增的視窗載入檔案</td>
</tr>
<tr>
<td></td>
<td>:sp</td>
<td>新增水平分割視窗，並在新增的視窗載入目前的檔案</td>
</tr>
<tr>
<td></td>
<td>:sp <em>檔案名稱</em></td>
<td>新增水平分割視窗，並在新增的視窗載入檔案</td>
</tr>
<tr>
<td></td>
<td>:vsp</td>
<td>新增垂直分割視窗，並在新增的視窗載入目前的檔案</td>
</tr>
<tr>
<td></td>
<td>:vsp <em>檔案名稱</em></td>
<td>新增垂直分割視窗，並在新增的視窗載入檔案</td>
</tr>
<tr>
<td>*</td>
<td><kbd>Ctrl</kbd> + <kbd>W</kbd> → <kbd>方向鍵</kbd></td>
<td>切換視窗</td>
</tr>
<tr>
<td>*</td>
<td>:only</td>
<td>僅保留目前的視窗</td>
</tr>
</tbody>
</table>
<h3>頁籤</h3>
<table border="1">
<tbody>
<tr>
<th></th>
<th>指令</th>
<th>說明</th>
</tr>
<tr>
<td>*</td>
<td>:tabe</td>
<td>新增頁籤</td>
</tr>
<tr>
<td>*</td>
<td>:tabe <em>檔案名稱</em></td>
<td>新增頁籤，並在新頁籤載入檔案</td>
</tr>
<tr>
<td></td>
<td>:tabc</td>
<td>關閉目前的頁籤，等同 :q</td>
</tr>
<tr>
<td></td>
<td>:tabo</td>
<td>關閉所有頁籤</td>
</tr>
<tr>
<td></td>
<td>:tabn</td>
<td>移至下一個頁籤</td>
</tr>
<tr>
<td></td>
<td>:tabp</td>
<td>移至上一個頁籤</td>
</tr>
<tr>
<td>*</td>
<td>gt</td>
<td>移至下一個頁籤</td>
</tr>
<tr>
<td>*</td>
<td>gT</td>
<td>移至上一個頁籤</td>
</tr>
<tr>
<td>*</td>
<td>:tabfirst</td>
<td>移至第一個頁籤</td>
</tr>
<tr>
<td>*</td>
<td>:tablast</td>
<td>移至最後一個頁籤</td>
</tr>
<tr>
<td>*</td>
<td>:tabm <em>頁籤編號</em></td>
<td>移至特定編號的頁籤 (編號從 0 開始)</td>
</tr>
<tr>
<td></td>
<td>:tabs</td>
<td>列出所有頁籤</td>
</tr>
</tbody>
</table>
<h3>其它指令</h3>
<table border="1">
<tbody>
<tr>
<th></th>
<th>指令</th>
<th>說明</th>
</tr>
<tr>
<td>*</td>
<td>J</td>
<td>將游標行與下一行合併</td>
</tr>
<tr>
<td>*</td>
<td>u</td>
<td>還原指令</td>
</tr>
<tr>
<td>*</td>
<td><kbd>Ctrl</kbd> + <kbd>R</kbd></td>
<td>重做指令</td>
</tr>
<tr>
<td>*</td>
<td><kbd>Ctrl</kbd> + <kbd>N</kbd></td>
<td>自動補齊曾輸入過的單字</td>
</tr>
<tr>
<td>*</td>
<td>.</td>
<td>重覆上一個指令</td>
</tr>
<tr>
<td></td>
<td>! <em>命令</em></td>
<td>執行 linux 指令，並顯示執行結果</td>
</tr>
<tr>
<td></td>
<td>TOhtml</td>
<td>將目前編輯的檔案轉換成 HTML 原始碼 (會新增一個水平分割視窗)</td>
</tr>
</tbody>
</table>
<h3>檔案瀏覽器操作</h3>
<p>請先以 :Ex 相關指令進入檔案瀏覽器</p>
<table border="1">
<tbody>
<tr>
<th></th>
<th>指令</th>
<th>說明</th>
</tr>
<tr>
<td>*</td>
<td>-</td>
<td>到上層目錄</td>
</tr>
<tr>
<td>*</td>
<td>d</td>
<td>建立目錄</td>
</tr>
<tr>
<td>*</td>
<td>D</td>
<td>刪除目錄</td>
</tr>
<tr>
<td>*</td>
<td>R</td>
<td>重新命名</td>
</tr>
<tr>
<td>*</td>
<td>s</td>
<td>切換排序方式</td>
</tr>
<tr>
<td></td>
<td>r</td>
<td>切換升冪/降冪排序</td>
</tr>
<tr>
<td></td>
<td>i</td>
<td>切換檔案的排列方式</td>
</tr>
<tr>
<td>*</td>
<td>/</td>
<td>搜尋字串</td>
</tr>
<tr>
<td></td>
<td>x</td>
<td>執行檔案</td>
</tr>
<tr>
<td>*</td>
<td>o</td>
<td>新增水平視窗</td>
</tr>
<tr>
<td>*</td>
<td>v</td>
<td>新增垂直視窗</td>
</tr>
</tbody>
</table>
<h3>vim 的設定檔</h3>
<p>通常我會編輯 /etc/vimrc，在檔案最後加入:</p>
<pre><span style="color: #008800;">" 顯示列號</span>
set number
<span style="color: #008800;">" 語法高亮度顯示</span>
syntax on
<span style="color: #008800;">" 標記搜尋到的字串</span>
set hlsearch
<span style="color: #008800;">" 自動縮排</span>
set autoindent
<span style="color: #008800;">" 顯示說明</span>
set ruler
<span style="color: #008800;">" 顯示編輯狀態</span>
set showmode
<span style="color: #008800;">" 設定註解的顏色</span>
highlight Comment ctermfg=cyan
<span style="color: #008800;">" 設定搜尋到的字串顏色</span>
highlight Search term=reverse ctermbg=4 ctermfg=7
<span style="color: #008800;">" 設定 tab 鍵的字元數</span>
set tabstop=4</pre>
