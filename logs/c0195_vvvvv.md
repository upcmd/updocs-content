---
title: "c0195_vvvvv"
date: 2020-10-06T23:46:28+1010:00
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
      ModRepoUsernameRef -> 
      ModRepoPasswordRef -> 
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
    (*impl.Scopes)(0xc000175260)(<nil>)
    
    ---------group vars----------
    
    global: (*core.Cache)({
    })
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    (*core.Cache)({
    })
    
    (*core.Cache)(0xc0000b68e8)({
    })
    
    [runtime global] dvar expanded result:
    {
    }
    
    
    -------runtime global final merged with dvars-------
    
    (*core.Cache)({
    })
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    {
      Name: "",
      Do: {
        {
          "cmd": {
            "reg": "myfile",
            "content": "hello, world"
          },
          "name": "tmpFile"
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
          "name": "print",
          "cmd": "file content: {{.my_file_content}}"
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
          "func": "shell",
          "do": "cat {{.myfile}}"
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
    filename: /tmp/BpLnfgDsc2WD8F2qNfHK5a84592347706
    map[filename:{{.myfile}} reg:my_file_content]
    ~SubStep3: [readFile:  ]
    after reg the var - contextual global:
    
    (*core.Cache)({
      "myfile": "/tmp/BpLnfgDsc2WD8F2qNfHK5a84592347706",
      "my_file_content": "hello, world"
    })
    
    after reg the var - local:
    
    (*core.Cache)({
      "my_file_content": "hello, world",
      "up_runtime_task_layer_number": 0,
      "myfile": "/tmp/BpLnfgDsc2WD8F2qNfHK5a84592347706"
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
      "my_file_content": "hello, world",
      "up_runtime_task_layer_number": 0,
      "up_runtime_shell_exec_result": (*utils.ExecResult)(<nil>),
      "myfile": "/tmp/BpLnfgDsc2WD8F2qNfHK5a84592347706"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 0,
      "up_runtime_shell_exec_result": (*utils.ExecResult)(<nil>),
      "myfile": "/tmp/BpLnfgDsc2WD8F2qNfHK5a84592347706",
      "my_file_content": "hello, world"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "myfile": "/tmp/BpLnfgDsc2WD8F2qNfHK5a84592347706",
      "my_file_content": "hello, world",
      "up_runtime_task_layer_number": 0,
      "up_runtime_shell_exec_result": (*utils.ExecResult)(<nil>)
    })
    
    cmd( 1):
    cat {{.myfile}}
    
    cmd=>:
    cat /tmp/BpLnfgDsc2WD8F2qNfHK5a84592347706
    -
    hello, world
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=42) "cat /tmp/BpLnfgDsc2WD8F2qNfHK5a84592347706",
     Code: (int) 0,
     Output: (string) (len=12) "hello, world",
     ErrMsg: (string) ""
    }
    
    . ok
    -Step2: [
    this shows you delete the tmp file in step finally
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
        Cmd: "cat /tmp/BpLnfgDsc2WD8F2qNfHK5a84592347706",
        Code: 0,
        Output: "hello, world",
        ErrMsg: ""
      }),
      "myfile": "/tmp/BpLnfgDsc2WD8F2qNfHK5a84592347706",
      "my_file_content": "hello, world",
      "up_runtime_task_layer_number": 0,
      "up_runtime_shell_exec_result": (*utils.ExecResult)(<nil>)
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "myfile": "/tmp/BpLnfgDsc2WD8F2qNfHK5a84592347706",
      "my_file_content": "hello, world",
      "up_runtime_task_layer_number": 0,
      "up_runtime_shell_exec_result": (*utils.ExecResult)(<nil>),
      "last_result": (*utils.ExecResult)({
        Cmd: "cat /tmp/BpLnfgDsc2WD8F2qNfHK5a84592347706",
        Code: 0,
        Output: "hello, world",
        ErrMsg: ""
      })
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "up_runtime_shell_exec_result": (*utils.ExecResult)(<nil>),
      "last_result": (*utils.ExecResult)({
        Cmd: "cat /tmp/BpLnfgDsc2WD8F2qNfHK5a84592347706",
        Code: 0,
        Output: "hello, world",
        ErrMsg: ""
      }),
      "myfile": "/tmp/BpLnfgDsc2WD8F2qNfHK5a84592347706",
      "my_file_content": "hello, world"
    })
    
    cmd( 1):
    rm -f {{.myfile}}
    
    cmd=>:
    rm -f /tmp/BpLnfgDsc2WD8F2qNfHK5a84592347706
    -
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=44) "rm -f /tmp/BpLnfgDsc2WD8F2qNfHK5a84592347706",
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
      "up_runtime_shell_exec_result": (*utils.ExecResult)(<nil>),
      "last_result": (*utils.ExecResult)({
        Cmd: "rm -f /tmp/BpLnfgDsc2WD8F2qNfHK5a84592347706",
        Code: 0,
        Output: "",
        ErrMsg: ""
      }),
      "myfile": "/tmp/BpLnfgDsc2WD8F2qNfHK5a84592347706",
      "my_file_content": "hello, world",
      "up_runtime_task_layer_number": 0
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "my_file_content": "hello, world",
      "up_runtime_task_layer_number": 0,
      "up_runtime_shell_exec_result": (*utils.ExecResult)(<nil>),
      "last_result": (*utils.ExecResult)({
        Cmd: "rm -f /tmp/BpLnfgDsc2WD8F2qNfHK5a84592347706",
        Code: 0,
        Output: "",
        ErrMsg: ""
      }),
      "myfile": "/tmp/BpLnfgDsc2WD8F2qNfHK5a84592347706"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "up_runtime_shell_exec_result": (*utils.ExecResult)(<nil>),
      "last_result": (*utils.ExecResult)({
        Cmd: "rm -f /tmp/BpLnfgDsc2WD8F2qNfHK5a84592347706",
        Code: 0,
        Output: "",
        ErrMsg: ""
      }),
      "myfile": "/tmp/BpLnfgDsc2WD8F2qNfHK5a84592347706",
      "my_file_content": "hello, world"
    })
    
    cmd( 1):
    cat {{.myfile}}
    
    cmd=>:
    cat /tmp/BpLnfgDsc2WD8F2qNfHK5a84592347706
    -
    cat: can't open '/tmp/BpLnfgDsc2WD8F2qNfHK5a84592347706': No such file or directory
    
    -
     .. failed(suppressed if it is not the last step)
    (utils.ExecResult) {
     Cmd: (string) (len=42) "cat /tmp/BpLnfgDsc2WD8F2qNfHK5a84592347706",
     Code: (int) 1,
     Output: (string) "",
     ErrMsg: (string) (len=84) "cat: can't open '/tmp/BpLnfgDsc2WD8F2qNfHK5a84592347706': No such file or directory\n"
    }
    
     WARN: [ignoreError:] - [Error ignored!!!]
    task Finally:
    Step1: [
    this shows you delete the tmp file in task finally
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
      "myfile": "/tmp/BpLnfgDsc2WD8F2qNfHK5a84592347706",
      "my_file_content": "hello, world",
      "last_result": (*utils.ExecResult)(<nil>),
      "up_runtime_task_layer_number": 0
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "my_file_content": "hello, world",
      "last_result": (*utils.ExecResult)(<nil>),
      "up_runtime_task_layer_number": 0,
      "myfile": "/tmp/BpLnfgDsc2WD8F2qNfHK5a84592347706"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "my_file_content": "hello, world",
      "last_result": (*utils.ExecResult)(<nil>),
      "up_runtime_task_layer_number": 0,
      "myfile": "/tmp/BpLnfgDsc2WD8F2qNfHK5a84592347706"
    })
    
    cmd( 1):
    cat {{.myfile}}
    
    cmd=>:
    cat /tmp/BpLnfgDsc2WD8F2qNfHK5a84592347706
    -
    cat: can't open '/tmp/BpLnfgDsc2WD8F2qNfHK5a84592347706': No such file or directory
    
    -
     .. failed(suppressed if it is not the last step)
    (utils.ExecResult) {
     Cmd: (string) (len=42) "cat /tmp/BpLnfgDsc2WD8F2qNfHK5a84592347706",
     Code: (int) 1,
     Output: (string) "",
     ErrMsg: (string) (len=84) "cat: can't open '/tmp/BpLnfgDsc2WD8F2qNfHK5a84592347706': No such file or directory\n"
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
