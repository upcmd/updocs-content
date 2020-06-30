---
title: "c0049_vvvvv"
date: 2020-07-01T15:34:27+77:00
draft: false
weight: 10494

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0049
                 Verbose -> vvvvv
              ModuleName -> elegant_albattani9
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0049
    -------full vars in scopes------
    (*impl.Scopes)(0xc00000e8c0)((len=1 cap=1) {
     (impl.Scope) {
      Name: (string) (len=6) "global",
      Ref: (string) "",
      RefDir: (string) "",
      Members: ([]string) <nil>,
      Vars: (core.Cache) <nil>,
      Dvars: (impl.Dvars) (len=1 cap=1) {
       (impl.Dvar) {
        Name: (string) (len=6) "SCHOOL",
        Value: (string) (len=11) "James Rules",
        Desc: (string) "",
        Expand: (int) 0,
        Flags: ([]string) (len=1 cap=1) {
         (string) (len=6) "envvar"
        },
        Rendered: (string) "",
        Secure: (*utils.SecureSetting)(<nil>),
        Ref: (string) "",
        RefDir: (string) "",
        DataKey: (string) "",
        DataPath: (string) "",
        DataTemplate: (string) ""
       }
      }
     }
    })
    
    [global] dvar expanded result:
    {
      "SCHOOL": "James Rules",
      "envvar_SCHOOL": "James Rules"
    }
    
    
    scope[global] merged: {
      "SCHOOL": "James Rules",
      "envvar_SCHOOL": "James Rules"
    }
    
    
    ---------group vars----------
    
    global: {
      "SCHOOL": "James Rules",
      "envvar_SCHOOL": "James Rules"
    }
    
    
    groups members:[]
    module: [elegant_albattani9] instance id: [dev]
    merged[ dev ] runtime vars:
    {
      "envvar_SCHOOL": "James Rules",
      "SCHOOL": "James Rules"
    }
    
    (core.Cache) (len=2) {
     (string) (len=13) "envvar_SCHOOL": (string) (len=11) "James Rules",
     (string) (len=6) "SCHOOL": (string) (len=11) "James Rules"
    }
    
    [runtime global] dvar expanded result:
    {
      "envvar_STUDENT_NAME": "James Bond",
      "STUDENT_AGE": "18",
      "envvar_STUDENT_AGE": "18",
      "STUDENT_NAME": "James Bond"
    }
    
    
    -------runtime global final merged with dvars-------
    
    {
      "envvar_SCHOOL": "James Rules",
      "SCHOOL": "James Rules",
      "STUDENT_NAME": "James Bond",
      "envvar_STUDENT_NAME": "James Bond",
      "STUDENT_AGE": "18",
      "envvar_STUDENT_AGE": "18"
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    {
      Name: "",
      Do: {
        "env |grep STUDENT_NAME",
        "env |grep STUDENT_AGE"
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
      "envvar_SCHOOL": "James Rules",
      "SCHOOL": "James Rules",
      "STUDENT_NAME": "James Bond",
      "envvar_STUDENT_NAME": "James Bond",
      "STUDENT_AGE": "18",
      "envvar_STUDENT_AGE": "18"
    })
    
    [local] dvar expanded result:
    {
      "envvar_STUDENT_NAME": "Tom Hanks",
      "STUDENT_NAME": "Tom Hanks"
    }
    
    
    scope[local] merged: {
      "envvar_STUDENT_NAME": "Tom Hanks",
      "STUDENT_AGE": "18",
      "envvar_STUDENT_AGE": "18",
      "envvar_SCHOOL": "James Rules",
      "SCHOOL": "James Rules",
      "STUDENT_NAME": "Tom Hanks"
    }
    
    
    elegant_albattani9: overall final exec vars:
    
    (*core.Cache)({
      "envvar_STUDENT_NAME": "Tom Hanks",
      "STUDENT_AGE": "18",
      "envvar_STUDENT_AGE": "18",
      "envvar_SCHOOL": "James Rules",
      "SCHOOL": "James Rules",
      "STUDENT_NAME": "Tom Hanks"
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
    
    cmd( 2):
    env |grep STUDENT_AGE
    
     \_ env |grep STUDENT_AGE
    STUDENT_AGE=18
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=14) "STUDENT_AGE=18",
     ErrMsg: (string) ""
    }
    
    . ok
    -Step2: [: since there is no local envvar for STUDENT_NAME
    it should use global envvar value 'james bond'
     ]
    {
      Name: "",
      Do: {
        "env |grep STUDENT_NAME",
        "env |grep STUDENT_AGE",
        "env |grep SCHOOL"
      },
      Dox: <nil>,
      Func: "shell",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "since there is no local envvar for STUDENT_NAME\nit should use global envvar value 'james bond'\n",
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
      "STUDENT_AGE": "18",
      "envvar_STUDENT_AGE": "18",
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "STUDENT_AGE=18",
        ErrMsg: ""
      }),
      "envvar_SCHOOL": "James Rules",
      "SCHOOL": "James Rules",
      "STUDENT_NAME": "James Bond",
      "envvar_STUDENT_NAME": "James Bond"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "envvar_SCHOOL": "James Rules",
      "SCHOOL": "James Rules",
      "STUDENT_NAME": "James Bond",
      "envvar_STUDENT_NAME": "James Bond",
      "STUDENT_AGE": "18",
      "envvar_STUDENT_AGE": "18",
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "STUDENT_AGE=18",
        ErrMsg: ""
      })
    }
    
    
    elegant_albattani9: overall final exec vars:
    
    (*core.Cache)({
      "STUDENT_AGE": "18",
      "envvar_STUDENT_AGE": "18",
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "STUDENT_AGE=18",
        ErrMsg: ""
      }),
      "envvar_SCHOOL": "James Rules",
      "SCHOOL": "James Rules",
      "STUDENT_NAME": "James Bond",
      "envvar_STUDENT_NAME": "James Bond"
    })
    
    cmd( 1):
    env |grep STUDENT_NAME
    
     \_ env |grep STUDENT_NAME
    STUDENT_NAME=James Bond
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=23) "STUDENT_NAME=James Bond",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    env |grep STUDENT_AGE
    
     \_ env |grep STUDENT_AGE
    STUDENT_AGE=18
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=14) "STUDENT_AGE=18",
     ErrMsg: (string) ""
    }
    
    cmd( 3):
    env |grep SCHOOL
    
     \_ env |grep SCHOOL
    SCHOOL=James Rules
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=18) "SCHOOL=James Rules",
     ErrMsg: (string) ""
    }
    
    . ok
    
```

##### Logs with different verbose level
* [c0049 log - verbose level v](../../logs/c0049_v)
* [c0049 log - verbose level vv](../../logs/c0049_vv)
* [c0049 log - verbose level vvv](../../logs/c0049_vvv)
* [c0049 log - verbose level vvvv](../../logs/c0049_vvvv)
* [c0049 log - verbose level vvvvv](../../logs/c0049_vvvvv)

##### References
* [Related Chapter](../../env-vars/c0049)
