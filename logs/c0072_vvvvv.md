---
title: "c0072_vvvvv"
date: 2020-09-18T01:27:32+99:00
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
    (*impl.Scopes)(0xc0001bf460)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    {
      "school": "sydney grammar",
      "age": 12,
      "said": "Boa constrictors swallow their prey whole",
      "save_to": "/tmp/mystory2.txt",
      "read_dir": "/tmp",
      "read_file": "mystory2.txt",
      "name": "little prince"
    }
    
    (core.Cache) (len=7) {
     (string) (len=6) "school": (string) (len=14) "sydney grammar",
     (string) (len=3) "age": (int) 12,
     (string) (len=4) "said": (string) (len=41) "Boa constrictors swallow their prey whole",
     (string) (len=7) "save_to": (string) (len=17) "/tmp/mystory2.txt",
     (string) (len=8) "read_dir": (string) (len=4) "/tmp",
     (string) (len=9) "read_file": (string) (len=12) "mystory2.txt",
     (string) (len=4) "name": (string) (len=13) "little prince"
    }
    
    [runtime global] dvar expanded result:
    {
      "intest": "false"
    }
    
    
    -------runtime global final merged with dvars-------
    
    {
      "school": "sydney grammar",
      "intest": "false",
      "age": 12,
      "said": "Boa constrictors swallow their prey whole",
      "save_to": "/tmp/mystory2.txt",
      "read_dir": "/tmp",
      "read_file": "mystory2.txt",
      "name": "little prince"
    }
    
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
      "name": "little prince",
      "intest": "false",
      "up_runtime_task_layer_number": 0,
      "age": 12,
      "said": "Boa constrictors swallow their prey whole",
      "save_to": "/tmp/mystory2.txt",
      "read_dir": "/tmp"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "school": "sydney grammar",
      "save_to": "/tmp/mystory2.txt",
      "name": "little prince",
      "up_runtime_task_layer_number": 0,
      "age": 12,
      "read_file": "mystory2.txt",
      "read_dir": "/tmp",
      "intest": "false",
      "said": "Boa constrictors swallow their prey whole"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "age": 12,
      "said": "Boa constrictors swallow their prey whole",
      "save_to": "/tmp/mystory2.txt",
      "read_dir": "/tmp",
      "name": "little prince",
      "intest": "false",
      "up_runtime_task_layer_number": 0,
      "read_file": "mystory2.txt",
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
      "said": "Boa constrictors swallow their prey whole",
      "read_file": "mystory2.txt",
      "name": "little prince",
      "school": "sydney grammar",
      "age": 12,
      "read_dir": "/tmp",
      "up_runtime_task_layer_number": 0,
      "last_result": (*utils.ExecResult)({
        Cmd: "pwd",
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "save_to": "/tmp/mystory2.txt",
      "intest": "false",
      "register_task_root": (*utils.ExecResult)({
        Cmd: "pwd",
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      })
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "read_dir": "/tmp",
      "up_runtime_task_layer_number": 0,
      "save_to": "/tmp/mystory2.txt",
      "intest": "false",
      "register_task_root": (*utils.ExecResult)({
        Cmd: "pwd",
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "read_file": "mystory2.txt",
      "school": "sydney grammar",
      "age": 12,
      "said": "Boa constrictors swallow their prey whole",
      "name": "little prince",
      "last_result": (*utils.ExecResult)({
        Cmd: "pwd",
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      })
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "pwd",
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "save_to": "/tmp/mystory2.txt",
      "intest": "false",
      "register_task_root": (*utils.ExecResult)({
        Cmd: "pwd",
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "said": "Boa constrictors swallow their prey whole",
      "read_file": "mystory2.txt",
      "name": "little prince",
      "school": "sydney grammar",
      "age": 12,
      "read_dir": "/tmp",
      "up_runtime_task_layer_number": 0
    })
    
    intest is: [{{.intest}}]
    ~SubStep1: [print:  ]
    intest is: [false]
    map[desc:the value of .intest is string but not bool so you can not simply use if .intest for condition name:correct_working_dir value:{{if eq .intest "true" }}{{.register_task_root.Output}}{{else}}{{.register_task_root.Output}}{{end}}]
    ~SubStep2: [reg:  ]
    after reg the var - contextual global:
    
    (*core.Cache)({
      "name": "little prince",
      "school": "sydney grammar",
      "intest": "false",
      "register_task_root": (*utils.ExecResult)({
        Cmd: "pwd",
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "correct_working_dir": "/up_project/up",
      "age": 12,
      "read_dir": "/tmp",
      "read_file": "mystory2.txt",
      "said": "Boa constrictors swallow their prey whole",
      "save_to": "/tmp/mystory2.txt",
      "last_result": (*utils.ExecResult)({
        Cmd: "pwd",
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      })
    })
    
    after reg the var - local:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "pwd",
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "save_to": "/tmp/mystory2.txt",
      "intest": "false",
      "register_task_root": (*utils.ExecResult)({
        Cmd: "pwd",
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "correct_working_dir": "/up_project/up",
      "said": "Boa constrictors swallow their prey whole",
      "read_file": "mystory2.txt",
      "name": "little prince",
      "school": "sydney grammar",
      "age": 12,
      "read_dir": "/tmp",
      "up_runtime_task_layer_number": 0
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
          "desc": "render a template file to a file 1",
          "cmd": {
            "src": "{{.correct_working_dir}}/tests/functests/d0072.template",
            "dest": "/tmp/mystory.txt"
          },
          "name": "template"
        },
        {
          "name": "readFile",
          "desc": "read content of a file and register it to a var",
          "cmd": {
            "filename": "mystory.txt",
            "dir": "/tmp",
            "reg": "my_interesting_story"
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
      "intest": "false",
      "register_task_root": (*utils.ExecResult)({
        Cmd: "pwd",
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "correct_working_dir": "/up_project/up",
      "save_to": "/tmp/mystory2.txt",
      "age": 12,
      "read_dir": "/tmp",
      "read_file": "mystory2.txt",
      "school": "sydney grammar",
      "up_runtime_task_layer_number": 0,
      "said": "Boa constrictors swallow their prey whole",
      "last_result": (*utils.ExecResult)({
        Cmd: "pwd",
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "name": "little prince"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "school": "sydney grammar",
      "intest": "false",
      "register_task_root": (*utils.ExecResult)({
        Cmd: "pwd",
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "correct_working_dir": "/up_project/up",
      "save_to": "/tmp/mystory2.txt",
      "age": 12,
      "read_dir": "/tmp",
      "up_runtime_task_layer_number": 0,
      "name": "little prince",
      "read_file": "mystory2.txt",
      "said": "Boa constrictors swallow their prey whole",
      "last_result": (*utils.ExecResult)({
        Cmd: "pwd",
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      })
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "name": "little prince",
      "said": "Boa constrictors swallow their prey whole",
      "last_result": (*utils.ExecResult)({
        Cmd: "pwd",
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "read_dir": "/tmp",
      "read_file": "mystory2.txt",
      "school": "sydney grammar",
      "intest": "false",
      "register_task_root": (*utils.ExecResult)({
        Cmd: "pwd",
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "correct_working_dir": "/up_project/up",
      "save_to": "/tmp/mystory2.txt",
      "age": 12,
      "up_runtime_task_layer_number": 0
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
      "said": "Boa constrictors swallow their prey whole",
      "save_to": "/tmp/mystory2.txt",
      "last_result": (*utils.ExecResult)({
        Cmd: "pwd",
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "my_interesting_story": "  My name is little prince, my school is sydney grammar\n  Once when I was 12 years old\n  In the book it said: Boa constrictors swallow their prey whole\n  I pondered deeply, then, over the adventures of the jungle.\n",
      "intest": "false",
      "register_task_root": (*utils.ExecResult)({
        Cmd: "pwd",
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "correct_working_dir": "/up_project/up",
      "age": 12,
      "read_dir": "/tmp",
      "read_file": "mystory2.txt",
      "name": "little prince",
      "school": "sydney grammar"
    })
    
    after reg the var - local:
    
    (*core.Cache)({
      "name": "little prince",
      "said": "Boa constrictors swallow their prey whole",
      "last_result": (*utils.ExecResult)({
        Cmd: "pwd",
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "read_dir": "/tmp",
      "read_file": "mystory2.txt",
      "school": "sydney grammar",
      "intest": "false",
      "register_task_root": (*utils.ExecResult)({
        Cmd: "pwd",
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "correct_working_dir": "/up_project/up",
      "save_to": "/tmp/mystory2.txt",
      "age": 12,
      "up_runtime_task_layer_number": 0,
      "my_interesting_story": "  My name is little prince, my school is sydney grammar\n  Once when I was 12 years old\n  In the book it said: Boa constrictors swallow their prey whole\n  I pondered deeply, then, over the adventures of the jungle.\n"
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
          "name": "template",
          "desc": "render a template file to a file 2",
          "cmd": {
            "src": "{{.correct_working_dir}}/tests/functests/d0072.template",
            "dest": "{{.save_to}}"
          }
        },
        {
          "name": "readFile",
          "desc": "read content of a file and register it to a var",
          "cmd": {
            "filename": "{{.read_file}}",
            "dir": "{{.read_dir}}",
            "reg": "my_interesting_story2"
          }
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
      "save_to": "/tmp/mystory2.txt",
      "correct_working_dir": "/up_project/up",
      "age": 12,
      "read_file": "mystory2.txt",
      "said": "Boa constrictors swallow their prey whole",
      "my_interesting_story": "  My name is little prince, my school is sydney grammar\n  Once when I was 12 years old\n  In the book it said: Boa constrictors swallow their prey whole\n  I pondered deeply, then, over the adventures of the jungle.\n",
      "register_task_root": (*utils.ExecResult)({
        Cmd: "pwd",
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "read_dir": "/tmp",
      "name": "little prince",
      "school": "sydney grammar",
      "intest": "false",
      "up_runtime_task_layer_number": 0,
      "last_result": (*utils.ExecResult)({
        Cmd: "pwd",
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      })
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "my_interesting_story": "  My name is little prince, my school is sydney grammar\n  Once when I was 12 years old\n  In the book it said: Boa constrictors swallow their prey whole\n  I pondered deeply, then, over the adventures of the jungle.\n",
      "save_to": "/tmp/mystory2.txt",
      "correct_working_dir": "/up_project/up",
      "name": "little prince",
      "school": "sydney grammar",
      "intest": "false",
      "last_result": (*utils.ExecResult)({
        Cmd: "pwd",
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "read_file": "mystory2.txt",
      "said": "Boa constrictors swallow their prey whole",
      "read_dir": "/tmp",
      "up_runtime_task_layer_number": 0,
      "register_task_root": (*utils.ExecResult)({
        Cmd: "pwd",
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "age": 12
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "school": "sydney grammar",
      "intest": "false",
      "up_runtime_task_layer_number": 0,
      "last_result": (*utils.ExecResult)({
        Cmd: "pwd",
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "my_interesting_story": "  My name is little prince, my school is sydney grammar\n  Once when I was 12 years old\n  In the book it said: Boa constrictors swallow their prey whole\n  I pondered deeply, then, over the adventures of the jungle.\n",
      "register_task_root": (*utils.ExecResult)({
        Cmd: "pwd",
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "read_dir": "/tmp",
      "name": "little prince",
      "said": "Boa constrictors swallow their prey whole",
      "save_to": "/tmp/mystory2.txt",
      "correct_working_dir": "/up_project/up",
      "age": 12,
      "read_file": "mystory2.txt"
    })
    
    map[dest:{{.save_to}} src:{{.correct_working_dir}}/tests/functests/d0072.template]
    ~SubStep1: [template: render a template file to a file 2 ]
    map[dir:{{.read_dir}} filename:{{.read_file}} reg:my_interesting_story2]
    ~SubStep2: [readFile: read content of a file and register it to a var ]
    after reg the var - contextual global:
    
    (*core.Cache)({
      "intest": "false",
      "register_task_root": (*utils.ExecResult)({
        Cmd: "pwd",
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "correct_working_dir": "/up_project/up",
      "age": 12,
      "read_dir": "/tmp",
      "read_file": "mystory2.txt",
      "name": "little prince",
      "school": "sydney grammar",
      "my_interesting_story2": "  My name is little prince, my school is sydney grammar\n  Once when I was 12 years old\n  In the book it said: Boa constrictors swallow their prey whole\n  I pondered deeply, then, over the adventures of the jungle.\n",
      "said": "Boa constrictors swallow their prey whole",
      "save_to": "/tmp/mystory2.txt",
      "last_result": (*utils.ExecResult)({
        Cmd: "pwd",
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "my_interesting_story": "  My name is little prince, my school is sydney grammar\n  Once when I was 12 years old\n  In the book it said: Boa constrictors swallow their prey whole\n  I pondered deeply, then, over the adventures of the jungle.\n"
    })
    
    after reg the var - local:
    
    (*core.Cache)({
      "save_to": "/tmp/mystory2.txt",
      "register_task_root": (*utils.ExecResult)({
        Cmd: "pwd",
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "name": "little prince",
      "intest": "false",
      "my_interesting_story": "  My name is little prince, my school is sydney grammar\n  Once when I was 12 years old\n  In the book it said: Boa constrictors swallow their prey whole\n  I pondered deeply, then, over the adventures of the jungle.\n",
      "correct_working_dir": "/up_project/up",
      "age": 12,
      "read_file": "mystory2.txt",
      "said": "Boa constrictors swallow their prey whole",
      "read_dir": "/tmp",
      "school": "sydney grammar",
      "up_runtime_task_layer_number": 0,
      "my_interesting_story2": "  My name is little prince, my school is sydney grammar\n  Once when I was 12 years old\n  In the book it said: Boa constrictors swallow their prey whole\n  I pondered deeply, then, over the adventures of the jungle.\n",
      "last_result": (*utils.ExecResult)({
        Cmd: "pwd",
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      })
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
