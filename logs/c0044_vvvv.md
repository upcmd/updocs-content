---
title: "c0044_vvvv"
date: 2020-08-09T01:36:05+88:00
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
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
                 Timeout -> 3600000
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0044
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    {
    }
    
    dvar> homedir:
    "/root"
    
    -
    /root
    dvar> yourhome:
    "Your path is set to /root "
    
    -
    Your path is set to /root 
    -------runtime global final merged with dvars-------
    
    {
      "homedir": "/root",
      "yourhome": "Your path is set to /root "
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "homedir": "/root",
      "yourhome": "Your path is set to /root "
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "homedir": "/root",
      "yourhome": "Your path is set to /root "
    })
    
    ~SubStep1: [print:  ]
    /root
    ~SubStep2: [print:  ]
    Your path is set to /root 
    -Step2:
    current exec runtime vars:
    (*core.Cache)({
      "homedir": "/root",
      "yourhome": "Your path is set to /root "
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "homedir": "/root",
      "yourhome": "Your path is set to /root "
    })
    
    cmd( 1):
    echo """my home is at {{.homedir}}"""
    
    cmd=>:
    echo """my home is at /root"""<=
    my home is at /root
     .. ok
    cmd( 2):
    echo """my home is at $HOME"""
    
    cmd=>:
    echo """my home is at $HOME"""<=
    my home is at /root
     .. ok
    cmd( 3):
    echo """{{.yourhome}}"""
    
    cmd=>:
    echo """Your path is set to /root """<=
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
