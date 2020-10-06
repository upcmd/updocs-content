---
title: "c0072_vvvvv"
date: 2020-10-06T23:46:03+1010:00
draft: false
weight: 10724

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
    loading [Task]:  ./tests/functests/c0072
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc00011c860)(<nil>)
    
    ---------group vars----------
    
    global: (*core.Cache)({
    })
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    (*core.Cache)({
      "read_dir": "/tmp",
      "read_file": "mystory2.txt",
      "name": "little prince",
      "school": "sydney grammar",
      "age": 12,
      "said": "Boa constrictors swallow their prey whole",
      "save_to": "/tmp/mystory2.txt"
    })
    
    (*core.Cache)(0xc00014c120)((len=7) {
     (string) (len=8) "read_dir": (string) (len=4) "/tmp",
     (string) (len=9) "read_file": (string) (len=12) "mystory2.txt",
     (string) (len=4) "name": (string) (len=13) "little prince",
     (string) (len=6) "school": (string) (len=14) "sydney grammar",
     (string) (len=3) "age": (int) 12,
     (string) (len=4) "said": (string) (len=41) "Boa constrictors swallow their prey whole",
     (string) (len=7) "save_to": (string) (len=17) "/tmp/mystory2.txt"
    })
    
    [runtime global] dvar expanded result:
    {
      "intest": "false"
    }
    
    
    -------runtime global final merged with dvars-------
    
    (*core.Cache)({
      "read_dir": "/tmp",
      "read_file": "mystory2.txt",
      "intest": "false",
      "name": "little prince",
      "school": "sydney grammar",
      "age": 12,
      "said": "Boa constrictors swallow their prey whole",
      "save_to": "/tmp/mystory2.txt"
    })
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    {
      Name: "",
      Do: {
        "echo \"?intest ->  {{.intest}}\"",
        "pwd"
      },
      Dox: <nil>,
      Func: "shell",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "",
      Reg: "register_task_root",
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
      "read_file": "mystory2.txt",
      "school": "sydney grammar",
      "save_to": "/tmp/mystory2.txt",
      "read_dir": "/tmp",
      "age": 12,
      "said": "Boa constrictors swallow their prey whole",
      "up_runtime_task_layer_number": 0,
      "intest": "false",
      "name": "little prince"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "school": "sydney grammar",
      "age": 12,
      "said": "Boa constrictors swallow their prey whole",
      "read_dir": "/tmp",
      "intest": "false",
      "up_runtime_task_layer_number": 0,
      "save_to": "/tmp/mystory2.txt",
      "name": "little prince",
      "read_file": "mystory2.txt"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "read_file": "mystory2.txt",
      "read_dir": "/tmp",
      "name": "little prince",
      "save_to": "/tmp/mystory2.txt",
      "age": 12,
      "said": "Boa constrictors swallow their prey whole",
      "intest": "false",
      "school": "sydney grammar"
    })
    
    cmd( 1):
    echo "?intest ->  {{.intest}}"
    
    cmd=>:
    echo "?intest ->  false"
    -
    ?intest ->  false
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=24) "echo \"?intest ->  false\"",
     Code: (int) 0,
     Output: (string) (len=17) "?intest ->  false",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    pwd
    
    cmd=>:
    pwd
    -
    /up_project/up
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=3) "pwd",
     Code: (int) 0,
     Output: (string) (len=14) "/up_project/up",
     ErrMsg: (string) ""
    }
    
    . ok
    -Step2:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "intest is: [{{.intest}}]"
        },
        {
          "name": "reg",
          "cmd": {
            "name": "correct_working_dir",
            "desc": "the value of .intest is string but not bool so you can not simply use if .intest for condition",
            "value": "{{if eq .intest \"true\" }}{{.register_task_root.Output}}{{else}}{{.register_task_root.Output}}{{end}}"
          }
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
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "age": 12,
      "said": "Boa constrictors swallow their prey whole",
      "school": "sydney grammar",
      "save_to": "/tmp/mystory2.txt",
      "read_file": "mystory2.txt",
      "up_runtime_task_layer_number": 0,
      "register_task_root": (*utils.ExecResult)({
        Cmd: "pwd",
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "last_result": (*utils.ExecResult)({
        Cmd: "pwd",
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "name": "little prince",
      "intest": "false",
      "read_dir": "/tmp"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "intest": "false",
      "up_runtime_task_layer_number": 0,
      "age": 12,
      "school": "sydney grammar",
      "read_dir": "/tmp",
      "register_task_root": (*utils.ExecResult)({
        Cmd: "pwd",
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "last_result": (*utils.ExecResult)({
        Cmd: "pwd",
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "name": "little prince",
      "read_file": "mystory2.txt",
      "said": "Boa constrictors swallow their prey whole",
      "save_to": "/tmp/mystory2.txt"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "age": 12,
      "said": "Boa constrictors swallow their prey whole",
      "save_to": "/tmp/mystory2.txt",
      "register_task_root": (*utils.ExecResult)({
        Cmd: "pwd",
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "name": "little prince",
      "intest": "false",
      "read_file": "mystory2.txt",
      "up_runtime_task_layer_number": 0,
      "school": "sydney grammar",
      "last_result": (*utils.ExecResult)({
        Cmd: "pwd",
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "read_dir": "/tmp"
    })
    
    intest is: [{{.intest}}]
    ~SubStep1: [print:  ]
    intest is: [false]
    map[desc:the value of .intest is string but not bool so you can not simply use if .intest for condition name:correct_working_dir value:{{if eq .intest "true" }}{{.register_task_root.Output}}{{else}}{{.register_task_root.Output}}{{end}}]
    ~SubStep2: [reg:  ]
    after reg the var - contextual global:
    
    (*core.Cache)({
      "school": "sydney grammar",
      "read_dir": "/tmp",
      "read_file": "mystory2.txt",
      "name": "little prince",
      "age": 12,
      "said": "Boa constrictors swallow their prey whole",
      "save_to": "/tmp/mystory2.txt",
      "intest": "false",
      "register_task_root": (*utils.ExecResult)({
        Cmd: "pwd",
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "last_result": (*utils.ExecResult)({
        Cmd: "pwd",
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "correct_working_dir": "/up_project/up"
    })
    
    after reg the var - local:
    
    (*core.Cache)({
      "name": "little prince",
      "intest": "false",
      "read_file": "mystory2.txt",
      "up_runtime_task_layer_number": 0,
      "correct_working_dir": "/up_project/up",
      "register_task_root": (*utils.ExecResult)({
        Cmd: "pwd",
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "last_result": (*utils.ExecResult)({
        Cmd: "pwd",
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "save_to": "/tmp/mystory2.txt",
      "school": "sydney grammar",
      "read_dir": "/tmp",
      "age": 12,
      "said": "Boa constrictors swallow their prey whole"
    })
    
    -Step3:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "root dir is: [{{.register_task_root.Output}}]"
        },
        {
          "name": "print",
          "cmd": "correct working dir is: [{{.correct_working_dir}}]"
        },
        {
          "name": "template",
          "desc": "render a template file to a file 1",
          "cmd": {
            "src": "{{.correct_working_dir}}/tests/functests/d0072.template",
            "dest": "/tmp/mystory.txt"
          }
        },
        {
          "name": "readFile",
          "desc": "read content of a file and register it to a var",
          "cmd": {
            "dir": "/tmp",
            "reg": "my_interesting_story",
            "filename": "mystory.txt"
          }
        },
        {
          "name": "print",
          "cmd": "{{.my_interesting_story}}"
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
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "correct_working_dir": "/up_project/up",
      "age": 12,
      "school": "sydney grammar",
      "register_task_root": (*utils.ExecResult)({
        Cmd: "pwd",
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "last_result": (*utils.ExecResult)({
        Cmd: "pwd",
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "read_file": "mystory2.txt",
      "name": "little prince",
      "said": "Boa constrictors swallow their prey whole",
      "read_dir": "/tmp",
      "intest": "false",
      "save_to": "/tmp/mystory2.txt"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "read_dir": "/tmp",
      "age": 12,
      "save_to": "/tmp/mystory2.txt",
      "intest": "false",
      "register_task_root": (*utils.ExecResult)({
        Cmd: "pwd",
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "last_result": (*utils.ExecResult)({
        Cmd: "pwd",
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "said": "Boa constrictors swallow their prey whole",
      "school": "sydney grammar",
      "correct_working_dir": "/up_project/up",
      "name": "little prince",
      "read_file": "mystory2.txt",
      "up_runtime_task_layer_number": 0
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "pwd",
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0,
      "name": "little prince",
      "age": 12,
      "save_to": "/tmp/mystory2.txt",
      "read_file": "mystory2.txt",
      "intest": "false",
      "register_task_root": (*utils.ExecResult)({
        Cmd: "pwd",
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "said": "Boa constrictors swallow their prey whole",
      "correct_working_dir": "/up_project/up",
      "read_dir": "/tmp",
      "school": "sydney grammar"
    })
    
    root dir is: [{{.register_task_root.Output}}]
    ~SubStep1: [print:  ]
    root dir is: [/up_project/up]
    correct working dir is: [{{.correct_working_dir}}]
    ~SubStep2: [print:  ]
    correct working dir is: [/up_project/up]
    map[dest:/tmp/mystory.txt src:{{.correct_working_dir}}/tests/functests/d0072.template]
    ~SubStep3: [template: render a template file to a file 1 ]
    map[dir:/tmp filename:mystory.txt reg:my_interesting_story]
    ~SubStep4: [readFile: read content of a file and register it to a var ]
    after reg the var - contextual global:
    
    (*core.Cache)({
      "register_task_root": (*utils.ExecResult)({
        Cmd: "pwd",
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "last_result": (*utils.ExecResult)({
        Cmd: "pwd",
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "correct_working_dir": "/up_project/up",
      "name": "little prince",
      "age": 12,
      "said": "Boa constrictors swallow their prey whole",
      "save_to": "/tmp/mystory2.txt",
      "intest": "false",
      "school": "sydney grammar",
      "read_dir": "/tmp",
      "read_file": "mystory2.txt",
      "my_interesting_story": "  My name is little prince, my school is sydney grammar\n  Once when I was 12 years old\n  In the book it said: Boa constrictors swallow their prey whole\n  I pondered deeply, then, over the adventures of the jungle.\n"
    })
    
    after reg the var - local:
    
    (*core.Cache)({
      "said": "Boa constrictors swallow their prey whole",
      "school": "sydney grammar",
      "read_dir": "/tmp",
      "my_interesting_story": "  My name is little prince, my school is sydney grammar\n  Once when I was 12 years old\n  In the book it said: Boa constrictors swallow their prey whole\n  I pondered deeply, then, over the adventures of the jungle.\n",
      "intest": "false",
      "register_task_root": (*utils.ExecResult)({
        Cmd: "pwd",
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "last_result": (*utils.ExecResult)({
        Cmd: "pwd",
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "save_to": "/tmp/mystory2.txt",
      "read_file": "mystory2.txt",
      "up_runtime_task_layer_number": 0,
      "correct_working_dir": "/up_project/up",
      "name": "little prince",
      "age": 12
    })
    
    {{.my_interesting_story}}
    ~SubStep5: [print:  ]
      My name is little prince, my school is sydney grammar
      Once when I was 12 years old
      In the book it said: Boa constrictors swallow their prey whole
      I pondered deeply, then, over the adventures of the jungle.
    
    -Step4:
    {
      Name: "",
      Do: {
        {
          "cmd": {
            "src": "{{.correct_working_dir}}/tests/functests/d0072.template",
            "dest": "{{.save_to}}"
          },
          "name": "template",
          "desc": "render a template file to a file 2"
        },
        {
          "desc": "read content of a file and register it to a var",
          "cmd": {
            "filename": "{{.read_file}}",
            "dir": "{{.read_dir}}",
            "reg": "my_interesting_story2"
          },
          "name": "readFile"
        },
        {
          "name": "print",
          "cmd": "{{.my_interesting_story2}}"
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
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "school": "sydney grammar",
      "my_interesting_story": "  My name is little prince, my school is sydney grammar\n  Once when I was 12 years old\n  In the book it said: Boa constrictors swallow their prey whole\n  I pondered deeply, then, over the adventures of the jungle.\n",
      "save_to": "/tmp/mystory2.txt",
      "last_result": (*utils.ExecResult)({
        Cmd: "pwd",
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0,
      "said": "Boa constrictors swallow their prey whole",
      "register_task_root": (*utils.ExecResult)({
        Cmd: "pwd",
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "read_file": "mystory2.txt",
      "age": 12,
      "intest": "false",
      "correct_working_dir": "/up_project/up",
      "name": "little prince",
      "read_dir": "/tmp"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "name": "little prince",
      "said": "Boa constrictors swallow their prey whole",
      "register_task_root": (*utils.ExecResult)({
        Cmd: "pwd",
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "my_interesting_story": "  My name is little prince, my school is sydney grammar\n  Once when I was 12 years old\n  In the book it said: Boa constrictors swallow their prey whole\n  I pondered deeply, then, over the adventures of the jungle.\n",
      "age": 12,
      "up_runtime_task_layer_number": 0,
      "last_result": (*utils.ExecResult)({
        Cmd: "pwd",
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "correct_working_dir": "/up_project/up",
      "school": "sydney grammar",
      "read_dir": "/tmp",
      "read_file": "mystory2.txt",
      "save_to": "/tmp/mystory2.txt",
      "intest": "false"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "read_file": "mystory2.txt",
      "correct_working_dir": "/up_project/up",
      "save_to": "/tmp/mystory2.txt",
      "intest": "false",
      "last_result": (*utils.ExecResult)({
        Cmd: "pwd",
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0,
      "register_task_root": (*utils.ExecResult)({
        Cmd: "pwd",
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "my_interesting_story": "  My name is little prince, my school is sydney grammar\n  Once when I was 12 years old\n  In the book it said: Boa constrictors swallow their prey whole\n  I pondered deeply, then, over the adventures of the jungle.\n",
      "age": 12,
      "name": "little prince",
      "said": "Boa constrictors swallow their prey whole",
      "school": "sydney grammar",
      "read_dir": "/tmp"
    })
    
    map[dest:{{.save_to}} src:{{.correct_working_dir}}/tests/functests/d0072.template]
    ~SubStep1: [template: render a template file to a file 2 ]
    map[dir:{{.read_dir}} filename:{{.read_file}} reg:my_interesting_story2]
    ~SubStep2: [readFile: read content of a file and register it to a var ]
    after reg the var - contextual global:
    
    (*core.Cache)({
      "school": "sydney grammar",
      "read_dir": "/tmp",
      "read_file": "mystory2.txt",
      "my_interesting_story": "  My name is little prince, my school is sydney grammar\n  Once when I was 12 years old\n  In the book it said: Boa constrictors swallow their prey whole\n  I pondered deeply, then, over the adventures of the jungle.\n",
      "my_interesting_story2": "  My name is little prince, my school is sydney grammar\n  Once when I was 12 years old\n  In the book it said: Boa constrictors swallow their prey whole\n  I pondered deeply, then, over the adventures of the jungle.\n",
      "name": "little prince",
      "age": 12,
      "said": "Boa constrictors swallow their prey whole",
      "save_to": "/tmp/mystory2.txt",
      "intest": "false",
      "register_task_root": (*utils.ExecResult)({
        Cmd: "pwd",
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "last_result": (*utils.ExecResult)({
        Cmd: "pwd",
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "correct_working_dir": "/up_project/up"
    })
    
    after reg the var - local:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "last_result": (*utils.ExecResult)({
        Cmd: "pwd",
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "name": "little prince",
      "said": "Boa constrictors swallow their prey whole",
      "register_task_root": (*utils.ExecResult)({
        Cmd: "pwd",
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "read_dir": "/tmp",
      "read_file": "mystory2.txt",
      "correct_working_dir": "/up_project/up",
      "save_to": "/tmp/mystory2.txt",
      "intest": "false",
      "age": 12,
      "my_interesting_story": "  My name is little prince, my school is sydney grammar\n  Once when I was 12 years old\n  In the book it said: Boa constrictors swallow their prey whole\n  I pondered deeply, then, over the adventures of the jungle.\n",
      "my_interesting_story2": "  My name is little prince, my school is sydney grammar\n  Once when I was 12 years old\n  In the book it said: Boa constrictors swallow their prey whole\n  I pondered deeply, then, over the adventures of the jungle.\n",
      "school": "sydney grammar"
    })
    
    {{.my_interesting_story2}}
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
