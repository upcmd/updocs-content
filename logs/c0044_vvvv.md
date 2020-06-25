---
title: "c0044_vvvv"
date: 2020-06-25T01:55:44+66:00
draft: false
weight: 10443

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
                 Verbose -> vvvv
              ModuleName -> determined_yalow7
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0044
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [determined_yalow7] instance id: [dev]
    merged[ dev ] runtime vars:
    {
    }
    
    dvar> homedir:
    "/root"
    
    dvar> yourhome:
    "Your path is set to /root "
    
    -------runtime global final merged with dvars-------
    
    {
      "homedir": "/root",
      "yourhome": "Your path is set to /root "
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
      "homedir": "/root",
      "yourhome": "Your path is set to /root "
    })
    
    determined_yalow7: overall final exec vars:
    
    (*core.Cache)({
      "homedir": "/root",
      "yourhome": "Your path is set to /root "
    })
    
    ~SubStep1: [print:  ]
    /root
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
    
    determined_yalow7: overall final exec vars:
    
    (*core.Cache)({
      "yourhome": "Your path is set to /root ",
      "homedir": "/root"
    })
    
    cmd( 1):
    echo """my home is at {{.homedir}}"""
    
     \_ echo """my home is at /root"""
    my home is at /root
     .. ok
    cmd( 2):
    echo """my home is at $HOME"""
    
     \_ echo """my home is at $HOME"""
    my home is at /root
     .. ok
    cmd( 3):
    echo """{{.yourhome}}"""
    
     \_ echo """Your path is set to /root """
    Your path is set to /root
     .. ok
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