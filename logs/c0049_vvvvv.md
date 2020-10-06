---
title: "c0049_vvvvv"
date: 2020-10-07T00:11:08+1010:00
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
    loading [Task]:  ./tests/functests/c0049
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001e7500)((len=1 cap=1) {
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
         (string) (len=6) "envVar"
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
      "envVar_SCHOOL": "James Rules"
    }
    
    
    scope[global] merged: {
      "SCHOOL": "James Rules",
      "envVar_SCHOOL": "James Rules"
    }
    
    
    ---------group vars----------
    
    global: (*core.Cache)({
      "SCHOOL": "James Rules",
      "envVar_SCHOOL": "James Rules"
    })
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    (*core.Cache)({
      "SCHOOL": "James Rules",
      "envVar_SCHOOL": "James Rules"
    })
    
    (*core.Cache)(0xc000126980)((len=2) {
     (string) (len=6) "SCHOOL": (string) (len=11) "James Rules",
     (string) (len=13) "envVar_SCHOOL": (string) (len=11) "James Rules"
    })
    
    [runtime global] dvar expanded result:
    {
      "STUDENT_NAME": "James Bond",
      "envVar_STUDENT_NAME": "James Bond",
      "STUDENT_AGE": "18",
      "envVar_STUDENT_AGE": "18"
    }
    
    
    -------runtime global final merged with dvars-------
    
    (*core.Cache)({
      "envVar_SCHOOL": "James Rules",
      "envVar_STUDENT_NAME": "James Bond",
      "STUDENT_AGE": "18",
      "envVar_STUDENT_AGE": "18",
      "STUDENT_NAME": "James Bond",
      "SCHOOL": "James Rules"
    })
    
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
            "envVar"
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
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "STUDENT_NAME": "James Bond",
      "SCHOOL": "James Rules",
      "up_runtime_task_layer_number": 0,
      "envVar_SCHOOL": "James Rules",
      "envVar_STUDENT_NAME": "James Bond",
      "STUDENT_AGE": "18",
      "envVar_STUDENT_AGE": "18"
    })
    
    [local] dvar expanded result:
    {
      "STUDENT_NAME": "Tom Hanks",
      "envVar_STUDENT_NAME": "Tom Hanks"
    }
    
    
    scope[local] merged: {
      "STUDENT_AGE": "18",
      "envVar_STUDENT_AGE": "18",
      "STUDENT_NAME": "Tom Hanks",
      "SCHOOL": "James Rules",
      "up_runtime_task_layer_number": 0,
      "envVar_SCHOOL": "James Rules",
      "envVar_STUDENT_NAME": "Tom Hanks"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "envVar_STUDENT_AGE": "18",
      "STUDENT_NAME": "Tom Hanks",
      "SCHOOL": "James Rules",
      "up_runtime_task_layer_number": 0,
      "envVar_SCHOOL": "James Rules",
      "envVar_STUDENT_NAME": "Tom Hanks",
      "STUDENT_AGE": "18"
    })
    
    cmd( 1):
    env |grep STUDENT_NAME
    
    cmd=>:
    env |grep STUDENT_NAME
    -
    STUDENT_NAME=Tom Hanks
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=22) "env |grep STUDENT_NAME",
     Code: (int) 0,
     Output: (string) (len=22) "STUDENT_NAME=Tom Hanks",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    env |grep STUDENT_AGE
    
    cmd=>:
    env |grep STUDENT_AGE
    -
    STUDENT_AGE=18
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=21) "env |grep STUDENT_AGE",
     Code: (int) 0,
     Output: (string) (len=14) "STUDENT_AGE=18",
     ErrMsg: (string) ""
    }
    
    . ok
    -Step2: [
    since there is no local envVar for STUDENT_NAME
    it should use global envVar value 'james bond'
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
      Desc: "since there is no local envVar for STUDENT_NAME\nit should use global envVar value 'james bond'\n",
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
      "last_result": (*utils.ExecResult)({
        Cmd: "env |grep STUDENT_AGE",
        Code: 0,
        Output: "STUDENT_AGE=18",
        ErrMsg: ""
      }),
      "SCHOOL": "James Rules",
      "up_runtime_task_layer_number": 0,
      "envVar_SCHOOL": "James Rules",
      "envVar_STUDENT_NAME": "James Bond",
      "STUDENT_AGE": "18",
      "envVar_STUDENT_AGE": "18",
      "STUDENT_NAME": "James Bond"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "envVar_SCHOOL": "James Rules",
      "envVar_STUDENT_NAME": "James Bond",
      "STUDENT_AGE": "18",
      "envVar_STUDENT_AGE": "18",
      "STUDENT_NAME": "James Bond",
      "last_result": (*utils.ExecResult)({
        Cmd: "env |grep STUDENT_AGE",
        Code: 0,
        Output: "STUDENT_AGE=18",
        ErrMsg: ""
      }),
      "SCHOOL": "James Rules",
      "up_runtime_task_layer_number": 0
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "env |grep STUDENT_AGE",
        Code: 0,
        Output: "STUDENT_AGE=18",
        ErrMsg: ""
      }),
      "SCHOOL": "James Rules",
      "up_runtime_task_layer_number": 0,
      "envVar_SCHOOL": "James Rules",
      "envVar_STUDENT_NAME": "James Bond",
      "STUDENT_AGE": "18",
      "envVar_STUDENT_AGE": "18",
      "STUDENT_NAME": "James Bond"
    })
    
    cmd( 1):
    env |grep STUDENT_NAME
    
    cmd=>:
    env |grep STUDENT_NAME
    -
    STUDENT_NAME=James Bond
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=22) "env |grep STUDENT_NAME",
     Code: (int) 0,
     Output: (string) (len=23) "STUDENT_NAME=James Bond",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    env |grep STUDENT_AGE
    
    cmd=>:
    env |grep STUDENT_AGE
    -
    STUDENT_AGE=18
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=21) "env |grep STUDENT_AGE",
     Code: (int) 0,
     Output: (string) (len=14) "STUDENT_AGE=18",
     ErrMsg: (string) ""
    }
    
    cmd( 3):
    env |grep SCHOOL
    
    cmd=>:
    env |grep SCHOOL
    -
    SCHOOL=James Rules
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=16) "env |grep SCHOOL",
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
