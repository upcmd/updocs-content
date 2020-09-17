---
title: "c0195_vvvv"
date: 2020-09-18T01:27:59+99:00
draft: false
weight: 11953

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
                 Verbose -> vvvv
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
                 Timeout -> 3600000
     MaxModuelCallLayers -> 256
               EntryTask -> task
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0195
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    {
    }
    
    -------runtime global final merged with dvars-------
    
    {
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0
    })
    
    ~SubStep1: [tmpFile:  ]
    tmp file handler: myfile
    ~SubStep2: [print:  ]
    filename: /tmp/BpLnfgDsc2WD8F2qNfHK5a84656262108
    ~SubStep3: [readFile:  ]
    ~SubStep4: [print:  ]
    file content: hello, world
    Step Finally:
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "myfile": "/tmp/BpLnfgDsc2WD8F2qNfHK5a84656262108",
      "my_file_content": "hello, world",
      "up_runtime_task_layer_number": 0,
      "up_runtime_shell_exec_result": (*utils.ExecResult)(<nil>)
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "myfile": "/tmp/BpLnfgDsc2WD8F2qNfHK5a84656262108",
      "my_file_content": "hello, world",
      "up_runtime_task_layer_number": 0,
      "up_runtime_shell_exec_result": (*utils.ExecResult)(<nil>)
    })
    
    cmd( 1):
    cat {{.myfile}}
    
    cmd=>:
    cat /tmp/BpLnfgDsc2WD8F2qNfHK5a84656262108
    -
    hello, world
    -
     .. ok
    . ok
    -Step2: [: this shows you delete the tmp file in step finally
     ]
    current exec runtime vars:
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "cat /tmp/BpLnfgDsc2WD8F2qNfHK5a84656262108",
        Code: 0,
        Output: "hello, world",
        ErrMsg: ""
      }),
      "myfile": "/tmp/BpLnfgDsc2WD8F2qNfHK5a84656262108",
      "up_runtime_task_layer_number": 0,
      "up_runtime_shell_exec_result": (*utils.ExecResult)(<nil>),
      "my_file_content": "hello, world"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "myfile": "/tmp/BpLnfgDsc2WD8F2qNfHK5a84656262108",
      "up_runtime_task_layer_number": 0,
      "up_runtime_shell_exec_result": (*utils.ExecResult)(<nil>),
      "my_file_content": "hello, world",
      "last_result": (*utils.ExecResult)({
        Cmd: "cat /tmp/BpLnfgDsc2WD8F2qNfHK5a84656262108",
        Code: 0,
        Output: "hello, world",
        ErrMsg: ""
      })
    })
    
    cmd( 1):
    rm -f {{.myfile}}
    
    cmd=>:
    rm -f /tmp/BpLnfgDsc2WD8F2qNfHK5a84656262108
    -
    
    -
     .. ok
    . ok
    -Step3:
    current exec runtime vars:
    (*core.Cache)({
      "myfile": "/tmp/BpLnfgDsc2WD8F2qNfHK5a84656262108",
      "my_file_content": "hello, world",
      "last_result": (*utils.ExecResult)({
        Cmd: "rm -f /tmp/BpLnfgDsc2WD8F2qNfHK5a84656262108",
        Code: 0,
        Output: "",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0,
      "up_runtime_shell_exec_result": (*utils.ExecResult)(<nil>)
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "myfile": "/tmp/BpLnfgDsc2WD8F2qNfHK5a84656262108",
      "my_file_content": "hello, world",
      "last_result": (*utils.ExecResult)({
        Cmd: "rm -f /tmp/BpLnfgDsc2WD8F2qNfHK5a84656262108",
        Code: 0,
        Output: "",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0,
      "up_runtime_shell_exec_result": (*utils.ExecResult)(<nil>)
    })
    
    cmd( 1):
    cat {{.myfile}}
    
    cmd=>:
    cat /tmp/BpLnfgDsc2WD8F2qNfHK5a84656262108
    -
    cat: can't open '/tmp/BpLnfgDsc2WD8F2qNfHK5a84656262108': No such file or directory
    
    -
     .. failed(suppressed if it is not the last step)
     WARN: [ignoreError:] - [Error ignored!!!]
    task Finally:
    Step1: [: this shows you delete the tmp file in task finally
    this is deactivated
    just for reference
     ]
     WARN: [*] - [Step is deactivated!]
    Step2:
    current exec runtime vars:
    (*core.Cache)({
      "last_result": (*utils.ExecResult)(<nil>),
      "up_runtime_task_layer_number": 0,
      "myfile": "/tmp/BpLnfgDsc2WD8F2qNfHK5a84656262108",
      "my_file_content": "hello, world"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "myfile": "/tmp/BpLnfgDsc2WD8F2qNfHK5a84656262108",
      "my_file_content": "hello, world",
      "last_result": (*utils.ExecResult)(<nil>),
      "up_runtime_task_layer_number": 0
    })
    
    cmd( 1):
    cat {{.myfile}}
    
    cmd=>:
    cat /tmp/BpLnfgDsc2WD8F2qNfHK5a84656262108
    -
    cat: can't open '/tmp/BpLnfgDsc2WD8F2qNfHK5a84656262108': No such file or directory
    
    -
     .. failed(suppressed if it is not the last step)
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
