# LineCount README

The LineCount extension for Visual Studio Code counts and displays the lines of code, the lines of comment, the lines of blank. 


[![Version](https://vsmarketplacebadge.apphb.com/version/yycalm.linecount.svg)](https://marketplace.visualstudio.com/items?itemName=yycalm.linecount)

[![Installs](https://vsmarketplacebadge.apphb.com/installs/yycalm.linecount.svg)](https://marketplace.visualstudio.com/items?itemName=yycalm.linecount)

[![Ratings](https://vsmarketplacebadge.apphb.com/rating/yycalm.linecount.svg)](https://marketplace.visualstudio.com/items?itemName=yycalm.linecount)

---

## Features

* Count current file. 

* Count workspace files, you can custom the includes/excludes file pattern.

* Support languages: c,cpp,java,js,ts,cs,sql,pas,perl,python,ruby,vb('),html(<!--,-->),bat(::),sh(#),ini(;),fortran(!),m(%).

* You can customize the comment symbol.

* Line number information can be output to JSON, TXT file.

## Installs

* ext install linecount

* Through Code

    Download source code and install dependencies:

```
git clone https://github.com/yycalm/linecount.git
cd linecount
npm install
code .
```

## Extension Settings
 
* `LineCount.showStatusBarItem`:(boolean|default `true`) Show/hide the status bar item for LineCount commands.
* `LineCount.includes`:(string array|default `"**/*"`) Search files pattern.
* `LineCount.excludes`:(string array|default `"**/.vscode/**,**/node_modules/**"`) files and folders that you want exclude them.
* `LineCount.output.txt`:(boolean | default `true`) Whether output to TXT file.
* `LineCount.output.json`:(boolean | default `true`) Whether output to JSON file.
* `LineCount.output.outdir`:(string | default `out`) output file path.
* `LineCount.output.comment.ext`:(string array| required) file extension. if it`s "*", the rule for other files. default c style.
* `LineCount.output.comment.separator.linecomment`:(string |default none) Single line comment symbol.
* `LineCount.output.comment.separator.linetol`:(boolean |default `false`) Whether the line comment must be started on the line.
* `LineCount.output.comment.separator.blockstart`:(string |default none) Block start comment symbol.
* `LineCount.output.comment.separator.blockend`:(string |default none) Block end comment symbol.
* `LineCount.output.comment.separator.blocktol`:(boolean |default `false`) Whether the block comment must be started on the line.
* `LineCount.output.comment.separator.string.doublequotes`:(boolean |default `true`) String using double quotes.
* `LineCount.output.comment.separator.string.singlequotes`:(boolean |default `true`) String using single quotes.

  LineCount configuration examples：

```
    "LineCount.includes": [     
                        "**/*" 
                        ]         
    
    "LineCount.excludes": [ 
                         "**/.vscode/**",
                        "**/node_modules/**"
                        ]

    "LineCount.output": {
                         "txt": true,       
                        "json": true,       
                        "outdir":"out"      
                        }

    "LineCount.comment":[
                        {
                            "ext": ["c","cpp","java"], 
                            "separator": {             
                                "linecomment": "//",   
                                "linetol":false,       
                                "blockstart": "/*",    
                                "blockend": "*/",      
                                "blocktol": false,     
                                "string":{
                                    "doublequotes": true,
                                    "singlequotes": false
                                }                                
                            }
                        }
                     ]
        

```



## Usage

There are two commands available. 
You can access them from the command palette (Ctrl+Shift+P on Windows/Linux), or click StatusBarItem 'LineCount'.

1. LineCount: Count current file:

![Count current file](https://github.com/yycalm/linecount/blob/master/images/countcurrentfile.gif?raw=true)


2. LineCount: Count Workspace files:

![Count workspace files](https://github.com/yycalm/linecount/blob/master/images/countworkspace.gif?raw=true)


## Support

[Repository](https://github.com/yycalm/linecount)


# License

MIT

-----------------------------------------------------------------------------------------------------------

**Enjoy!**