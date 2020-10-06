---
title: "c0072_vvvv"
date: 2020-10-06T23:46:03+1010:00
draft: false
weight: 10723

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0072
                 Verbose -> vvvv
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
                 Timeout -> 3600000
     MaxModuelCallLayers -> 256
               EntryTask -> task
      ModRepoUsernameRef -> 
      ModRepoPasswordRef -> 
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0072
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    ---------group vars----------
    
    global: (*core.Cache)({
    })
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    (*core.Cache)({
      "age": 12,
      "said": "Boa constrictors swallow their prey whole",
      "save_to": "/tmp/mystory2.txt",
      "read_dir": "/tmp",
      "read_file": "mystory2.txt",
      "name": "little prince",
      "school": "sydney grammar"
    })
    
    -------runtime global final merged with dvars-------
    
    (*core.Cache)({
      "save_to": "/tmp/mystory2.txt",
      "read_dir": "/tmp",
      "read_file": "mystory2.txt",
      "name": "little prince",
      "school": "sydney grammar",
      "intest": "false",
      "age": 12,
      "said": "Boa constrictors swallow their prey whole"
    })
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "said": "Boa constrictors swallow their prey whole",
      "name": "little prince",
      "save_to": "/tmp/mystory2.txt",
      "age": 12,
      "read_file": "mystory2.txt",
      "up_runtime_task_layer_number": 0,
      "read_dir": "/tmp",
      "school": "sydney grammar",
      "intest": "false"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "read_file": "mystory2.txt",
      "age": 12,
      "said": "Boa constrictors swallow their prey whole",
      "read_dir": "/tmp",
      "save_to": "/tmp/mystory2.txt",
      "up_runtime_task_layer_number": 0,
      "name": "little prince",
      "school": "sydney grammar",
      "intest": "false"
    })
    
    cmd( 1):
    echo "?intest ->  {{.intest}}"
    
    cmd=>:
    echo "?intest ->  false"
    -
    ?intest ->  false
    
    -
     .. ok
    cmd( 2):
    pwd
    
    cmd=>:
    pwd
    -
    /up_project/up
    
    -
     .. ok
    . ok
    -Step2:
    current exec runtime vars:
    (*core.Cache)({
      "register_task_root": (*utils.ExecResult)({
        Cmd: "pwd",
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "said": "Boa constrictors swallow their prey whole",
      "read_dir": "/tmp",
      "read_file": "mystory2.txt",
      "up_runtime_task_layer_number": 0,
      "name": "little prince",
      "school": "sydney grammar",
      "save_to": "/tmp/mystory2.txt",
      "intest": "false",
      "age": 12,
      "last_result": (*utils.ExecResult)({
        Cmd: "pwd",
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      })
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "read_file": "mystory2.txt",
      "save_to": "/tmp/mystory2.txt",
      "intest": "false",
      "age": 12,
      "last_result": (*utils.ExecResult)({
        Cmd: "pwd",
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "name": "little prince",
      "up_runtime_task_layer_number": 0,
      "read_dir": "/tmp",
      "school": "sydney grammar",
      "register_task_root": (*utils.ExecResult)({
        Cmd: "pwd",
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "said": "Boa constrictors swallow their prey whole"
    })
    
    ~SubStep1: [print:  ]
    intest is: [false]
    ~SubStep2: [reg:  ]
    -Step3:
    current exec runtime vars:
    (*core.Cache)({
      "register_task_root": (*utils.ExecResult)({
        Cmd: "pwd",
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0,
      "age": 12,
      "said": "Boa constrictors swallow their prey whole",
      "school": "sydney grammar",
      "name": "little prince",
      "last_result": (*utils.ExecResult)({
        Cmd: "pwd",
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "correct_working_dir": "/up_project/up",
      "save_to": "/tmp/mystory2.txt",
      "read_file": "mystory2.txt",
      "read_dir": "/tmp",
      "intest": "false"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "correct_working_dir": "/up_project/up",
      "name": "little prince",
      "last_result": (*utils.ExecResult)({
        Cmd: "pwd",
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "read_dir": "/tmp",
      "up_runtime_task_layer_number": 0,
      "intest": "false",
      "save_to": "/tmp/mystory2.txt",
      "read_file": "mystory2.txt",
      "school": "sydney grammar",
      "register_task_root": (*utils.ExecResult)({
        Cmd: "pwd",
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "age": 12,
      "said": "Boa constrictors swallow their prey whole"
    })
    
    ~SubStep1: [print:  ]
    root dir is: [/up_project/up]
    ~SubStep2: [print:  ]
    correct working dir is: [/up_project/up]
    ~SubStep3: [template: render a template file to a file 1 ]
    ~SubStep4: [readFile: read content of a file and register it to a var ]
    ~SubStep5: [print:  ]
      My name is little prince, my school is sydney grammar
      Once when I was 12 years old
      In the book it said: Boa constrictors swallow their prey whole
      I pondered deeply, then, over the adventures of the jungle.
    
    -Step4:
    current exec runtime vars:
    (*core.Cache)({
      "said": "Boa constrictors swallow their prey whole",
      "read_file": "mystory2.txt",
      "age": 12,
      "up_runtime_task_layer_number": 0,
      "last_result": (*utils.ExecResult)({
        Cmd: "pwd",
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "my_interesting_story": "  My name is little prince, my school is sydney grammar\n  Once when I was 12 years old\n  In the book it said: Boa constrictors swallow their prey whole\n  I pondered deeply, then, over the adventures of the jungle.\n",
      "read_dir": "/tmp",
      "school": "sydney grammar",
      "correct_working_dir": "/up_project/up",
      "name": "little prince",
      "intest": "false",
      "register_task_root": (*utils.ExecResult)({
        Cmd: "pwd",
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "save_to": "/tmp/mystory2.txt"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "read_file": "mystory2.txt",
      "correct_working_dir": "/up_project/up",
      "age": 12,
      "intest": "false",
      "register_task_root": (*utils.ExecResult)({
        Cmd: "pwd",
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "read_dir": "/tmp",
      "said": "Boa constrictors swallow their prey whole",
      "name": "little prince",
      "up_runtime_task_layer_number": 0,
      "last_result": (*utils.ExecResult)({
        Cmd: "pwd",
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "my_interesting_story": "  My name is little prince, my school is sydney grammar\n  Once when I was 12 years old\n  In the book it said: Boa constrictors swallow their prey whole\n  I pondered deeply, then, over the adventures of the jungle.\n",
      "save_to": "/tmp/mystory2.txt",
      "school": "sydney grammar"
    })
    
    ~SubStep1: [template: render a template file to a file 2 ]
    ~SubStep2: [readFile: read content of a file and register it to a var ]
    ~SubStep3: [print:  ]
      My name is little prince, my school is sydney grammar
      Once when I was 12 years old
      In the book it said: Boa constrictors swallow their prey whole
      I pondered deeply, then, over the adventures of the jungle.
    
    
```

##### Logs with different verbose level
* [c0072 log - verbose level v](../../logs/c0072_v)
* [c0072 log - verbose level vv](../../logs/c0072_vv)
* [c0072 log - verbose level vvv](../../logs/c0072_vvv)
* [c0072 log - verbose level vvvv](../../logs/c0072_vvvv)
* [c0072 log - verbose level vvvvv](../../logs/c0072_vvvvv)

##### References
* [Related Chapter](../../templating/c0072)
