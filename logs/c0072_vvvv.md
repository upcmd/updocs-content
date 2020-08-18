---
title: "c0072_vvvv"
date: 2020-08-18T15:16:01+88:00
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
    
    global: {
    }
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    {
      "name": "little prince",
      "school": "sydney grammar",
      "age": 12,
      "said": "Boa constrictors swallow their prey whole",
      "save_to": "/tmp/mystory2.txt",
      "read_dir": "/tmp",
      "read_file": "mystory2.txt"
    }
    
    -------runtime global final merged with dvars-------
    
    {
      "read_dir": "/tmp",
      "intest": "false",
      "read_file": "mystory2.txt",
      "name": "little prince",
      "school": "sydney grammar",
      "age": 12,
      "said": "Boa constrictors swallow their prey whole",
      "save_to": "/tmp/mystory2.txt"
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "save_to": "/tmp/mystory2.txt",
      "read_dir": "/tmp",
      "intest": "false",
      "read_file": "mystory2.txt",
      "name": "little prince",
      "school": "sydney grammar",
      "age": 12,
      "said": "Boa constrictors swallow their prey whole"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "intest": "false",
      "read_file": "mystory2.txt",
      "name": "little prince",
      "school": "sydney grammar",
      "age": 12,
      "said": "Boa constrictors swallow their prey whole",
      "save_to": "/tmp/mystory2.txt",
      "read_dir": "/tmp"
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
      "read_file": "mystory2.txt",
      "school": "sydney grammar",
      "save_to": "/tmp/mystory2.txt",
      "intest": "false",
      "name": "little prince",
      "said": "Boa constrictors swallow their prey whole",
      "age": 12,
      "read_dir": "/tmp",
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
      "school": "sydney grammar",
      "save_to": "/tmp/mystory2.txt",
      "intest": "false",
      "name": "little prince",
      "register_task_root": (*utils.ExecResult)({
        Cmd: "pwd",
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "said": "Boa constrictors swallow their prey whole",
      "age": 12,
      "read_dir": "/tmp",
      "last_result": (*utils.ExecResult)({
        Cmd: "pwd",
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      })
    })
    
    ~SubStep1: [print:  ]
    intest is: [false]
    ~SubStep2: [reg:  ]
    -Step3:
    current exec runtime vars:
    (*core.Cache)({
      "correct_working_dir": "/up_project/up",
      "name": "little prince",
      "read_dir": "/tmp",
      "last_result": (*utils.ExecResult)({
        Cmd: "pwd",
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "intest": "false",
      "age": 12,
      "register_task_root": (*utils.ExecResult)({
        Cmd: "pwd",
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "read_file": "mystory2.txt",
      "school": "sydney grammar",
      "said": "Boa constrictors swallow their prey whole",
      "save_to": "/tmp/mystory2.txt"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "school": "sydney grammar",
      "said": "Boa constrictors swallow their prey whole",
      "save_to": "/tmp/mystory2.txt",
      "intest": "false",
      "age": 12,
      "register_task_root": (*utils.ExecResult)({
        Cmd: "pwd",
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "read_file": "mystory2.txt",
      "name": "little prince",
      "read_dir": "/tmp",
      "last_result": (*utils.ExecResult)({
        Cmd: "pwd",
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "correct_working_dir": "/up_project/up"
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
      "intest": "false",
      "correct_working_dir": "/up_project/up",
      "name": "little prince",
      "age": 12,
      "register_task_root": (*utils.ExecResult)({
        Cmd: "pwd",
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "my_interesting_story": "  My name is little prince, my school is sydney grammar\n  Once when I was 12 years old\n  In the book it said: Boa constrictors swallow their prey whole\n  I pondered deeply, then, over the adventures of the jungle.\n",
      "read_file": "mystory2.txt",
      "school": "sydney grammar",
      "read_dir": "/tmp",
      "last_result": (*utils.ExecResult)({
        Cmd: "pwd",
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "said": "Boa constrictors swallow their prey whole",
      "save_to": "/tmp/mystory2.txt"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "intest": "false",
      "correct_working_dir": "/up_project/up",
      "name": "little prince",
      "age": 12,
      "register_task_root": (*utils.ExecResult)({
        Cmd: "pwd",
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "my_interesting_story": "  My name is little prince, my school is sydney grammar\n  Once when I was 12 years old\n  In the book it said: Boa constrictors swallow their prey whole\n  I pondered deeply, then, over the adventures of the jungle.\n",
      "read_file": "mystory2.txt",
      "school": "sydney grammar",
      "read_dir": "/tmp",
      "last_result": (*utils.ExecResult)({
        Cmd: "pwd",
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "said": "Boa constrictors swallow their prey whole",
      "save_to": "/tmp/mystory2.txt"
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
