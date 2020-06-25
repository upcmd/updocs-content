---
title: "c0089_vvvvv"
date: 2020-06-25T01:55:52+66:00
draft: false
weight: 10894

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0089
                 Verbose -> vvvvv
              ModuleName -> naughty_wozniak7
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0089
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001ced80)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [naughty_wozniak7] instance id: [dev]
    merged[ dev ] runtime vars:
    {
      "dynadir": "./tests/functests"
    }
    
    (core.Cache) (len=1) {
     (string) (len=7) "dynadir": (string) (len=17) "./tests/functests"
    }
    
    [runtime global] dvar expanded result:
    {
    }
    
    
    -------runtime global final merged with dvars-------
    
    {
      "dynadir": "./tests/functests"
    }
    
    loading [flow ref]:  ./tests/functests/c0089-task-main.yml
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    {
      Name: "",
      Do: {
        "echo \"task step 1\"",
        "echo \"task step 2\""
      },
      Dox: <nil>,
      Func: "shell",
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
      "dynadir": "./tests/functests"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "dynadir": "./tests/functests"
    }
    
    
    naughty_wozniak7: overall final exec vars:
    
    (*core.Cache)({
      "dynadir": "./tests/functests"
    })
    
    cmd( 1):
    echo "task step 1"
    
     \_ echo "task step 1"
    task step 1
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=11) "task step 1",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo "task step 2"
    
     \_ echo "task step 2"
    task step 2
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=11) "task step 2",
     ErrMsg: (string) ""
    }
    
    . ok
    
```

##### Logs with different verbose level
* [c0089 log - verbose level v](../../logs/c0089_v)
* [c0089 log - verbose level vv](../../logs/c0089_vv)
* [c0089 log - verbose level vvv](../../logs/c0089_vvv)
* [c0089 log - verbose level vvvv](../../logs/c0089_vvvv)
* [c0089 log - verbose level vvvvv](../../logs/c0089_vvvvv)

##### References
* [Related Chapter](../../organization/c0089)