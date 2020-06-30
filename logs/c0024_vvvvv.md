---
title: "c0024_vvvvv"
date: 2020-07-01T15:34:23+77:00
draft: false
weight: 10244

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0024
                 Verbose -> vvvvv
              ModuleName -> determined_bohr7
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0024
    -------full vars in scopes------
    (*impl.Scopes)(0xc00000e480)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [determined_bohr7] instance id: [dev]
    merged[ dev ] runtime vars:
    {
      "student": {
        "name": "Tom",
        "gender": "Male",
        "school": "Sydney Grammar"
      }
    }
    
    (core.Cache) (len=1) {
     (string) (len=7) "student": (map[string]interface {}) (len=3) {
      (string) (len=4) "name": (string) (len=3) "Tom",
      (string) (len=6) "gender": (string) (len=4) "Male",
      (string) (len=6) "school": (string) (len=14) "Sydney Grammar"
     }
    }
    
    [runtime global] dvar expanded result:
    {
      "studentname": "Tom",
      "studentgender": "Male"
    }
    
    
    -------runtime global final merged with dvars-------
    
    {
      "student": {
        "gender": "Male",
        "school": "Sydney Grammar",
        "name": "Tom"
      },
      "studentname": "Tom",
      "studentgender": "Male"
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    {
      Name: "",
      Do: {
        "echo \"student=>{{.student}}\"",
        "echo \"name=>{{.studentname}}\"",
        "echo \"gender=>{{.studentgender}}\"",
        "echo \"school=>{{.student.school}}\""
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
        "school": "Sydney Grammar",
        "name": "Tom",
        "gender": "Male"
      },
      "studentname": "Tom",
      "studentgender": "Male"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "student": {
        "school": "Sydney Grammar",
        "name": "Tom",
        "gender": "Male"
      },
      "studentname": "Tom",
      "studentgender": "Male"
    }
    
    
    determined_bohr7: overall final exec vars:
    
    (*core.Cache)({
      "studentgender": "Male",
      "student": {
        "gender": "Male",
        "school": "Sydney Grammar",
        "name": "Tom"
      },
      "studentname": "Tom"
    })
    
    cmd( 1):
    echo "student=>{{.student}}"
    
     \_ echo "student=>map[gender:Male name:Tom school:Sydney Grammar]"
    student=>map[gender:Male name:Tom school:Sydney Grammar]
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=56) "student=>map[gender:Male name:Tom school:Sydney Grammar]",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo "name=>{{.studentname}}"
    
     \_ echo "name=>Tom"
    name=>Tom
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=9) "name=>Tom",
     ErrMsg: (string) ""
    }
    
    cmd( 3):
    echo "gender=>{{.studentgender}}"
    
     \_ echo "gender=>Male"
    gender=>Male
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=12) "gender=>Male",
     ErrMsg: (string) ""
    }
    
    cmd( 4):
    echo "school=>{{.student.school}}"
    
     \_ echo "school=>Sydney Grammar"
    school=>Sydney Grammar
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=22) "school=>Sydney Grammar",
     ErrMsg: (string) ""
    }
    
    . ok
    
```

##### Logs with different verbose level
* [c0024 log - verbose level v](../../logs/c0024_v)
* [c0024 log - verbose level vv](../../logs/c0024_vv)
* [c0024 log - verbose level vvv](../../logs/c0024_vvv)
* [c0024 log - verbose level vvvv](../../logs/c0024_vvvv)
* [c0024 log - verbose level vvvvv](../../logs/c0024_vvvvv)

##### References
* [Related Chapter](../../dvars/c0024)
