---
title: "c0044_vvvvv"
date: 2020-06-27T03:09:20+66:00
draft: false
weight: 10444

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0044
                 Verbose -> vvvvv
              ModuleName -> elated_swartz9
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0044
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001ed0e0)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [elated_swartz9] instance id: [dev]
    merged[ dev ] runtime vars:
    {
    }
    
    (core.Cache) {
    }
    
    dvar> homedir:
    "/root"
    
    dvar> yourhome:
    "Your path is set to /root "
    
    [runtime global] dvar expanded result:
    {
      "homedir": "/root",
      "yourhome": "Your path is set to /root "
    }
    
    
    -------runtime global final merged with dvars-------
    
    {
      "yourhome": "Your path is set to /root ",
      "homedir": "/root"
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
          "cmd": "{{.homedir}}"
        },
        {
          "name": "print",
          "cmd": "{{.yourhome}}"
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
      "yourhome": "Your path is set to /root ",
      "homedir": "/root"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "homedir": "/root",
      "yourhome": "Your path is set to /root "
    }
    
    
    elated_swartz9: overall final exec vars:
    
    (*core.Cache)({
      "homedir": "/root",
      "yourhome": "Your path is set to /root "
    })
    
    {{.homedir}}
    ~SubStep1: [print:  ]
    /root
    {{.yourhome}}
    ~SubStep2: [print:  ]
    Your path is set to /root 
    -Step2:
    {
      Name: "",
      Do: {
        "echo \"\"\"my home is at {{.homedir}}\"\"\"",
        "echo \"\"\"my home is at $HOME\"\"\"",
        "echo \"\"\"{{.yourhome}}\"\"\""
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
      "homedir": "/root",
      "yourhome": "Your path is set to /root "
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "homedir": "/root",
      "yourhome": "Your path is set to /root "
    }
    
    
    elated_swartz9: overall final exec vars:
    
    (*core.Cache)({
      "homedir": "/root",
      "yourhome": "Your path is set to /root "
    })
    
    cmd( 1):
    echo """my home is at {{.homedir}}"""
    
     \_ echo """my home is at /root"""
    my home is at /root
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=19) "my home is at /root",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo """my home is at $HOME"""
    
     \_ echo """my home is at $HOME"""
    my home is at /root
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=19) "my home is at /root",
     ErrMsg: (string) ""
    }
    
    cmd( 3):
    echo """{{.yourhome}}"""
    
     \_ echo """Your path is set to /root """
    Your path is set to /root
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=25) "Your path is set to /root",
     ErrMsg: (string) ""
    }
    
    . ok
    
```

##### Logs with different verbose level
* [c0044 log - verbose level v](../../logs/c0044_v)
* [c0044 log - verbose level vv](../../logs/c0044_vv)
* [c0044 log - verbose level vvv](../../logs/c0044_vvv)
* [c0044 log - verbose level vvvv](../../logs/c0044_vvvv)
* [c0044 log - verbose level vvvvv](../../logs/c0044_vvvvv)

##### References
* [Related Chapter](../../env-vars/c0044)
