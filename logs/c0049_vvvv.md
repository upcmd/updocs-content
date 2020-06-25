---
title: "c0049_vvvv"
date: 2020-06-25T01:55:45+66:00
draft: false
weight: 10493

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
                 Verbose -> vvvv
              ModuleName -> fervent_kowalevski4
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0049
    ---------group vars----------
    
    global: {
      "envvar_SCHOOL": "James Rules",
      "SCHOOL": "James Rules"
    }
    
    
    groups members:[]
    module: [fervent_kowalevski4] instance id: [dev]
    merged[ dev ] runtime vars:
    {
      "envvar_SCHOOL": "James Rules",
      "SCHOOL": "James Rules"
    }
    
    -------runtime global final merged with dvars-------
    
    {
      "envvar_STUDENT_AGE": "18",
      "envvar_SCHOOL": "James Rules",
      "SCHOOL": "James Rules",
      "STUDENT_NAME": "James Bond",
      "envvar_STUDENT_NAME": "James Bond",
      "STUDENT_AGE": "18"
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
    
    fervent_kowalevski4: overall final exec vars:
    
    (*core.Cache)({
      "envvar_STUDENT_AGE": "18",
      "envvar_SCHOOL": "James Rules",
      "SCHOOL": "James Rules",
      "STUDENT_NAME": "Tom Hanks",
      "envvar_STUDENT_NAME": "Tom Hanks",
      "STUDENT_AGE": "18"
    })
    
    cmd( 1):
    env |grep STUDENT_NAME
    
     \_ env |grep STUDENT_NAME
    STUDENT_NAME=Tom Hanks
     .. ok
    cmd( 2):
    env |grep STUDENT_AGE
    
     \_ env |grep STUDENT_AGE
    STUDENT_AGE=18
     .. ok
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
      "STUDENT_NAME": "James Bond",
      "envvar_STUDENT_NAME": "James Bond",
      "STUDENT_AGE": "18",
      "envvar_STUDENT_AGE": "18",
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "STUDENT_AGE=18",
        ErrMsg: ""
      }),
      "envvar_SCHOOL": "James Rules",
      "SCHOOL": "James Rules"
    })
    
    fervent_kowalevski4: overall final exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "STUDENT_AGE=18",
        ErrMsg: ""
      }),
      "envvar_SCHOOL": "James Rules",
      "SCHOOL": "James Rules",
      "STUDENT_NAME": "James Bond",
      "envvar_STUDENT_NAME": "James Bond",
      "STUDENT_AGE": "18",
      "envvar_STUDENT_AGE": "18"
    })
    
    cmd( 1):
    env |grep STUDENT_NAME
    
     \_ env |grep STUDENT_NAME
    STUDENT_NAME=James Bond
     .. ok
    cmd( 2):
    env |grep STUDENT_AGE
    
     \_ env |grep STUDENT_AGE
    STUDENT_AGE=18
     .. ok
    cmd( 3):
    env |grep SCHOOL
    
     \_ env |grep SCHOOL
    SCHOOL=James Rules
     .. ok
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
