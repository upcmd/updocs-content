---
title: "c0072_vvvv"
date: 2020-06-25T01:55:49+66:00
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
              ModuleName -> elegant_almeida7
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0072
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [elegant_almeida7] instance id: [dev]
    merged[ dev ] runtime vars:
    {
      "read_dir": "/tmp",
      "read_file": "mystory2.txt",
      "name": "little prince",
      "school": "sydney grammar",
      "age": 12,
      "said": "Boa constrictors swallow their prey whole",
      "save_to": "/tmp/mystory2.txt"
    }
    
    -------runtime global final merged with dvars-------
    
    {
      "read_file": "mystory2.txt",
      "name": "little prince",
      "school": "sydney grammar",
      "age": 12,
      "said": "Boa constrictors swallow their prey whole",
      "save_to": "/tmp/mystory2.txt",
      "intest": "false",
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
      "intest": "false",
      "read_dir": "/tmp",
      "read_file": "mystory2.txt",
      "name": "little prince",
      "school": "sydney grammar",
      "age": 12,
      "said": "Boa constrictors swallow their prey whole",
      "save_to": "/tmp/mystory2.txt"
    })
    
    elegant_almeida7: overall final exec vars:
    
    (*core.Cache)({
      "read_file": "mystory2.txt",
      "name": "little prince",
      "school": "sydney grammar",
      "age": 12,
      "said": "Boa constrictors swallow their prey whole",
      "save_to": "/tmp/mystory2.txt",
      "intest": "false",
      "read_dir": "/tmp"
    })
    
    cmd( 1):
    echo "?intest ->  {{.intest}}"
    
     \_ echo "?intest ->  false"
    ?intest ->  false
     .. ok
    cmd( 2):
    pwd
    
     \_ pwd
    /up_project/up
     .. ok
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
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "school": "sydney grammar",
      "save_to": "/tmp/mystory2.txt",
      "said": "Boa constrictors swallow their prey whole",
      "intest": "false",
      "age": 12,
      "read_file": "mystory2.txt",
      "register_task_root": (*utils.ExecResult)({
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "read_dir": "/tmp",
      "name": "little prince"
    })
    
    elegant_almeida7: overall final exec vars:
    
    (*core.Cache)({
      "read_file": "mystory2.txt",
      "read_dir": "/tmp",
      "save_to": "/tmp/mystory2.txt",
      "intest": "false",
      "register_task_root": (*utils.ExecResult)({
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "name": "little prince",
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "school": "sydney grammar",
      "said": "Boa constrictors swallow their prey whole",
      "age": 12
    })
    
    ~SubStep1: [print:  ]
    intest is: [false]
    ~SubStep2: [reg:  ]
    -Step3:
    {
      Name: "",
      Do: {
        {
          "cmd": "root dir is: [{{.register_task_root.Output}}]",
          "name": "print"
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
          "name": "readfile",
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
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "read_dir": "/tmp",
      "name": "little prince",
      "said": "Boa constrictors swallow their prey whole",
      "intest": "false",
      "correct_working_dir": "/up_project/up",
      "read_file": "mystory2.txt",
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "age": 12,
      "register_task_root": (*utils.ExecResult)({
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "school": "sydney grammar",
      "save_to": "/tmp/mystory2.txt"
    })
    
    elegant_almeida7: overall final exec vars:
    
    (*core.Cache)({
      "read_dir": "/tmp",
      "said": "Boa constrictors swallow their prey whole",
      "age": 12,
      "school": "sydney grammar",
      "correct_working_dir": "/up_project/up",
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "name": "little prince",
      "intest": "false",
      "register_task_root": (*utils.ExecResult)({
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "save_to": "/tmp/mystory2.txt",
      "read_file": "mystory2.txt"
    })
    
    ~SubStep1: [print:  ]
    root dir is: [/up_project/up]
    ~SubStep2: [print:  ]
    correct working dir is: [/up_project/up]
    ~SubStep3: [template: render a template file to a file 1 ]
    ~SubStep4: [readfile: read content of a file and register it to a var ]
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
          "desc": "read content of a file and register it to a var",
          "cmd": {
            "dir": "{{.read_dir}}",
            "reg": "my_interesting_story2",
            "filename": "{{.read_file}}"
          },
          "name": "readfile"
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
      "save_to": "/tmp/mystory2.txt",
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "my_interesting_story": "  My name is little prince, my school is sydney grammar\n  Once when I was 12 years old\n  In the book it said: Boa constrictors swallow their prey whole\n  I pondered deeply, then, over the adventures of the jungle.\n",
      "read_file": "mystory2.txt",
      "school": "sydney grammar",
      "age": 12,
      "said": "Boa constrictors swallow their prey whole",
      "intest": "false",
      "register_task_root": (*utils.ExecResult)({
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "correct_working_dir": "/up_project/up",
      "read_dir": "/tmp",
      "name": "little prince"
    })
    
    elegant_almeida7: overall final exec vars:
    
    (*core.Cache)({
      "said": "Boa constrictors swallow their prey whole",
      "register_task_root": (*utils.ExecResult)({
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "school": "sydney grammar",
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "read_file": "mystory2.txt",
      "age": 12,
      "correct_working_dir": "/up_project/up",
      "read_dir": "/tmp",
      "save_to": "/tmp/mystory2.txt",
      "my_interesting_story": "  My name is little prince, my school is sydney grammar\n  Once when I was 12 years old\n  In the book it said: Boa constrictors swallow their prey whole\n  I pondered deeply, then, over the adventures of the jungle.\n",
      "name": "little prince",
      "intest": "false"
    })
    
    ~SubStep1: [template: render a template file to a file 2 ]
    ~SubStep2: [readfile: read content of a file and register it to a var ]
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