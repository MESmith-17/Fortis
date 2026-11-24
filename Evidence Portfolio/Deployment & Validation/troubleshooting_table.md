

|ID|Error|Explanation|Fix|Commit|
|-|-|-|-|-|
|Error 01|NativeCommandError at setup.psl:76|pip keeps uninstalling llama\_cpp\_python|Edit $ErrorActionPreference to display the error message but continue running commands anyway, rather than halting executions.|https://github.com/MESmith-17/Fortis/commit/528a4ecaa58c357743a54bfe06f8e82cac8345e8|
|Error 02|The setup accepted Python 3.15|The regex Python 3\\. (1\[0-4]\|\[0-9] has no end anchor, so kept matching to the '1' in '3.15'.|Made the version check prefer '3.13' and reject 3.14+.<br />Added 'chromadb >=1.0'|https://github.com/MESmith-17/Fortis/commit/5e19cf41ab2f989d16cb69164ae51b1e4aace976|
|Error 03|AI outputted a "network error" and terminal showed an 'OSError' in 'llama\_backend\_init'|The llama-cpp-python 0.3.38 crashed at the backend init with illegal instruction.|Downgrade the llama-cpp-python==0.3.19, which passes to llama\_backend\_init()|N/A|



