---
title: "c0006_vvvvv"
date: 2020-10-07T00:11:01+1010:00
draft: false
weight: 10064

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0006
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
    loading [Task]:  ./tests/functests/c0006
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc000264fe0)(<nil>)
    
    ---------group vars----------
    
    global: (*core.Cache)({
    })
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    (*core.Cache)({
    })
    
    (*core.Cache)(0xc0000bc8c8)({
    })
    
    [runtime global] dvar expanded result:
    {
    }
    
    
    -------runtime global final merged with dvars-------
    
    (*core.Cache)({
    })
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1: [: to test display env vars from shell context ]
    {
      Name: "",
      Do: {
        "echo \"aaa: $aaa\"\n",
        "echo \"bbb: $bbb\"\n",
        "echo \"aaa':' $aaa\"",
        "echo \"aaa\":\" $aaa\"",
        "echo \"aaa -> $aaa\""
      },
      Dox: <nil>,
      Func: "shell",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "to test display env vars from shell context",
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
      "up_runtime_task_layer_number": 0
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 0
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0
    })
    
    cmd( 1):
    echo "aaa: $aaa"
    
    
    cmd=>:
    echo "aaa: $aaa"
    
    -
    aaa: 
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=17) "echo \"aaa: $aaa\"\n",
     Code: (int) 0,
     Output: (string) (len=4) "aaa:",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo "bbb: $bbb"
    
    
    cmd=>:
    echo "bbb: $bbb"
    
    -
    bbb: 
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=17) "echo \"bbb: $bbb\"\n",
     Code: (int) 0,
     Output: (string) (len=4) "bbb:",
     ErrMsg: (string) ""
    }
    
    cmd( 3):
    echo "aaa':' $aaa"
    
    cmd=>:
    echo "aaa':' $aaa"
    -
    aaa':' 
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=18) "echo \"aaa':' $aaa\"",
     Code: (int) 0,
     Output: (string) (len=6) "aaa':'",
     ErrMsg: (string) ""
    }
    
    cmd( 4):
    echo "aaa":" $aaa"
    
    cmd=>:
    echo "aaa":" $aaa"
    -
    aaa: 
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=18) "echo \"aaa\":\" $aaa\"",
     Code: (int) 0,
     Output: (string) (len=4) "aaa:",
     ErrMsg: (string) ""
    }
    
    cmd( 5):
    echo "aaa -> $aaa"
    
    cmd=>:
    echo "aaa -> $aaa"
    -
    aaa -> 
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=18) "echo \"aaa -> $aaa\"",
     Code: (int) 0,
     Output: (string) (len=6) "aaa ->",
     ErrMsg: (string) ""
    }
    
    . ok
    
```

##### Logs with different verbose level
* [c0006 log - verbose level v](../../logs/c0006_v)
* [c0006 log - verbose level vv](../../logs/c0006_vv)
* [c0006 log - verbose level vvv](../../logs/c0006_vvv)
* [c0006 log - verbose level vvvv](../../logs/c0006_vvvv)
* [c0006 log - verbose level vvvvv](../../logs/c0006_vvvvv)

##### References
* [Related Chapter](../../quick-start/c0006)
