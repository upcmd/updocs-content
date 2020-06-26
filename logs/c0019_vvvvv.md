---
title: "c0019_vvvvv"
date: 2020-06-27T03:09:16+66:00
draft: false
weight: 10194

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0019
                 Verbose -> vvvvv
              ModuleName -> cranky_hodgkin2
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0019
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001ecea0)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [cranky_hodgkin2] instance id: [dev]
    merged[ dev ] runtime vars:
    {
      "school": "sydney grammar",
      "sg": {
        "name": "sydney grammar",
        "address": "Sydney, NSW 2000"
      }
    }
    
    (core.Cache) (len=2) {
     (string) (len=6) "school": (string) (len=14) "sydney grammar",
     (string) (len=2) "sg": (map[string]interface {}) (len=2) {
      (string) (len=7) "address": (string) (len=16) "Sydney, NSW 2000",
      (string) (len=4) "name": (string) (len=14) "sydney grammar"
     }
    }
    
    [runtime global] dvar expanded result:
    {
    }
    
    
    -------runtime global final merged with dvars-------
    
    {
      "school": "sydney grammar",
      "sg": {
        "name": "sydney grammar",
        "address": "Sydney, NSW 2000"
      }
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    {
      Name: "",
      Do: {
        "echo \"studentname -> {{.studentname}}\"",
        "echo \"gender -> male\"",
        "echo \"school -> {{.school}}\"",
        "echo \"nonexist -> {{.notexist}}\"",
        "echo \"SG details -> {{.sg.name}}/{{.sg.address}}\""
      },
      Dox: <nil>,
      Func: "shell",
      Vars: {
        "studentname": "Tom"
      },
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
      "school": "sydney grammar",
      "sg": {
        "name": "sydney grammar",
        "address": "Sydney, NSW 2000"
      },
      "studentname": "Tom"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "school": "sydney grammar",
      "sg": {
        "address": "Sydney, NSW 2000",
        "name": "sydney grammar"
      },
      "studentname": "Tom"
    }
    
    
    cranky_hodgkin2: overall final exec vars:
    
    (*core.Cache)({
      "sg": {
        "address": "Sydney, NSW 2000",
        "name": "sydney grammar"
      },
      "studentname": "Tom",
      "school": "sydney grammar"
    })
    
    cmd( 1):
    echo "studentname -> {{.studentname}}"
    
     \_ echo "studentname -> Tom"
    studentname -> Tom
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=18) "studentname -> Tom",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo "gender -> male"
    
     \_ echo "gender -> male"
    gender -> male
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=14) "gender -> male",
     ErrMsg: (string) ""
    }
    
    cmd( 3):
    echo "school -> {{.school}}"
    
     \_ echo "school -> sydney grammar"
    school -> sydney grammar
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=24) "school -> sydney grammar",
     ErrMsg: (string) ""
    }
    
    cmd( 4):
    echo "nonexist -> {{.notexist}}"
    
     \_ echo "nonexist -> <no value>"
    nonexist -> <no value>
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=22) "nonexist -> <no value>",
     ErrMsg: (string) ""
    }
    
    cmd( 5):
    echo "SG details -> {{.sg.name}}/{{.sg.address}}"
    
     \_ echo "SG details -> sydney grammar/Sydney, NSW 2000"
    SG details -> sydney grammar/Sydney, NSW 2000
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=45) "SG details -> sydney grammar/Sydney, NSW 2000",
     ErrMsg: (string) ""
    }
    
    . ok
    
```

##### Logs with different verbose level
* [c0019 log - verbose level v](../../logs/c0019_v)
* [c0019 log - verbose level vv](../../logs/c0019_vv)
* [c0019 log - verbose level vvv](../../logs/c0019_vvv)
* [c0019 log - verbose level vvvv](../../logs/c0019_vvvv)
* [c0019 log - verbose level vvvvv](../../logs/c0019_vvvvv)

##### References
* [Related Chapter](../../vars/c0019)
