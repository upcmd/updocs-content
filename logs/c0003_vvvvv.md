---
title: "c0003_vvvvv"
date: 2020-06-27T03:09:13+66:00
draft: false
weight: 10034

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0003
                 Verbose -> vvvvv
              ModuleName -> evil_bohr0
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0003
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001c6e20)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [evil_bohr0] instance id: [dev]
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
    Task1: [task ==> task: this is task1 ]
    Executing task stack layer: 1
    
    -Step1: [: do step1 in shell func ]
    {
      Name: "",
      Do: "echo \"hello\"\necho \"world\"\n",
      Dox: <nil>,
      Func: "shell",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "do step1 in shell func",
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
    
    
    evil_bohr0: overall final exec vars:
    
    (*core.Cache)({
    })
    
    cmd( 1):
    echo "hello"
    echo "world"
    
    
     \_ echo "hello"
    echo "world"
    
    hello
    world
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=11) "hello\nworld",
     ErrMsg: (string) ""
    }
    
    . ok
    
```

##### Logs with different verbose level
* [c0003 log - verbose level v](../../logs/c0003_v)
* [c0003 log - verbose level vv](../../logs/c0003_vv)
* [c0003 log - verbose level vvv](../../logs/c0003_vvv)
* [c0003 log - verbose level vvvv](../../logs/c0003_vvvv)
* [c0003 log - verbose level vvvvv](../../logs/c0003_vvvvv)

##### References
* [Related Chapter](../../quick-start/c0003)
