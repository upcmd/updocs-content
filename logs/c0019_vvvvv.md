---
title: "c0019_vvvvv"
date: 2020-10-07T00:11:03+1010:00
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
    loading [Task]:  ./tests/functests/c0019
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc000174f80)(<nil>)
    
    ---------group vars----------
    
    global: (*core.Cache)({
    })
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    (*core.Cache)({
      "sg": {
        "name": "sydney grammar",
        "address": "Sydney, NSW 2000"
      },
      "school": "sydney grammar"
    })
    
    (*core.Cache)(0xc0000b6908)((len=2) {
     (string) (len=6) "school": (string) (len=14) "sydney grammar",
     (string) (len=2) "sg": (map[string]interface {}) (len=2) {
      (string) (len=4) "name": (string) (len=14) "sydney grammar",
      (string) (len=7) "address": (string) (len=16) "Sydney, NSW 2000"
     }
    })
    
    [runtime global] dvar expanded result:
    {
    }
    
    
    -------runtime global final merged with dvars-------
    
    (*core.Cache)({
      "sg": {
        "address": "Sydney, NSW 2000",
        "name": "sydney grammar"
      },
      "school": "sydney grammar"
    })
    
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
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "studentname": "Tom",
      "school": "sydney grammar",
      "sg": {
        "address": "Sydney, NSW 2000",
        "name": "sydney grammar"
      },
      "up_runtime_task_layer_number": 0
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 0,
      "studentname": "Tom",
      "school": "sydney grammar",
      "sg": {
        "name": "sydney grammar",
        "address": "Sydney, NSW 2000"
      }
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "studentname": "Tom",
      "school": "sydney grammar",
      "sg": {
        "address": "Sydney, NSW 2000",
        "name": "sydney grammar"
      }
    })
    
    cmd( 1):
    echo "studentname -> {{.studentname}}"
    
    cmd=>:
    echo "studentname -> Tom"
    -
    studentname -> Tom
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=25) "echo \"studentname -> Tom\"",
     Code: (int) 0,
     Output: (string) (len=18) "studentname -> Tom",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo "gender -> male"
    
    cmd=>:
    echo "gender -> male"
    -
    gender -> male
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=21) "echo \"gender -> male\"",
     Code: (int) 0,
     Output: (string) (len=14) "gender -> male",
     ErrMsg: (string) ""
    }
    
    cmd( 3):
    echo "school -> {{.school}}"
    
    cmd=>:
    echo "school -> sydney grammar"
    -
    school -> sydney grammar
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=31) "echo \"school -> sydney grammar\"",
     Code: (int) 0,
     Output: (string) (len=24) "school -> sydney grammar",
     ErrMsg: (string) ""
    }
    
    cmd( 4):
    echo "nonexist -> {{.notexist}}"
    
    cmd=>:
    echo "nonexist -> <no value>"
    -
    nonexist -> <no value>
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=29) "echo \"nonexist -> <no value>\"",
     Code: (int) 0,
     Output: (string) (len=22) "nonexist -> <no value>",
     ErrMsg: (string) ""
    }
    
    cmd( 5):
    echo "SG details -> {{.sg.name}}/{{.sg.address}}"
    
    cmd=>:
    echo "SG details -> sydney grammar/Sydney, NSW 2000"
    -
    SG details -> sydney grammar/Sydney, NSW 2000
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=52) "echo \"SG details -> sydney grammar/Sydney, NSW 2000\"",
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
