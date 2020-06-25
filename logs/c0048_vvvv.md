---
title: "c0048_vvvv"
date: 2020-06-25T01:55:44+66:00
draft: false
weight: 10483

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0048
                 Verbose -> vvvv
              ModuleName -> high_goodall1
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0048
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [high_goodall1] instance id: [dev]
    merged[ dev ] runtime vars:
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
        "env |grep STUDENT_NAME"
      },
      Dox: <nil>,
      Func: "shell",
      Vars: <nil>,
      Dvars: {
        {
          Name: "STUDENT_NAME",
          Value: "Tom Hanks",
          Desc: "",
          Expand: 0,
          Flags: {
            "envvar"
          },
          Rendered: "",
          Secure: (*utils.SecureSetting)(<nil>),
          Ref: "",
          RefDir: "",
          DataKey: "",
          DataPath: "",
          DataTemplate: ""
        }
      },
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
    
    high_goodall1: overall final exec vars:
    
    (*core.Cache)({
      "STUDENT_NAME": "Tom Hanks",
      "envvar_STUDENT_NAME": "Tom Hanks"
    })
    
    cmd( 1):
    env |grep STUDENT_NAME
    
     \_ env |grep STUDENT_NAME
    STUDENT_NAME=Tom Hanks
     .. ok
    . ok
    
```

##### Logs with different verbose level
* [c0048 log - verbose level v](../../logs/c0048_v)
* [c0048 log - verbose level vv](../../logs/c0048_vv)
* [c0048 log - verbose level vvv](../../logs/c0048_vvv)
* [c0048 log - verbose level vvvv](../../logs/c0048_vvvv)
* [c0048 log - verbose level vvvvv](../../logs/c0048_vvvvv)

##### References
* [Related Chapter](../../env-vars/c0048)
