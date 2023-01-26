# Difficult Rocket Update Logs

- 感谢 `Github copilot` 的翻译(甚至这句话也是`copilot`翻译的)
  - 也就意味着以后的更新日志是中文记录+`copilot`翻译的(当然，也有可能是`Easy Translate`翻译的)
- Thanks `Github copilot` for translate (lazy yes!)
  - Means the update logs will lodge in Chinese and translated by `copilot`
- 可惜啊，github copilot 收费了


## Readme First!
##### most badge can be clicked and jump
[![Generic badge](https://img.shields.io/badge/SemVer-2.0.0-blue.svg)](https://Semver.org/)
![Generic badge](https://img.shields.io/badge/Version-0.6.5.0-yellow.svg)

- [![Readme-github](https://img.shields.io/badge/Readme-Github-blue.svg?style=flat-square&logo=Github)](https://github.com/shenjackyuanjie/Difficult-Rocket)
- [![Readme-gitee](https://img.shields.io/badge/Readme-Gitee-blue.svg?style=flat-square&logo=Gitee)](https://gitee.com/shenjackyuanjie/Difficult-Rocket)
- [![Readme-gitee](https://img.shields.io/badge/Readme-中文(点我!)-blue.svg?style=flat-square)](../../README.md)
- Using [SemVer 2.0.0](https://semver.org/) to manage version

## 202301 V 0.7.0

### 啊哈！ 现在真就是 0.7 了

### Add

- `libs.Difficult_Rocket_rs` (`DR_rs`) `0.1.0.0`
  - `get_version_str`
    - 返回 `DR_rs` 的版本号 可以用于检查我有没有忘记跑 `after_build.py`
    - 别问为啥不是返回一个 `Version` 对象 问就是懒得转换
  - `better_update_pats`
    - 用于优化 `SR1ShipRender.update_parts` 的性能
      - ( Python 原生的 for 循环真慢 )
  - `PartDatas`
    - 用于在 `PyObj` 里  暗 渡 陈 仓  装 `HashMap<uszie, SR1PartData>`

### 命令

- 有点尴尬，`sr1` 的命令不大好使，改成 `debug` 了
- `render`
  - `reset`
    - 用于重置现在这艘船的渲染 (避免你玩着玩着把船玩道不知道什么地方去了)

## 20230120 V 0.6.5.0

### 抱歉，我撒谎了（

0.6 还得来几个版本号

### Add

- 现在将文件拖拽至屏幕内可以渲染默认船只/渲染拖拽上来的解析成功的第一艘船
- 可以使用类似 SR1 的方式拖拽界面

### 命令行

- `stop`
  - 关闭游戏
- `fps`
  - `log`
    - 输出 fps 信息
  - `min`
    - 输出 最近 5s 的最小 fps
  - `max`
    - 输出 最近 5s 的最大 fps
- `default`
  - 将窗口大小恢复成默认
- `render`
  - 渲染 默认船只
- `sr1`
  - 下面的选项都是 DEBUG 用，不保证以后继续保留
  - `delta`
    - 渲染 SR1 渲染的偏移量
    - `mouse`
      - 渲染 SR1 渲染的鼠标偏移量
      - `delta`
        - 渲染 SR1 渲染的鼠标前进偏移量

### 优化(代码层面)

- 改掉了 `CommandText` 里的离谱代码
- 优化了 `tools.load_file` 的逻辑（其实是几个版本之前的改动
- `CommandText.match` -> `CommandText.re_match`
- 感谢 @caffe 的 pyglet `macosx` 分支
- 暂未实装
  - `Translates` 的优化
    - 以后多语言用起来会更方便
  - `Tr` 的优化
    - 跟 `Translates` 配套
  - `Difficult_Rocket_rs`
    - DR 的 Rust 优化
    - 基于 `pyo3`

## 20221124 V 0.6.4

### 最后的 0.6 呢

### Add

- `Logger!`
- nuitka 文档
- 准备给我的 5600x 的散热器洗一洗（
- 一些 client
- `Github Action` 的自动 build

### Changes

- 将 `utils.translates` 中的字体名称常量移动至 `api.types.Fonts` 中
- 删除了 `README-cn.md` ( 合并到 `README.md` 中 )
- 将 `README.md` 与 `README-en.md` 的内容统一
- 重新调整 `requirement.txt` 的内容 ( 使内容更加有条理性 )
- 删除了一些无用的代码 ( For second-dev )
- 更新了 `Toml` 文件 ( 使其更加规范 )
- 更新了 `screen api`
- 更新了 `pyglet` 版本
- 删除了 `main.config`
- 更新了 `logger`
- 更新了 `nuitka.yml`
- 尝试加载 `icon`
- 更新了主项目

## 20220627

## 20220511 V 0.6.3

- 咕了好久的 update log 了
- github copilot 卒了，所以没有英文
  - GitHub copy alot break , so no more English

### Change

- 将 `api/Exp` 改为文件夹 `api/Exp/__init__.py`
- 再次重写了 `client.load_fonts()` 现在改为直接加载单独的 `pyglet_load_fonts_folder()`
- 更新了 `command/` 里的一大堆东西
- 退钱！开摆！



## 202202xx V 0.6.2

### Add

[然后就很快被替换成MCDR的了]: <> (- 添加模块 `semver` 和协议 &#40;`LICENSE.txt`&#41;)
[Add soon been replace by MCDR]: <> (  - Add modules `semver` Add LICENSE &#40;`LICENSE.txt`&#41;)
- 添加了 `libs.MCDR` 文件夹 (`new_thread`没有包含在内)
  - Add `libs.MCDR` folder (`new_thread` not included)
- 添加对 mod 的支持(还在写啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊啊)
- 计划写个设计文档
  - Plan to write a design document


## ~~202111 202112xx 20220119~~ 20220207 V 0.6.1

~~争取12月内发一个release~~

~~行了，这都2022年了，我接着摸，等我考完试(20220110)再发~~

20220207 可算是发了，ruaaaa

### Change

- 修改了 readme 文件的语言切换格式
  - Change the language switch format in readme
- 更新了所有文件的版权信息 (2021-2022)
  - Update all files copyright information (2021-2022)
- 重命名 `Difficult_Rocket.py` -> `DR.py`
  - 用于修复 `Pycharm` 检测模块时总是会把主文件检测成主程序，导致一些模块总是检测不到的问题
    - Rename `Difficult_Rocket.py` -> `DR.py`
    - Use it to fix `Pycharm` module detection problem
      - When the main file is detected as the main program, some modules will always be detected as the main program
- 把`api/translate`移动到根目录下
  - move `api/translate` to root directory
- 现在命令会慢慢消失，而不是立即消失
  - Now the command will disappear slowly, not immediately
- 重写了一遍` client.load_fonts()`
  - rewrite `client.load_fonts()`
- 重写了 `tools.load_file()` 的错误处理和 `.config` 文件的解析方式
  - 现在 `.config` 文件解析后会直接返回一个 `ConfigParser` 对象
  - 也就意味着不能再直接遍历 `.config` 文件返回的解析 ~~谁遍历.config文件啊~~
  - 同时也意味着可以直接用解析好的 `.config` 文件来修改 `.config` 文件
    - rewrite `tools.load_file()` error handling and `.config` file parsing method
      - now `.config` file parsing after return `ConfigParser` object
      - that means you can not directly traverse `.config` file return parsing ~~who traverse .config file~~
      - also means you can directly use parsed `.config` file to modify `.config` file
- 为 `pyglet` 添加 `Ctrl+C` 和 `Ctrl+V` 的快捷键解析
  - add `Ctrl+C` and `Ctrl+V` shortcut for `pyglet`
- 更新 `pyglet` 到 `2.0dev13`
  - update `pyglet` to `2.0dev13`

### Command

- `log_tick` 指令改为 `fps log`
  - command `log_tick` change to `fps log`
- `maxfps` 指令改为 `fps max`
  - command `maxfps` change to `fps max`
- `minfps` 指令改为 `fps min`
  - command `minfps` change to `fps min`

- 命令内容输出使用`CommandText`而不是`str`
  - 也就是说可以使用`CommandText.match`来匹配命令内容
  - command output use `CommandText` instead of `str`
    - means you can use `CommandText.match` to match command content
- 命令解析现在使用新的`CommandText.match`
  - command parse now use new `CommandText.match`

### Add

- 添加内置字体`Cascadia_Code`
  - add built-in font `Cascadia_Code`
- 添加模块 `xmltodict` `pyperclip`
  - add modules `xmltodict` `pyperclip`
- 添加了`json5` `pyglet` `pyperclip` `xmltodict` 的协议
  - 非常感谢上述模块的作者和维护者们
  - added `json5` `pyglet` `pyperclip` `xmltodict` LICENSE
    - thanks a lot to above module's author and maintainer
- 继续~~重~~新写了一个基于 `HTMLLabel` 的 `HTMLformatedLabel`
  - 同时为他写了一个 `decode_text2HTML` 工具(这也是咕咕咕的一大部分原因)
  - add a `HTMLformatedLabel` Label based on `HTMLLabel`
    - also write a `decode_text2HTML` tool (also a big reason why lazy)
- 增加内置模块 `toml` 和对应的 `LICENSE.txt`
  - Added built-in module `toml` and corresponding `LICENSE.txt`


## 20211025 V 0.6.0

#### Command Line Update!

### Change

- 现在 `Difficult Rocket` 只适用于 python3.8+
  - 因为 `:=` 的使用
  - now `Difficult Rocket` will only fit python3.8+
    - because `:=`
- 现在主程序崩溃时的报告处理方式有了新的方式
  - now main crash report handler have new way to handler crash
- 现在字体文件夹的名字改为 `HarmonyOS_Sans`
  - now fonts' folder's name is `HarmonyOS_Sans`

### Add

- `Difficult_Rocket.graphics.widgets.Parts`
  - have many costume value
- now `libs/fonts` have `HarmonyOS_Sans` font
- handler of `on_key_press` and `on_key_release` and `on_text`
  - `on_key_press` 和 `on_key_release` 和 `on_text` 的处理方式
- `game.config` config file
- `lang/en-us.json5` now up to date with `lang/zh-CN.json5`
- `translate/Lang.翻译` same as `Lang.lang`
- `command/CommandLine` to render command line
- `@new_thread` now can option if log this thread to `crash` or not
- `start.cmd` witch could debug easier

### Translate

- Add
  - `window`
    - `message.text`
    - `command.text`
    - `text.motion`
    - `text.motion_select`
    - `setup.use_time_ns`
    - `fonts.found`
    - `game.input_stop`
    - `game.command_stop`
    - `game.window_stop`
    - `game.stop_get`
    - `game.stop`
    - `game.end`
  - `client`
    - `setup.use_time_ns`

### Command

- now you can press `t` to call out a message window
  - or press `/` to open command line
  - not done
  - ~~useless until now~~
- new command
  - `/min_fps`
    - get min fps in 5 second
  - `/max_fps`
    - get max fps in 5 second
  - `/stop`
    - stop the game
  - `/default`
    - switch window size to default size


## 20210928 V 0.5.2

### Change

- now bin folder use the name `Difficult_Rocket`
- now test files no longer have `_test_` prefix
- now will always use local `pyglet` 
  - may change later
- fitting `pypy3.10` (well······ not success (because OpenGL, blame it))
- now `crash-report` have more information
- now when pressed, the sprite will rotate randomly
- now `pyglet.app.run()` use multiprocess
- now will always use `libs/` lib when using `pyglet` or `json5`
- now `tools.config()` is `tools.load_file()`
- now `lang` file have `server``client` and `window`

### Add

- ~~mods support will be done in 1.0.0~~
  - just maybe
- now you can use `DEBUGGING` to test or check game run stats
  - when `True` it will always make a crash report
- now `Difficult_Rocket.api.translate.Lang` can be used to auto translate text in `configs/lang/xxx.json5`
  - you can use `translate.tr[xxx]` to use translated info
  - and use `.format` to format info's `{}`
  - if translate is not found, `Lang` will try to find translate in default language translate
  - (witch was `zh-CN`)
- `crash` now have more information about multiprocess
- add some unused read_input in `client`
- now when `logs/` is not found logger will info `logger.mkdir`

### DEBUG

- now version on the window will be `0.5.2`

### Delete

- now `client.Client` and `server.Server` only use `net_mode` option
- `api.new_thread` have no more extra line of testing
- `configs/view.json5` now removed

### Translate

- add `mouse.release` and `language` to en-us
- add `language` to `zh-CN`
- add `tr.lang(xx, xx)` that can solve error on getting item from lang file
  - `tr[xxx]` can also use but won't solve error when item not found
  - so best use `tr.lang(xx, xx)`


## 20210902 V 0.5.1

### Change

- crash report's format
- crash report now use multithreading!
- some info in `client`
- `tools/format_bool` now use more clever way to format

### Add

- `on_resize(self, width, height):` in `client`
- auto crash report in `bin/crash/create_crash_report`
- `bin/api/Exp.py` some Exception
- `bin/api/translate` to create a `translate` class that can reload language


## 20210823 V 0.5.0

### Change

- many `sys.path.append()` and
- `try: import xxx except: from bin import xxx` has been removed
- and now IDE won't blame you when you open the file anymore!(LOL)
- `Server` now use Dev to delivery message between thread(will be done in 0.6.0)
- test files now use `_test_*.py` for names

### Add

- `crash.py` to handle and create crash report (not done)
- `DragSprite` (maybe will add in future pyglet update PR has been published)

### Delete

- `name_hanlder` in `configs.py`


## 20210811 V 0.4.6

### DEBUG

- game window doesn't use input `(*args, **kwargs)` to set up

### Change

- language type `zh-cn` -> `zh-CN`
- game window config now use `configs/main.config` to config
- `on_mouse_click` function's debug message now use `self.lang` to debug message (witch is multi-language)
- server client and main now use `logging.getLogger()`

### Add

- `[window_default]` in `configs/main.config`
- server and client now will output `PID` and `PPID` info as `INFO`
- `client` now change to `ClientWindow`

### Delete

- all game window render has been deleted
    - will be rewritten in 0.5.0
- delete some useless code
- delete some useless file


## 20210723 V 0.4.5

### DEBUG

- `new_thread.py` link of stackoverflow have an extra 'find' in the middle REMOVED

### Add

- `new_thread.py` now can use @new_thread to get a threaded fun

### Change

- `README.md` and `README-cn.md` change URL to file path
- `README.md` and `README-cn.md` some label style change
- Pre-installed `pyglet` upgrade from `1.5.16` -> `1.5.18`
- Pre-installed `json5` upgrade from `0.9.5` -> `0.9.6`


## 20210708 V 0.4.4

### PS

- Nice day everyone!
- I have finish my final exam on grade 8.
- Will soon reach grade 9, so update will be late very much.

### Change

- function `tools.config()` way of raise error change `tools.report_file_error()`
- function `tools.cb()` change name to `tools.format_bool()`
- config.py clear some useless import class
- changing configfile to main.config *doing

### Test change

- `test_config_file.py`
- `test_for_speed.py`
- `test_logging_conf.py`
- `test_speed_of_sprite.py`


## 2021/06/26 V 0.4.3

### DEBUG

- some name_format bug

### Change

- doing: change render pip line ('m really doing)
- default FPS from 120 -> 60

### Add

- add performance_test folder
- add some performances test


## 2021/05/24 V 0.4.2

### DEBUG

- using python version 3.8.9 still report `best3.8+`(lang name)(actually is debugging)

### Change

- change back how configs.py/name_format work(replace str) fix some issue
- doing remake for config sys (lazy yes!)
- clear bin/pyglet (already exits in bin/lib)

### Need Do

- debug name_format


## 2021/04/17 V 0.4.1

PS:

- `Va.b.c`

- a : Big Version (Big rewrite times) (now at DEMO making)
- b : Middle Rewrite Times (Yes I've rewritten for 4 times)
- c : normal updates

### DEBUG

- solve pre-installed lib can't use
- solve pre-installed lib's bug
- some other bugs

### Change

- plan to change config file format to .config (plan to)
- reformat all files (including libs)


## 2021/04/09 V 0.2.3/4

### Add

- support many things(also forget)

### Change

- `tools.name_handler()` now use `str.format` to handler str
- `DR/sys_value` folder now move to `DR/configs/sys_value`

### DEBUG

- many `tools.name_handler()` use bug(cause crashes)
- `{date}` can be successful use in `tools.name_handler()` (if you define the format of date)
- log file's filename incorrect (should be `xxxx-xx-xx xx-xx-xx DR.log` but be `{date} DR.log`)


## 2021/03/27 V 0.2.2/1

### Add

- add local libs
    - `pyglet 1.5.15`
    - `json5  0.9.5`

PS: now I'm not sure witch lib will be import first

the local lib or the pip libs

So I'll add some other code to make sure that DR will first try to import pip libs

not the local libs (todo)

### DEBUG

- some bugs(I forget them)
