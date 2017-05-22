# 关于sublimeText3的一些用法

## 快捷键列表（Shortcuts Cheatsheet）

我把本文出现的Sublime Text按其类型整理在这里，以便查阅。

**通用（General）**

- ↑↓←→：上下左右移动光标，注意不是不是KJHL！
- Alt：调出菜单
- Ctrl + Shift + P：调出命令板（Command Palette）
- Ctrl + `：调出控制台

**编辑（Editing）**

- Ctrl + Enter：在当前行下面新增一行然后跳至该行
- Ctrl + Shift + Enter：在当前行上面增加一行并跳至该行
- Ctrl + ←/→：进行逐词移动
- Ctrl + Shift + ←/→进行逐词选择
- Ctrl + ↑/↓移动当前显示区域
- Ctrl + Shift + ↑/↓移动当前行

**选择（Selecting）**

- Ctrl + D：选择当前光标所在的词并高亮该词所有出现的位置，再次Ctrl + D选择该词出现的下一个位置，在多重选词的过程中，使用Ctrl + K进行跳过，使用Ctrl + U进行回退，使用Esc退出多重编辑
- Ctrl + Shift + L：将当前选中区域打散
- Ctrl + J：把当前选中区域合并为一行
- Ctrl + M：在起始括号和结尾括号间切换
- Ctrl + Shift + M：快速选择括号间的内容
- Ctrl + Shift + J：快速选择同缩进的内容
- Ctrl + Shift + Space：快速选择当前作用域（Scope）的内容

**查找&替换（Finding&Replacing）**

- F3：跳至当前关键字下一个位置
- Shift + F3：跳到当前关键字上一个位置
- Alt + F3：选中当前关键字出现的所有位置
- Ctrl + F/H：进行标准查找/替换，之后：
- Alt + C：切换大小写敏感（Case-sensitive）模式
- Alt + W：切换整字匹配（Whole matching）模式
- Alt + R：切换正则匹配（Regex matching）模式
- Ctrl + Shift + H：替换当前关键字
- Ctrl + Alt + Enter：替换所有关键字匹配
- Ctrl + Shift + F：多文件搜索&替换

**跳转（Jumping）**

- Ctrl + P：跳转到指定文件，输入文件名后可以：
- @ 符号跳转：输入@symbol跳转到symbol符号所在的位置
- \# 关键字跳转：输入#keyword跳转到keyword所在的位置
- : 行号跳转：输入:12跳转到文件的第12行。
- Ctrl + R：跳转到指定符号
- Ctrl + G：跳转到指定行号

**窗口（Window）**

- Ctrl + Shift + N：创建一个新窗口
- Ctrl + N：在当前窗口创建一个新标签
- Ctrl + W：关闭当前标签，当窗口内没有标签时会关闭该窗口
- Ctrl + Shift + T：恢复刚刚关闭的标签

**屏幕（Screen）**

- F11：切换普通全屏
- Shift + F11：切换无干扰全屏
- Alt + Shift + 2：进行左右分屏
- Alt + Shift + 8：进行上下分屏
- Alt + Shift + 5：进行上下左右分屏
- 分屏之后，使用Ctrl + 数字键跳转到指定屏，使用Ctrl + Shift + 数字键将当前屏移动到指定屏

## 安装Package Control

	> 打开控制台，粘贴下面的代码

```
import urllib.request,os,hashlib; h = '7183a2d3e96f11eeadd761d777e62404' + 'e330c659d4bb41d3bdf022e94cab3cd0'; pf = 'Package Control.sublime-package'; ipp = sublime.installed_packages_path(); urllib.request.install_opener( urllib.request.build_opener( urllib.request.ProxyHandler()) ); by = urllib.request.urlopen( 'http://sublime.wbond.net/' + pf.replace(' ', '%20')).read(); dh = hashlib.sha256(by).hexdigest(); print('Error validating download (got %s instead of %s), please try manual install' % (dh, h)) if dh != h else open(os.path.join( ipp, pf), 'wb' ).write(by)
```

- 等待Package Control安装完成。之后使用Ctrl + Shift + P打开命令板，输入PC应出现Package Control
- 选择Install Package
- 输入要安装的Package即可安装

## Sublime最佳插件汇总

### [WebInspector](https://github.com/sokolovstas/SublimeWebInspector)

调试JavaScript特别棒的工具，成熟的Sublime代码检测工具。产品特点：使用绝对路径，控制台，调试步骤和断点，堆栈跟踪，为存储在用户设置中的项目断点。瞬间起效！还有来自于Mozilla的Fireplay，它被允许连接到Firefox Developer工具和最简单的调试器JSHint。

### [Emmet](http://emmet.io/)

Sublime Text编辑器最受欢迎的插件之一。Emmet，前身为Zen Coding，也是提升web开发人员工作效率最有效的方法之一。按下Tab键后，Emmet可以将一些简短的缩略词转换成完整的HTML/CSS代码片段。另外，我想提一提Hayaku——一个实用的层叠样式表的缩写集合。

来自于项目作者的最佳技术展示视频：（需要自己找梯子）

http://www.youtube.com/embed/sxW-V24MTXI?feature=player_embedded

### [Git](https://github.com/kemayo/sublime-text-git)

从它的名字我们就可以看出这个插件的本质——让你在自己喜欢的编辑器中直接使用Git。这种使用Git的方法可以为你节省很多时间。第一：你不必总是在Sublime和终端之间不断切换。第二：有一个很好的自动完成标签，不需要像git输入add-A，写add即可。第三：有类似Quick commit功能的东西，能够一键添加所有的改变并提交它们。

如果你只需要从Git获取远程仓库中的内容的话，那么我建议[Nettuts+ Fetch](https://sublime.wbond.net/packages/Nettuts%2B%20Fetch).。

还有Glue，在位于底部的小窗口中展示，可以让你写在Shell上。出于这个原因，现在你的编辑器已经不再局限于Git…

### [GitGutter](https://github.com/jisaacks/GitGutter)&[Modific](https://github.com/gornostal/Modific)

这些插件会高亮上次提交的更改行，换言之就是实时的比较工具。

![40+ Sublime Text 最佳插件汇总](http://static.open-open.com/news/uploadImg/20151229/20151229095341_578.png)

### [BracketHighlighter](https://sublime.wbond.net/packages/BracketHighlighter)

棒极了！打开和关闭任何部分的代码看起来应该是这样的。

![40+ Sublime Text 最佳插件汇总](http://static.open-open.com/news/uploadImg/20151229/20151229095342_755.jpg)

### [EditorConfig](https://github.com/sindresorhus/editorconfig-sublime)

![40+ Sublime Text 最佳插件汇总](http://static.open-open.com/news/uploadImg/20151229/20151229095343_175.png)

EditorConfig帮助开发人员定义和维护在不同编辑器和IDE之间的一致性编码风格。EditorConfig项目包括定义编码风格的文件格式和文本编辑器插件集合，这些插件能够让编辑器读取文件格式，并坚持被定义的样式。 .editorconfig文件的例子：

### [Sublimall](https://sublimall.org/)

同步Sublime Text编辑器之间所有配置（设置，插件，打开的文件，等）的一个灵巧的插件。一切都是免费的，你只需要创建一个帐户即可。它的一个简单的替代品是BufferScroll。

![40+ Sublime Text 最佳插件汇总](http://static.open-open.com/news/uploadImg/20151229/20151229095344_497.png)

### [AllAutocomplete](https://github.com/alienhard/SublimeAllAutocomplete)

Sublime Tex中的经典自动补全，只适用于当前文件。AllAutocomplete在当前窗口的所有打开文件中搜索可以大大简化开发过程。还有CodeIntel，具体化了IDE的功能，并为若干语言带来了“代码智能”，这些语言包括：JavaScript，Mason，XBL，XUL，RHTML，SCSS，Python，HTML，Ruby，Python3，XML，Sass，XSLT，Django，HTML5，Perl，CSS，Twig，Less，Smarty，Node.js，Tcl，TemplateToolkit，PHP。

![40+ Sublime Text 最佳插件汇总](http://static.open-open.com/news/uploadImg/20151229/20151229095344_178.png)

### [SublimeREPL](https://github.com/wuub/SublimeREPL)

也许，这是开发者最有用的插件之一。 SublimeREPL直接在编辑器中运行适用于许多许多语言的解释程序，这些语言包括：Clojure，CoffeeScript，F#，Groovy，Haskell，Lua，MozRepl，NodeJS，Python，R，Ruby，Scala，shell。

![40+ Sublime Text 最佳插件汇总](http://static.open-open.com/news/uploadImg/20151229/20151229095345_789.png)

### [DocBlockr](https://github.com/spadgos/sublime-jsdocs)

DocBlockr可成为你文档化代码的高效工具。输入/ **，然后按Tab键，该插件就会自动解析任何功能，并准备合适的模板。

![40+ Sublime Text 最佳插件汇总](http://static.open-open.com/news/uploadImg/20151229/20151229095346_686.png)

### [Floobits](https://floobits.com/)

适用于SublimeText，[vi](http://www.codeceo.com/article/vi-editor-guide.html)m，Emacs，IntelliJ IDEA非常棒的扩展，它允许开发人员在代码上以及不同编辑器之间的协作。

![40+ Sublime Text 最佳插件汇总](http://static.open-open.com/news/uploadImg/20151229/20151229095347_241.jpg)

### [AutoFileName](https://github.com/BoundInCode/AutoFileName)

自动完成文件路径——非常方便。所以就不说废话了。

![40+ Sublime Text 最佳插件汇总](http://static.open-open.com/news/uploadImg/20151229/20151229095347_992.jpg)

### [ColorPicker](http://weslly.github.io/ColorPicker/)

通常情况下，当我们需要调色板的时候，我们习惯于使用Photoshop或Gimp。但完整的拾色器可以直接在编辑器中使用——Ctrl/Cmd + Shift + C。还有很棒的GutterColor 喝ColorHighlighter，能够简化颜色代码中的取向：

![40+ Sublime Text 最佳插件汇总](http://static.open-open.com/news/uploadImg/20151229/20151229095348_211.png)

### [Colorcoder](https://github.com/vprimachenko/Sublime-Colorcoder)

高亮所有的变量，从而显著简化代码中的取向。尤其适用于有阅读障碍的开发人员。

[![40+ Sublime Text 最佳插件汇总](http://static.open-open.com/news/uploadImg/20151229/20151229095349_0.jpg)](http://static.codeceo.com/images/2015/12/stp11.jpg)

### [PlainTasks](https://github.com/aziz/PlainTasks)

超棒的待办事项列表！所有任务都存储在文件中，因此绑定任务到合适项目非常方便。它可以创建项目，分配标签，设置日期。超棒的用户界面和快捷键。

![40+ Sublime Text 最佳插件汇总](http://static.open-open.com/news/uploadImg/20151229/20151229095349_905.png)

### [MarkdownEditing](https://github.com/ttscoff/MarkdownEditing)

也许，这是用Markdown工作的最好插件，它拥有多种功能：语法高亮，缩写，自动完成，配色方案，等等。你也可以尝试MarkdownPreview当作替代的解决方案。

![40+ Sublime Text 最佳插件汇总](http://static.open-open.com/news/uploadImg/20151229/20151229095350_239.png)

## 再来一波实用插件

[Sublime SFTP](http://wbond.net/sublime_packages/sftp)
[CTags](https://github.com/SublimeText/CTags) - CTags支持Sublime.
[SideBarEnhancement](https://github.com/titoBouzout/SideBarEnhancements) - 在侧边栏的上下文菜单中有许多附加功能。
[ActualVim](https://github.com/lunixbochs/actualvim) - Sublime中的Vim - 集两个最喜欢的编辑器于一体。
[SublimeLinter](http://github.com/SublimeLinter/SublimeLinter) - C/C ++，Java，Python，PHP，JS，HTML，CSS等的内联lint高亮。
[CSScomb](https://github.com/csscomb/sublime-csscomb) - CSS编码风格格式器。
[FixMyJS](https://github.com/jshint/fixmyjs), [Jsfmt](https://github.com/paulirish/sublime-jsfmt) and [JsFormat](https://github.com/jdc0589/JsFormat) - JS / JSON的编码风格格式器。
[AStyleFormatter](https://github.com/timonwong/SublimeAStyleFormatter) - C / C ++ / C＃/ Java编码风格格式器。
[SVG-Snippets](https://github.com/jorgeatgu/SVG-Snippets) - 设置自定义的SVG片段。
[Inc-Dec-Value](https://github.com/rmaksim/Sublime-Text-2-Inc-Dec-Value) - 增加/减少数字，日期，十六进制颜色值，等等。
[Trailing Spaces](https://github.com/SublimeText/TrailingSpaces) - 高亮尾部的空格，并在瞬间将其删除。
[Alignment](http://wbond.net/sublime_packages/alignment) - 多行选择和多项选择超简单的对齐。
[Placeholders](https://github.com/mrmartineau/Placeholders) - 文字，图片，列表，表格等的片段集合。
[ApplySyntax](https://github.com/facelessuser/ApplySyntax) - 快速检测语法。
[StylToken](https://github.com/vcharnahrebel/style-token) - 允许用不同的颜色高亮某些文本片段（类似notepad++的“Style token”功能）。
[EasyMotion](https://github.com/tednaleid/sublime-EasyMotion) - 快速跳转到活跃视图可见区域中的任何字符。
[ZenTabs](https://github.com/travmik/ZenTabs) 和 [AdvancedNewFile](https://github.com/skuroda/Sublime-AdvancedNewFile) -提高默认选项卡的外观和文件创建。
[EncodingHelper](https://github.com/SublimeText/EncodingHelper) - 猜测文件的编码，显示在状态栏上，将各种编码转换为UTF-8。
[Gist](https://github.com/condemil/Gist) - 用Sublime (ST2)同步GitHub Gist。
[Clipboard History (ST2)](https://github.com/kemayo/sublime-text-2-clipboard-history) - 保持剪贴板项目的历史。

## 主题和颜色方案:

[Soda](http://buymeasoda.github.io/soda-theme/)
[Spacegray](http://kkga.github.io/spacegray/)
[Flatland](https://github.com/thinkpixellab/flatland)
[Tomorrow](https://github.com/chriskempson/tomorrow-theme)
[Base 16](https://github.com/chriskempson/base16)
[Solarized](http://ethanschoonover.com/solarized)
[Predawn](https://github.com/jamiewilson/predawn)
[itg.flat](https://sublime.wbond.net/packages/Theme%20-%20itg.flat)
适用于所有其他偏好 [Color Schemes](https://github.com/daylerees/colour-schemes) 和[Сolorsublime](http://colorsublime.com/).

