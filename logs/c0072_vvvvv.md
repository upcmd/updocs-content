---
title: "c0072_vvvvv"
date: 2020-06-27T03:09:23+66:00
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
              ModuleName -> cocky_meitner7
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0072
    -------full vars in scopes------
    (*impl.Scopes)(0xc000185380)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [cocky_meitner7] instance id: [dev]
    merged[ dev ] runtime vars:
    {
      "said": "Boa constrictors swallow their prey whole",
      "save_to": "/tmp/mystory2.txt",
      "read_dir": "/tmp",
      "read_file": "mystory2.txt",
      "name": "little prince",
      "school": "sydney grammar",
      "age": 12
    }
    
    (core.Cache) (len=7) {
     (string) (len=4) "said": (string) (len=41) "Boa constrictors swallow their prey whole",
     (string) (len=7) "save_to": (string) (len=17) "/tmp/mystory2.txt",
     (string) (len=8) "read_dir": (string) (len=4) "/tmp",
     (string) (len=9) "read_file": (string) (len=12) "mystory2.txt",
     (string) (len=4) "name": (string) (len=13) "little prince",
     (string) (len=6) "school": (string) (len=14) "sydney grammar",
     (string) (len=3) "age": (int) 12
    }
    
    [runtime global] dvar expanded result:
    {
      "intest": "false"
    }
    
    
    -------runtime global final merged with dvars-------
    
    {
      "intest": "false",
      "read_file": "mystory2.txt",
      "name": "little prince",
      "school": "sydney grammar",
      "age": 12,
      "said": "Boa constrictors swallow their prey whole",
      "save_to": "/tmp/mystory2.txt",
      "read_dir": "/tmp"
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
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "said": "Boa constrictors swallow their prey whole",
      "save_to": "/tmp/mystory2.txt",
      "read_dir": "/tmp",
      "intest": "false",
      "read_file": "mystory2.txt",
      "name": "little prince",
      "school": "sydney grammar",
      "age": 12
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "save_to": "/tmp/mystory2.txt",
      "read_dir": "/tmp",
      "intest": "false",
      "read_file": "mystory2.txt",
      "name": "little prince",
      "school": "sydney grammar",
      "age": 12,
      "said": "Boa constrictors swallow their prey whole"
    }
    
    
    cocky_meitner7: overall final exec vars:
    
    (*core.Cache)({
      "school": "sydney grammar",
      "age": 12,
      "said": "Boa constrictors swallow their prey whole",
      "save_to": "/tmp/mystory2.txt",
      "read_dir": "/tmp",
      "intest": "false",
      "read_file": "mystory2.txt",
      "name": "little prince"
    })
    
    cmd( 1):
    echo "?intest ->  {{.intest}}"
    
     \_ echo "?intest ->  false"
    ?intest ->  false
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=17) "?intest ->  false",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    pwd
    
     \_ pwd
    /up_project/up
     .. ok
    (utils.ExecResult) {
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
          "cmd": {
            "name": "correct_working_dir",
            "desc": "the value of .intest is string but not bool so you can not simply use if .intest for condition",
            "value": "{{if eq .intest \"true\" }}{{.register_task_root.Output}}{{else}}{{.register_task_root.Output}}{{end}}"
          },
          "name": "reg"
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
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "save_to": "/tmp/mystory2.txt",
      "intest": "false",
      "read_file": "mystory2.txt",
      "school": "sydney grammar",
      "said": "Boa constrictors swallow their prey whole",
      "read_dir": "/tmp",
      "register_task_root": (*utils.ExecResult)({
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "age": 12,
      "last_result": (*utils.ExecResult)({
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
      "name": "little prince",
      "said": "Boa constrictors swallow their prey whole",
      "read_dir": "/tmp",
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "save_to": "/tmp/mystory2.txt",
      "intest": "false",
      "register_task_root": (*utils.ExecResult)({
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "age": 12,
      "school": "sydney grammar",
      "read_file": "mystory2.txt"
    }
    
    
    cocky_meitner7: overall final exec vars:
    
    (*core.Cache)({
      "register_task_root": (*utils.ExecResult)({
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "age": 12,
      "school": "sydney grammar",
      "read_file": "mystory2.txt",
      "name": "little prince",
      "said": "Boa constrictors swallow their prey whole",
      "read_dir": "/tmp",
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "save_to": "/tmp/mystory2.txt",
      "intest": "false"
    })
    
    intest is: [{{.intest}}]
    ~SubStep1: [print:  ]
    intest is: [false]
    map[desc:the value of .intest is string but not bool so you can not simply use if .intest for condition name:correct_working_dir value:{{if eq .intest "true" }}{{.register_task_root.Output}}{{else}}{{.register_task_root.Output}}{{end}}]
    ~SubStep2: [reg:  ]
    after reg the var - contextual global:
    
    (*core.Cache)({
      "intest": "false",
      "register_task_root": (*utils.ExecResult)({
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "name": "little prince",
      "school": "sydney grammar",
      "said": "Boa constrictors swallow their prey whole",
      "save_to": "/tmp/mystory2.txt",
      "read_dir": "/tmp",
      "read_file": "mystory2.txt",
      "age": 12,
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "correct_working_dir": "/up_project/up"
    })
    
    after reg the var - local:
    
    (*core.Cache)({
      "register_task_root": (*utils.ExecResult)({
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "age": 12,
      "school": "sydney grammar",
      "read_file": "mystory2.txt",
      "name": "little prince",
      "said": "Boa constrictors swallow their prey whole",
      "read_dir": "/tmp",
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "save_to": "/tmp/mystory2.txt",
      "intest": "false",
      "correct_working_dir": "/up_project/up"
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
          "desc": "read content of a file and register it to a var",
          "cmd": {
            "dir": "/tmp",
            "reg": "my_interesting_story",
            "filename": "mystory.txt"
          },
          "name": "readfile"
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
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "correct_working_dir": "/up_project/up",
      "read_file": "mystory2.txt",
      "age": 12,
      "said": "Boa constrictors swallow their prey whole",
      "name": "little prince",
      "school": "sydney grammar",
      "register_task_root": (*utils.ExecResult)({
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "save_to": "/tmp/mystory2.txt",
      "read_dir": "/tmp",
      "intest": "false"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "school": "sydney grammar",
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "save_to": "/tmp/mystory2.txt",
      "intest": "false",
      "said": "Boa constrictors swallow their prey whole",
      "name": "little prince",
      "correct_working_dir": "/up_project/up",
      "read_file": "mystory2.txt",
      "age": 12,
      "read_dir": "/tmp",
      "register_task_root": (*utils.ExecResult)({
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      })
    }
    
    
    cocky_meitner7: overall final exec vars:
    
    (*core.Cache)({
      "read_dir": "/tmp",
      "register_task_root": (*utils.ExecResult)({
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "said": "Boa constrictors swallow their prey whole",
      "name": "little prince",
      "correct_working_dir": "/up_project/up",
      "read_file": "mystory2.txt",
      "age": 12,
      "save_to": "/tmp/mystory2.txt",
      "intest": "false",
      "school": "sydney grammar",
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      })
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
    ~SubStep4: [readfile: read content of a file and register it to a var ]
    after reg the var - contextual global:
    
    (*core.Cache)({
      "read_file": "mystory2.txt",
      "age": 12,
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "correct_working_dir": "/up_project/up",
      "name": "little prince",
      "school": "sydney grammar",
      "said": "Boa constrictors swallow their prey whole",
      "save_to": "/tmp/mystory2.txt",
      "read_dir": "/tmp",
      "intest": "false",
      "register_task_root": (*utils.ExecResult)({
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "my_interesting_story": "  My name is little prince, my school is sydney grammar\n  Once when I was 12 years old\n  In the book it said: Boa constrictors swallow their prey whole\n  I pondered deeply, then, over the adventures of the jungle.\n"
    })
    
    after reg the var - local:
    
    (*core.Cache)({
      "intest": "false",
      "school": "sydney grammar",
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "my_interesting_story": "  My name is little prince, my school is sydney grammar\n  Once when I was 12 years old\n  In the book it said: Boa constrictors swallow their prey whole\n  I pondered deeply, then, over the adventures of the jungle.\n",
      "save_to": "/tmp/mystory2.txt",
      "register_task_root": (*utils.ExecResult)({
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "said": "Boa constrictors swallow their prey whole",
      "name": "little prince",
      "correct_working_dir": "/up_project/up",
      "read_file": "mystory2.txt",
      "age": 12,
      "read_dir": "/tmp"
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
            "dest": "{{.save_to}}",
            "src": "{{.correct_working_dir}}/tests/functests/d0072.template"
          }
        },
        {
          "cmd": {
            "filename": "{{.read_file}}",
            "dir": "{{.read_dir}}",
            "reg": "my_interesting_story2"
          },
          "name": "readfile",
          "desc": "read content of a file and register it to a var"
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
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "correct_working_dir": "/up_project/up",
      "school": "sydney grammar",
      "said": "Boa constrictors swallow their prey whole",
      "intest": "false",
      "register_task_root": (*utils.ExecResult)({
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "my_interesting_story": "  My name is little prince, my school is sydney grammar\n  Once when I was 12 years old\n  In the book it said: Boa constrictors swallow their prey whole\n  I pondered deeply, then, over the adventures of the jungle.\n",
      "age": 12,
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "name": "little prince",
      "read_dir": "/tmp",
      "read_file": "mystory2.txt",
      "save_to": "/tmp/mystory2.txt"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "read_file": "mystory2.txt",
      "save_to": "/tmp/mystory2.txt",
      "read_dir": "/tmp",
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "correct_working_dir": "/up_project/up",
      "school": "sydney grammar",
      "register_task_root": (*utils.ExecResult)({
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "name": "little prince",
      "my_interesting_story": "  My name is little prince, my school is sydney grammar\n  Once when I was 12 years old\n  In the book it said: Boa constrictors swallow their prey whole\n  I pondered deeply, then, over the adventures of the jungle.\n",
      "age": 12,
      "said": "Boa constrictors swallow their prey whole",
      "intest": "false"
    }
    
    
    cocky_meitner7: overall final exec vars:
    
    (*core.Cache)({
      "my_interesting_story": "  My name is little prince, my school is sydney grammar\n  Once when I was 12 years old\n  In the book it said: Boa constrictors swallow their prey whole\n  I pondered deeply, then, over the adventures of the jungle.\n",
      "age": 12,
      "said": "Boa constrictors swallow their prey whole",
      "intest": "false",
      "name": "little prince",
      "read_dir": "/tmp",
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "correct_working_dir": "/up_project/up",
      "school": "sydney grammar",
      "register_task_root": (*utils.ExecResult)({
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "read_file": "mystory2.txt",
      "save_to": "/tmp/mystory2.txt"
    })
    
    map[dest:{{.save_to}} src:{{.correct_working_dir}}/tests/functests/d0072.template]
    ~SubStep1: [template: render a template file to a file 2 ]
    map[dir:{{.read_dir}} filename:{{.read_file}} reg:my_interesting_story2]
    ~SubStep2: [readfile: read content of a file and register it to a var ]
    after reg the var - contextual global:
    
    (*core.Cache)({
      "intest": "false",
      "register_task_root": (*utils.ExecResult)({
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "my_interesting_story": "  My name is little prince, my school is sydney grammar\n  Once when I was 12 years old\n  In the book it said: Boa constrictors swallow their prey whole\n  I pondered deeply, then, over the adventures of the jungle.\n",
      "name": "little prince",
      "school": "sydney grammar",
      "said": "Boa constrictors swallow their prey whole",
      "save_to": "/tmp/mystory2.txt",
      "read_dir": "/tmp",
      "read_file": "mystory2.txt",
      "age": 12,
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "correct_working_dir": "/up_project/up",
      "my_interesting_story2": "  My name is little prince, my school is sydney grammar\n  Once when I was 12 years old\n  In the book it said: Boa constrictors swallow their prey whole\n  I pondered deeply, then, over the adventures of the jungle.\n"
    })
    
    after reg the var - local:
    
    (*core.Cache)({
      "age": 12,
      "said": "Boa constrictors swallow their prey whole",
      "intest": "false",
      "name": "little prince",
      "my_interesting_story": "  My name is little prince, my school is sydney grammar\n  Once when I was 12 years old\n  In the book it said: Boa constrictors swallow their prey whole\n  I pondered deeply, then, over the adventures of the jungle.\n",
      "correct_working_dir": "/up_project/up",
      "school": "sydney grammar",
      "register_task_root": (*utils.ExecResult)({
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "read_file": "mystory2.txt",
      "save_to": "/tmp/mystory2.txt",
      "read_dir": "/tmp",
      "my_interesting_story2": "  My name is little prince, my school is sydney grammar\n  Once when I was 12 years old\n  In the book it said: Boa constrictors swallow their prey whole\n  I pondered deeply, then, over the adventures of the jungle.\n",
      "last_result": (*utils.ExecResult)({
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
