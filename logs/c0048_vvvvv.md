---
title: "c0048_vvvvv"
date: 2020-06-25T01:55:44+66:00
draft: false
weight: 10484

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
                 Verbose -> vvvvv
              ModuleName -> berserk_tesla6
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0048
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001a0820)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [berserk_tesla6] instance id: [dev]
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
    
    [local] dvar expanded result:
    {
      "STUDENT_NAME": "Tom Hanks",
      "envvar_STUDENT_NAME": "Tom Hanks"
    }
    
    
    scope[local] merged: {
      "STUDENT_NAME": "Tom Hanks",
      "envvar_STUDENT_NAME": "Tom Hanks"
    }
    
    
    berserk_tesla6: overall final exec vars:
    
    (*core.Cache)({
      "STUDENT_NAME": "Tom Hanks",
      "envvar_STUDENT_NAME": "Tom Hanks"
    })
    
    cmd( 1):
    env |grep STUDENT_NAME
    
     \_ env |grep STUDENT_NAME
    STUDENT_NAME=Tom Hanks
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=22) "STUDENT_NAME=Tom Hanks",
     ErrMsg: (string) ""
    }
    
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
