---
title: "c0006_vvvvv"
date: 2020-07-01T15:34:21+77:00
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
              ModuleName -> insane_darwin0
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0006
    -------full vars in scopes------
    (*impl.Scopes)(0xc000182f20)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [insane_darwin0] instance id: [dev]
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
    
    
    insane_darwin0: overall final exec vars:
    
    (*core.Cache)({
    })
    
    cmd( 1):
    echo "aaa: $aaa"
    
    
     \_ echo "aaa: $aaa"
    
    aaa:
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=4) "aaa:",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo "bbb: $bbb"
    
    
     \_ echo "bbb: $bbb"
    
    bbb:
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=4) "bbb:",
     ErrMsg: (string) ""
    }
    
    cmd( 3):
    echo "aaa':' $aaa"
    
     \_ echo "aaa':' $aaa"
    aaa':'
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=6) "aaa':'",
     ErrMsg: (string) ""
    }
    
    cmd( 4):
    echo "aaa":" $aaa"
    
     \_ echo "aaa":" $aaa"
    aaa:
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=4) "aaa:",
     ErrMsg: (string) ""
    }
    
    cmd( 5):
    echo "aaa -> $aaa"
    
     \_ echo "aaa -> $aaa"
    aaa ->
     .. ok
    (utils.ExecResult) {
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
