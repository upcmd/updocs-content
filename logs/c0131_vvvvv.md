---
title: "c0131_vvvvv"
date: 2020-06-27T03:09:32+66:00
draft: false
weight: 11314

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
                 Verbose -> vvvvv
              ModuleName -> desperate_cori7
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0131
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001cf540)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [desperate_cori7] instance id: [dev]
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
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
    }
    
    
    desperate_cori7: overall final exec vars:
    
    (*core.Cache)({
    })
    
    true/false value of goahead:
    {{.goahead}}
    {{not .goahead}}
    
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
              "cmd": "do something else step3 .......",
              "name": "print"
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
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
    }
    
    
    desperate_cori7: overall final exec vars:
    
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
