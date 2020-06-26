---
title: "c0120_vvvvv"
date: 2020-06-27T03:09:31+66:00
draft: false
weight: 11204

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0120
                 Verbose -> vvvvv
              ModuleName -> high_curie4
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0120
    -------full vars in scopes------
    (*impl.Scopes)(0xc00000e460)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [high_curie4] instance id: [dev]
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
    Task1: [task ==> task: main entry ]
    Executing task stack layer: 1
    
    -Step1:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "step1"
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
    
    
    high_curie4: overall final exec vars:
    
    (*core.Cache)({
    })
    
    step1
    ~SubStep1: [print:  ]
    step1
    -Step2:
    {
      Name: "",
      Do: {
        {
          "name": "break"
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
    
    
    high_curie4: overall final exec vars:
    
    (*core.Cache)({
    })
    
    ~SubStep1: [break:  ]
    -Step3:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "step2"
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
    
     WARN: [break] - [client chose to break]
    
```

##### Logs with different verbose level
* [c0120 log - verbose level v](../../logs/c0120_v)
* [c0120 log - verbose level vv](../../logs/c0120_vv)
* [c0120 log - verbose level vvv](../../logs/c0120_vvv)
* [c0120 log - verbose level vvvv](../../logs/c0120_vvvv)
* [c0120 log - verbose level vvvvv](../../logs/c0120_vvvvv)

##### References
* [Related Chapter](../../cmd-func/c0120)
