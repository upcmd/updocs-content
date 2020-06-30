---
title: "c0102_vvvv"
date: 2020-07-01T15:34:34+77:00
draft: false
weight: 11023

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0102
                 Verbose -> vvvv
              ModuleName -> silly_pike4
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0102
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [silly_pike4] instance id: [dev]
    merged[ dev ] runtime vars:
    {
      "mock_yml": "tom:\n  sex: male\n  age: 23\njason:\n  sex: male\n  age: 35\nemily:\n  sex: female\n  age: 32\n"
    }
    
    -------runtime global final merged with dvars-------
    
    {
      "mock_yml": "tom:\n  sex: male\n  age: 23\njason:\n  sex: male\n  age: 35\nemily:\n  sex: female\n  age: 32\n"
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    {
      Name: "",
      Do: {
        "echo \"{{.mock_yml}}\" > /tmp/mock_yml.yml"
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
      "mock_yml": "tom:\n  sex: male\n  age: 23\njason:\n  sex: male\n  age: 35\nemily:\n  sex: female\n  age: 32\n"
    })
    
    silly_pike4: overall final exec vars:
    
    (*core.Cache)({
      "mock_yml": "tom:\n  sex: male\n  age: 23\njason:\n  sex: male\n  age: 35\nemily:\n  sex: female\n  age: 32\n"
    })
    
    cmd( 1):
    echo "{{.mock_yml}}" > /tmp/mock_yml.yml
    
     \_ echo "tom:
      sex: male
      age: 23
    jason:
      sex: male
      age: 35
    emily:
      sex: female
      age: 32
    " > /tmp/mock_yml.yml
    
     .. ok
    . ok
    -Step2: [: inplace modification ]
    {
      Name: "",
      Do: {
        {
          "flags": {
            "inplace"
          },
          "name": "yml_delete",
          "cmd": {
            "ymlfile": "mock_yml.yml",
            "refdir": "/tmp",
            "path": "jason.sex",
            "verbose": "v"
          }
        },
        {
          "name": "readfile",
          "desc": "check new file content",
          "cmd": {
            "filename": "mock_yml.yml",
            "dir": "/tmp",
            "reg": "new_yml"
          }
        },
        {
          "name": "print",
          "desc": "show the modified yml content read from file",
          "cmd": "{{.new_yml}}"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "inplace modification",
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
      "mock_yml": "tom:\n  sex: male\n  age: 23\njason:\n  sex: male\n  age: 35\nemily:\n  sex: female\n  age: 32\n",
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "",
        ErrMsg: ""
      })
    })
    
    silly_pike4: overall final exec vars:
    
    (*core.Cache)({
      "mock_yml": "tom:\n  sex: male\n  age: 23\njason:\n  sex: male\n  age: 35\nemily:\n  sex: female\n  age: 32\n",
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "",
        ErrMsg: ""
      })
    })
    
    ~SubStep1: [yml_delete:  ]
    ~SubStep2: [readfile: check new file content ]
    ~SubStep3: [print: show the modified yml content read from file ]
    tom:
      sex: male
      age: 23
    jason:
      age: 35
    emily:
      sex: female
      age: 32
    
    -Step3: [: modify in memory and register to cache ]
    {
      Name: "",
      Do: {
        {
          "name": "yml_delete",
          "cmd": {
            "path": "jason.sex",
            "verbose": "vvvv",
            "reg": "modified_yml",
            "ymlfile": "mock_yml.yml",
            "refdir": "/tmp"
          },
          "flags": {
            "localonly"
          }
        },
        {
          "desc": "show the modified yml content registered",
          "cmd": "{{.modified_yml}}",
          "name": "print"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "modify in memory and register to cache",
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
      "mock_yml": "tom:\n  sex: male\n  age: 23\njason:\n  sex: male\n  age: 35\nemily:\n  sex: female\n  age: 32\n",
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "",
        ErrMsg: ""
      }),
      "new_yml": "tom:\n  sex: male\n  age: 23\njason:\n  age: 35\nemily:\n  sex: female\n  age: 32\n"
    })
    
    silly_pike4: overall final exec vars:
    
    (*core.Cache)({
      "mock_yml": "tom:\n  sex: male\n  age: 23\njason:\n  sex: male\n  age: 35\nemily:\n  sex: female\n  age: 32\n",
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "",
        ErrMsg: ""
      }),
      "new_yml": "tom:\n  sex: male\n  age: 23\njason:\n  age: 35\nemily:\n  sex: female\n  age: 32\n"
    })
    
    ~SubStep1: [yml_delete:  ]
    ~SubStep2: [print: show the modified yml content registered ]
    tom:
      sex: male
      age: 23
    jason:
      age: 35
    emily:
      sex: female
      age: 32
    
    
```

##### Logs with different verbose level
* [c0102 log - verbose level v](../../logs/c0102_v)
* [c0102 log - verbose level vv](../../logs/c0102_vv)
* [c0102 log - verbose level vvv](../../logs/c0102_vvv)
* [c0102 log - verbose level vvvv](../../logs/c0102_vvvv)
* [c0102 log - verbose level vvvvv](../../logs/c0102_vvvvv)

##### References
* [Related Chapter](../../cmd-func/c0102)
