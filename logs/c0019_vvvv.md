---
title: "c0019_vvvv"
date: 2020-06-27T03:09:15+66:00
draft: false
weight: 10193

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
                 Verbose -> vvvv
              ModuleName -> reverent_noyce8
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0019
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [reverent_noyce8] instance id: [dev]
    merged[ dev ] runtime vars:
    {
      "sg": {
        "name": "sydney grammar",
        "address": "Sydney, NSW 2000"
      },
      "school": "sydney grammar"
    }
    
    -------runtime global final merged with dvars-------
    
    {
      "sg": {
        "name": "sydney grammar",
        "address": "Sydney, NSW 2000"
      },
      "school": "sydney grammar"
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
      "sg": {
        "name": "sydney grammar",
        "address": "Sydney, NSW 2000"
      },
      "school": "sydney grammar",
      "studentname": "Tom"
    })
    
    reverent_noyce8: overall final exec vars:
    
    (*core.Cache)({
      "studentname": "Tom",
      "sg": {
        "name": "sydney grammar",
        "address": "Sydney, NSW 2000"
      },
      "school": "sydney grammar"
    })
    
    cmd( 1):
    echo "studentname -> {{.studentname}}"
    
     \_ echo "studentname -> Tom"
    studentname -> Tom
     .. ok
    cmd( 2):
    echo "gender -> male"
    
     \_ echo "gender -> male"
    gender -> male
     .. ok
    cmd( 3):
    echo "school -> {{.school}}"
    
     \_ echo "school -> sydney grammar"
    school -> sydney grammar
     .. ok
    cmd( 4):
    echo "nonexist -> {{.notexist}}"
    
     \_ echo "nonexist -> <no value>"
    nonexist -> <no value>
     .. ok
    cmd( 5):
    echo "SG details -> {{.sg.name}}/{{.sg.address}}"
    
     \_ echo "SG details -> sydney grammar/Sydney, NSW 2000"
    SG details -> sydney grammar/Sydney, NSW 2000
     .. ok
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
