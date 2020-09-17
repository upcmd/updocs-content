---
title: "c0195_vvvvv"
date: 2020-09-18T01:27:59+99:00
draft: false
weight: 11954

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0195
                 Verbose -> vvvvv
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
                 Timeout -> 3600000
     MaxModuelCallLayers -> 256
               EntryTask -> task
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0195
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001c9240)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    {
    }
    
    (core.Cache) {
    }
    
    [runtime global] dvar expanded result:
    {
    }
    
    
    -------runtime global final merged with dvars-------
    
    {
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    {
      Name: "",
      Do: {
        {
          "name": "tmpFile",
          "cmd": {
            "content": "hello, world",
            "reg": "myfile"
          }
        },
        {
          "name": "print",
          "cmd": "filename: {{.myfile}}"
        },
        {
          "name": "readFile",
          "cmd": {
            "filename": "{{.myfile}}",
            "reg": "my_file_content"
          }
        },
        {
          "cmd": "file content: {{.my_file_content}}",
          "name": "print"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "",
      Reg: "",
      Flags: <nil>,
      If: "",
      Else: <nil>,
      Loop: <nil>,
      Until: "",
      RefDir: "",
      VarsFile: "",
      Timeout: 0,
      Finally: {
        {
          "do": "cat {{.myfile}}",
          "func": "shell"
        },
        {
          "func": "shell",
          "desc": "this shows you delete the tmp file in step finally\n",
          "do": "rm -f {{.myfile}}"
        },
        {
          "func": "shell",
          "do": "cat {{.myfile}}",
          "flags": {
            "ignoreError"
          }
        }
      },
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 0
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 0
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0
    })
    
    map[content:hello, world reg:myfile]
    ~SubStep1: [tmpFile:  ]
    tmp file handler: myfile
    filename: {{.myfile}}
    ~SubStep2: [print:  ]
    filename: /tmp/BpLnfgDsc2WD8F2qNfHK5a84807381306
    map[filename:{{.myfile}} reg:my_file_content]
    ~SubStep3: [readFile:  ]
    after reg the var - contextual global:
    
    (*core.Cache)({
      "my_file_content": "hello, world",
      "myfile": "/tmp/BpLnfgDsc2WD8F2qNfHK5a84807381306"
    })
    
    after reg the var - local:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "myfile": "/tmp/BpLnfgDsc2WD8F2qNfHK5a84807381306",
      "my_file_content": "hello, world"
    })
    
    file content: {{.my_file_content}}
    ~SubStep4: [print:  ]
    file content: hello, world
    Step Finally:
    (*utils.ExecResult)(<nil>)
    
    -Step1:
    {
      Name: "",
      Do: "cat {{.myfile}}",
      Dox: <nil>,
      Func: "shell",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "",
      Reg: "",
      Flags: <nil>,
      If: "",
      Else: <nil>,
      Loop: <nil>,
      Until: "",
      RefDir: "",
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "myfile": "/tmp/BpLnfgDsc2WD8F2qNfHK5a84807381306",
      "my_file_content": "hello, world",
      "up_runtime_task_layer_number": 0,
      "up_runtime_shell_exec_result": (*utils.ExecResult)(<nil>)
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "myfile": "/tmp/BpLnfgDsc2WD8F2qNfHK5a84807381306",
      "my_file_content": "hello, world",
      "up_runtime_task_layer_number": 0,
      "up_runtime_shell_exec_result": (*utils.ExecResult)(<nil>)
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "myfile": "/tmp/BpLnfgDsc2WD8F2qNfHK5a84807381306",
      "my_file_content": "hello, world",
      "up_runtime_task_layer_number": 0,
      "up_runtime_shell_exec_result": (*utils.ExecResult)(<nil>)
    })
    
    cmd( 1):
    cat {{.myfile}}
    
    cmd=>:
    cat /tmp/BpLnfgDsc2WD8F2qNfHK5a84807381306
    -
    hello, world
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=42) "cat /tmp/BpLnfgDsc2WD8F2qNfHK5a84807381306",
     Code: (int) 0,
     Output: (string) (len=12) "hello, world",
     ErrMsg: (string) ""
    }
    
    . ok
    -Step2: [: this shows you delete the tmp file in step finally
     ]
    {
      Name: "",
      Do: "rm -f {{.myfile}}",
      Dox: <nil>,
      Func: "shell",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "this shows you delete the tmp file in step finally\n",
      Reg: "",
      Flags: <nil>,
      If: "",
      Else: <nil>,
      Loop: <nil>,
      Until: "",
      RefDir: "",
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "cat /tmp/BpLnfgDsc2WD8F2qNfHK5a84807381306",
        Code: 0,
        Output: "hello, world",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0,
      "up_runtime_shell_exec_result": (*utils.ExecResult)(<nil>),
      "myfile": "/tmp/BpLnfgDsc2WD8F2qNfHK5a84807381306",
      "my_file_content": "hello, world"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "myfile": "/tmp/BpLnfgDsc2WD8F2qNfHK5a84807381306",
      "my_file_content": "hello, world",
      "last_result": (*utils.ExecResult)({
        Cmd: "cat /tmp/BpLnfgDsc2WD8F2qNfHK5a84807381306",
        Code: 0,
        Output: "hello, world",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0,
      "up_runtime_shell_exec_result": (*utils.ExecResult)(<nil>)
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "cat /tmp/BpLnfgDsc2WD8F2qNfHK5a84807381306",
        Code: 0,
        Output: "hello, world",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0,
      "up_runtime_shell_exec_result": (*utils.ExecResult)(<nil>),
      "myfile": "/tmp/BpLnfgDsc2WD8F2qNfHK5a84807381306",
      "my_file_content": "hello, world"
    })
    
    cmd( 1):
    rm -f {{.myfile}}
    
    cmd=>:
    rm -f /tmp/BpLnfgDsc2WD8F2qNfHK5a84807381306
    -
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=44) "rm -f /tmp/BpLnfgDsc2WD8F2qNfHK5a84807381306",
     Code: (int) 0,
     Output: (string) "",
     ErrMsg: (string) ""
    }
    
    . ok
    -Step3:
    {
      Name: "",
      Do: "cat {{.myfile}}",
      Dox: <nil>,
      Func: "shell",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "",
      Reg: "",
      Flags: {
        "ignoreError"
      },
      If: "",
      Else: <nil>,
      Loop: <nil>,
      Until: "",
      RefDir: "",
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "myfile": "/tmp/BpLnfgDsc2WD8F2qNfHK5a84807381306",
      "my_file_content": "hello, world",
      "last_result": (*utils.ExecResult)({
        Cmd: "rm -f /tmp/BpLnfgDsc2WD8F2qNfHK5a84807381306",
        Code: 0,
        Output: "",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0,
      "up_runtime_shell_exec_result": (*utils.ExecResult)(<nil>)
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "myfile": "/tmp/BpLnfgDsc2WD8F2qNfHK5a84807381306",
      "my_file_content": "hello, world",
      "last_result": (*utils.ExecResult)({
        Cmd: "rm -f /tmp/BpLnfgDsc2WD8F2qNfHK5a84807381306",
        Code: 0,
        Output: "",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0,
      "up_runtime_shell_exec_result": (*utils.ExecResult)(<nil>)
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_shell_exec_result": (*utils.ExecResult)(<nil>),
      "myfile": "/tmp/BpLnfgDsc2WD8F2qNfHK5a84807381306",
      "my_file_content": "hello, world",
      "last_result": (*utils.ExecResult)({
        Cmd: "rm -f /tmp/BpLnfgDsc2WD8F2qNfHK5a84807381306",
        Code: 0,
        Output: "",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0
    })
    
    cmd( 1):
    cat {{.myfile}}
    
    cmd=>:
    cat /tmp/BpLnfgDsc2WD8F2qNfHK5a84807381306
    -
    cat: can't open '/tmp/BpLnfgDsc2WD8F2qNfHK5a84807381306': No such file or directory
    
    -
     .. failed(suppressed if it is not the last step)
    (utils.ExecResult) {
     Cmd: (string) (len=42) "cat /tmp/BpLnfgDsc2WD8F2qNfHK5a84807381306",
     Code: (int) 1,
     Output: (string) "",
     ErrMsg: (string) (len=84) "cat: can't open '/tmp/BpLnfgDsc2WD8F2qNfHK5a84807381306': No such file or directory\n"
    }
    
     WARN: [ignoreError:] - [Error ignored!!!]
    task Finally:
    Step1: [: this shows you delete the tmp file in task finally
    this is deactivated
    just for reference
     ]
    {
      Name: "",
      Do: <nil>,
      Dox: "rm -f {{.myfile}}",
      Func: "shell",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "this shows you delete the tmp file in task finally\nthis is deactivated\njust for reference\n",
      Reg: "",
      Flags: <nil>,
      If: "",
      Else: <nil>,
      Loop: <nil>,
      Until: "",
      RefDir: "",
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
     WARN: [*] - [Step is deactivated!]
    Step2:
    {
      Name: "",
      Do: "cat {{.myfile}}",
      Dox: <nil>,
      Func: "shell",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "",
      Reg: "",
      Flags: {
        "ignoreError"
      },
      If: "",
      Else: <nil>,
      Loop: <nil>,
      Until: "",
      RefDir: "",
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "my_file_content": "hello, world",
      "last_result": (*utils.ExecResult)(<nil>),
      "myfile": "/tmp/BpLnfgDsc2WD8F2qNfHK5a84807381306"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "last_result": (*utils.ExecResult)(<nil>),
      "myfile": "/tmp/BpLnfgDsc2WD8F2qNfHK5a84807381306",
      "up_runtime_task_layer_number": 0,
      "my_file_content": "hello, world"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "my_file_content": "hello, world",
      "last_result": (*utils.ExecResult)(<nil>),
      "myfile": "/tmp/BpLnfgDsc2WD8F2qNfHK5a84807381306",
      "up_runtime_task_layer_number": 0
    })
    
    cmd( 1):
    cat {{.myfile}}
    
    cmd=>:
    cat /tmp/BpLnfgDsc2WD8F2qNfHK5a84807381306
    -
    cat: can't open '/tmp/BpLnfgDsc2WD8F2qNfHK5a84807381306': No such file or directory
    
    -
     .. failed(suppressed if it is not the last step)
    (utils.ExecResult) {
     Cmd: (string) (len=42) "cat /tmp/BpLnfgDsc2WD8F2qNfHK5a84807381306",
     Code: (int) 1,
     Output: (string) "",
     ErrMsg: (string) (len=84) "cat: can't open '/tmp/BpLnfgDsc2WD8F2qNfHK5a84807381306': No such file or directory\n"
    }
    
     WARN: [ignoreError:] - [Error ignored!!!]
    
```

##### Logs with different verbose level
* [c0195 log - verbose level v](../../logs/c0195_v)
* [c0195 log - verbose level vv](../../logs/c0195_vv)
* [c0195 log - verbose level vvv](../../logs/c0195_vvv)
* [c0195 log - verbose level vvvv](../../logs/c0195_vvvv)
* [c0195 log - verbose level vvvvv](../../logs/c0195_vvvvv)

##### References
* [Related Chapter](../../cmd-func/c0195)
