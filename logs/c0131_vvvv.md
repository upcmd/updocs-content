---
title: "c0131_vvvv"
date: 2020-06-27T03:09:32+66:00
draft: false
weight: 11313

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0131
                 Verbose -> vvvv
              ModuleName -> adoring_morse3
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0131
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [adoring_morse3] instance id: [dev]
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
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "true/false value of goahead:\n{{.goahead}}\n{{not .goahead}}\n"
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
    })
    
    adoring_morse3: overall final exec vars:
    
    (*core.Cache)({
    })
    
    ~SubStep1: [print:  ]
    true/false value of goahead:
    <no value>
    true
    
    -Step2: [: show use a flow in else ]
    {
      Name: "",
      Do: {
        "goahead"
      },
      Dox: <nil>,
      Func: "call",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "show use a flow in else",
      Reg: "",
      Flags: <nil>,
      If: "{{.goahead}}",
      Else: {
        {
          "func": "cmd",
          "do": {
            {
              "name": "print",
              "cmd": "do something else step1 ......."
            }
          }
        },
        {
          "func": "shell",
          "do": {
            "echo do something else step2 ......."
          }
        },
        {
          "func": "cmd",
          "do": {
            {
              "name": "print",
              "cmd": "do something else step3 ......."
            }
          }
        },
        {
          "func": "call",
          "desc": "show it is same that you could assemble a list of tasks for if true condition",
          "vars": {
            "goahead": true
          },
          "do": {
            "goelse"
          }
        }
      },
      Loop: <nil>,
      Until: "",
      RefDir: "",
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
    })
    
    adoring_morse3: overall final exec vars:
    
    (*core.Cache)({
    })
    
    condition failed, skip executing step 
    
    
```

##### Logs with different verbose level
* [c0131 log - verbose level v](../../logs/c0131_v)
* [c0131 log - verbose level vv](../../logs/c0131_vv)
* [c0131 log - verbose level vvv](../../logs/c0131_vvv)
* [c0131 log - verbose level vvvv](../../logs/c0131_vvvv)
* [c0131 log - verbose level vvvvv](../../logs/c0131_vvvvv)

##### References
* [Related Chapter](../../flow-controll/c0131)
