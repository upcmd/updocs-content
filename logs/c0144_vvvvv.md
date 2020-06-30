---
title: "c0144_vvvvv"
date: 2020-07-01T15:34:42+77:00
draft: false
weight: 11444

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0144
                 Verbose -> vvvvv
              ModuleName -> sharp_torvalds0
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0144
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001f2dc0)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [sharp_torvalds0] instance id: [dev]
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
    
    -Step1: [: main job ]
    {
      Name: "",
      Do: {
        "pwd"
      },
      Dox: <nil>,
      Func: "shell",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "main job",
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
    
    
    sharp_torvalds0: overall final exec vars:
    
    (*core.Cache)({
    })
    
    cmd( 1):
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
    
```

##### Logs with different verbose level
* [c0144 log - verbose level v](../../logs/c0144_v)
* [c0144 log - verbose level vv](../../logs/c0144_vv)
* [c0144 log - verbose level vvv](../../logs/c0144_vvv)
* [c0144 log - verbose level vvvv](../../logs/c0144_vvvv)
* [c0144 log - verbose level vvvvv](../../logs/c0144_vvvvv)

##### References
* [Related Chapter](../../usage/c0144)
