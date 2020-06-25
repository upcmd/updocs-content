---
title: "c0064_vvvvv"
date: 2020-06-25T01:55:47+66:00
draft: false
weight: 10644

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0064
                 Verbose -> vvvvv
              ModuleName -> kickass_yonath1
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0064
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001eaf20)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [kickass_yonath1] instance id: [dev]
    merged[ dev ] runtime vars:
    {
      "student": {
        "school": "Sydney Grammar",
        "name": "Tom",
        "gender": "Male"
      }
    }
    
    (core.Cache) (len=1) {
     (string) (len=7) "student": (map[string]interface {}) (len=3) {
      (string) (len=6) "gender": (string) (len=4) "Male",
      (string) (len=6) "school": (string) (len=14) "Sydney Grammar",
      (string) (len=4) "name": (string) (len=3) "Tom"
     }
    }
    
    [runtime global] dvar expanded result:
    {
    }
    
    
    -------runtime global final merged with dvars-------
    
    {
      "student": {
        "school": "Sydney Grammar",
        "name": "Tom",
        "gender": "Male"
      }
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    {
      Name: "",
      Do: {
        "echo \"hello 1\""
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
      "student": {
        "name": "Tom",
        "gender": "Male",
        "school": "Sydney Grammar"
      }
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "student": {
        "name": "Tom",
        "gender": "Male",
        "school": "Sydney Grammar"
      }
    }
    
    
    kickass_yonath1: overall final exec vars:
    
    (*core.Cache)({
      "student": {
        "name": "Tom",
        "gender": "Male",
        "school": "Sydney Grammar"
      }
    })
    
    cmd( 1):
    echo "hello 1"
    
     \_ echo "hello 1"
    hello 1
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=7) "hello 1",
     ErrMsg: (string) ""
    }
    
    . ok
    -Step2:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "desc": "print some info",
          "cmd": "hello, this is print commmand"
        },
        {
          "cmd": "hello, {{.student.school}}",
          "name": "print"
        },
        {
          "name": "print",
          "cmd": "hello, {{.student.school}}\nhello, {{.student.school}}\n"
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
      "student": {
        "name": "Tom",
        "gender": "Male",
        "school": "Sydney Grammar"
      },
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "hello 1",
        ErrMsg: ""
      })
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "student": {
        "gender": "Male",
        "school": "Sydney Grammar",
        "name": "Tom"
      },
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "hello 1",
        ErrMsg: ""
      })
    }
    
    
    kickass_yonath1: overall final exec vars:
    
    (*core.Cache)({
      "student": {
        "gender": "Male",
        "school": "Sydney Grammar",
        "name": "Tom"
      },
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "hello 1",
        ErrMsg: ""
      })
    })
    
    hello, this is print commmand
    ~SubStep1: [print: print some info ]
    hello, this is print commmand
    hello, {{.student.school}}
    ~SubStep2: [print:  ]
    hello, Sydney Grammar
    hello, {{.student.school}}
    hello, {{.student.school}}
    
    ~SubStep3: [print:  ]
    hello, Sydney Grammar
    hello, Sydney Grammar
    
    
```

##### Logs with different verbose level
* [c0064 log - verbose level v](../../logs/c0064_v)
* [c0064 log - verbose level vv](../../logs/c0064_vv)
* [c0064 log - verbose level vvv](../../logs/c0064_vvv)
* [c0064 log - verbose level vvvv](../../logs/c0064_vvvv)
* [c0064 log - verbose level vvvvv](../../logs/c0064_vvvvv)

##### References
* [Related Chapter](../../cmd-func/c0064)