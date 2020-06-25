---
title: "c0024_vvvv"
date: 2020-06-25T01:55:40+66:00
draft: false
weight: 10243

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
                 Verbose -> vvvv
              ModuleName -> evil_lumiere5
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0024
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [evil_lumiere5] instance id: [dev]
    merged[ dev ] runtime vars:
    {
      "student": {
        "school": "Sydney Grammar",
        "name": "Tom",
        "gender": "Male"
      }
    }
    
    -------runtime global final merged with dvars-------
    
    {
      "student": {
        "school": "Sydney Grammar",
        "name": "Tom",
        "gender": "Male"
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
    
    evil_lumiere5: overall final exec vars:
    
    (*core.Cache)({
      "studentname": "Tom",
      "studentgender": "Male",
      "student": {
        "school": "Sydney Grammar",
        "name": "Tom",
        "gender": "Male"
      }
    })
    
    cmd( 1):
    echo "student=>{{.student}}"
    
     \_ echo "student=>map[gender:Male name:Tom school:Sydney Grammar]"
    student=>map[gender:Male name:Tom school:Sydney Grammar]
     .. ok
    cmd( 2):
    echo "name=>{{.studentname}}"
    
     \_ echo "name=>Tom"
    name=>Tom
     .. ok
    cmd( 3):
    echo "gender=>{{.studentgender}}"
    
     \_ echo "gender=>Male"
    gender=>Male
     .. ok
    cmd( 4):
    echo "school=>{{.student.school}}"
    
     \_ echo "school=>Sydney Grammar"
    school=>Sydney Grammar
     .. ok
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
