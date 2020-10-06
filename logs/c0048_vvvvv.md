---
title: "c0048_vvvvv"
date: 2020-10-07T00:11:08+1010:00
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
    loading [Task]:  ./tests/functests/c0048
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001bf2e0)(<nil>)
    
    ---------group vars----------
    
    global: (*core.Cache)({
    })
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    (*core.Cache)({
    })
    
    (*core.Cache)(0xc00000e910)({
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
    
    -Step1: [
    The envVar flag makes the dvar name STUDENT_NAME is accessible as environment vars
    ]
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
      Desc: "The envVar flag makes the dvar name STUDENT_NAME is accessible as environment vars\n",
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
      "STUDENT_NAME": "Tom Hanks",
      "envVar_STUDENT_NAME": "Tom Hanks"
    }
    
    
    scope[local] merged: {
      "envVar_STUDENT_NAME": "Tom Hanks",
      "up_runtime_task_layer_number": 0,
      "STUDENT_NAME": "Tom Hanks"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "STUDENT_NAME": "Tom Hanks",
      "envVar_STUDENT_NAME": "Tom Hanks"
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
    
    . ok
    -Step2: [
    STUDENT_NAME is also accessible in dvar processing
    ]
    {
      Name: "",
      Do: {
        "env |grep STUDENT_NAME",
        "echo \"student_name_re_map is [{{.student_name_re_map}}]\""
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
        },
        {
          Name: "student_name_re_map",
          Value: "{{ env \"STUDENT_NAME\" |default \"student_name_re_map\" }}",
          Desc: "",
          Expand: 0,
          Flags: <nil>,
          Rendered: "",
          Secure: (*utils.SecureSetting)(<nil>),
          Ref: "",
          RefDir: "",
          DataKey: "",
          DataPath: "",
          DataTemplate: ""
        }
      },
      Desc: "STUDENT_NAME is also accessible in dvar processing\n",
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
        Cmd: "env |grep STUDENT_NAME",
        Code: 0,
        Output: "STUDENT_NAME=Tom Hanks",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0
    })
    
    [local] dvar expanded result:
    {
      "STUDENT_NAME": "Tom Hanks",
      "envVar_STUDENT_NAME": "Tom Hanks",
      "student_name_re_map": "Tom Hanks"
    }
    
    
    scope[local] merged: {
      "envVar_STUDENT_NAME": "Tom Hanks",
      "student_name_re_map": "Tom Hanks",
      "last_result": (*utils.ExecResult)({
        Cmd: "env |grep STUDENT_NAME",
        Code: 0,
        Output: "STUDENT_NAME=Tom Hanks",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0,
      "STUDENT_NAME": "Tom Hanks"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "STUDENT_NAME": "Tom Hanks",
      "envVar_STUDENT_NAME": "Tom Hanks",
      "student_name_re_map": "Tom Hanks",
      "last_result": (*utils.ExecResult)({
        Cmd: "env |grep STUDENT_NAME",
        Code: 0,
        Output: "STUDENT_NAME=Tom Hanks",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0
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
    echo "student_name_re_map is [{{.student_name_re_map}}]"
    
    cmd=>:
    echo "student_name_re_map is [Tom Hanks]"
    -
    student_name_re_map is [Tom Hanks]
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=41) "echo \"student_name_re_map is [Tom Hanks]\"",
     Code: (int) 0,
     Output: (string) (len=34) "student_name_re_map is [Tom Hanks]",
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
