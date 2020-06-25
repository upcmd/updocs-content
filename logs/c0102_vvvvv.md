---
title: "c0102_vvvvv"
date: 2020-06-25T01:55:56+66:00
draft: false
weight: 11024

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
                 Verbose -> vvvvv
              ModuleName -> sad_franklin8
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0102
    -------full vars in scopes------
    (*impl.Scopes)(0xc000159260)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [sad_franklin8] instance id: [dev]
    merged[ dev ] runtime vars:
    {
      "mock_yml": "tom:\n  sex: male\n  age: 23\njason:\n  sex: male\n  age: 35\nemily:\n  sex: female\n  age: 32\n"
    }
    
    (core.Cache) (len=1) {
     (string) (len=8) "mock_yml": (string) (len=87) "tom:\n  sex: male\n  age: 23\njason:\n  sex: male\n  age: 35\nemily:\n  sex: female\n  age: 32\n"
    }
    
    [runtime global] dvar expanded result:
    {
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
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "mock_yml": "tom:\n  sex: male\n  age: 23\njason:\n  sex: male\n  age: 35\nemily:\n  sex: female\n  age: 32\n"
    }
    
    
    sad_franklin8: overall final exec vars:
    
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
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) "",
     ErrMsg: (string) ""
    }
    
    . ok
    -Step2: [: inplace modification ]
    {
      Name: "",
      Do: {
        {
          "name": "yml_delete",
          "cmd": {
            "verbose": "v",
            "ymlfile": "mock_yml.yml",
            "refdir": "/tmp",
            "path": "jason.sex"
          },
          "flags": {
            "inplace"
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
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "mock_yml": "tom:\n  sex: male\n  age: 23\njason:\n  sex: male\n  age: 35\nemily:\n  sex: female\n  age: 32\n",
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "",
        ErrMsg: ""
      })
    }
    
    
    sad_franklin8: overall final exec vars:
    
    (*core.Cache)({
      "mock_yml": "tom:\n  sex: male\n  age: 23\njason:\n  sex: male\n  age: 35\nemily:\n  sex: female\n  age: 32\n",
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "",
        ErrMsg: ""
      })
    })
    
    map[path:jason.sex refdir:/tmp verbose:v ymlfile:mock_yml.yml]
    ~SubStep1: [yml_delete:  ]
    yml modified:
    
    ""
    
    map[dir:/tmp filename:mock_yml.yml reg:new_yml]
    ~SubStep2: [readfile: check new file content ]
    after reg the var - contextual global:
    
    (*core.Cache)({
      "mock_yml": "tom:\n  sex: male\n  age: 23\njason:\n  sex: male\n  age: 35\nemily:\n  sex: female\n  age: 32\n",
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "",
        ErrMsg: ""
      }),
      "new_yml": "tom:\n  sex: male\n  age: 23\njason:\n  age: 35\nemily:\n  sex: female\n  age: 32\n"
    })
    
    after reg the var - local:
    
    (*core.Cache)({
      "mock_yml": "tom:\n  sex: male\n  age: 23\njason:\n  sex: male\n  age: 35\nemily:\n  sex: female\n  age: 32\n",
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "",
        ErrMsg: ""
      }),
      "new_yml": "tom:\n  sex: male\n  age: 23\njason:\n  age: 35\nemily:\n  sex: female\n  age: 32\n"
    })
    
    {{.new_yml}}
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
            "reg": "modified_yml",
            "ymlfile": "mock_yml.yml",
            "refdir": "/tmp",
            "path": "jason.sex",
            "verbose": "vvvv"
          },
          "flags": {
            "localonly"
          }
        },
        {
          "cmd": "{{.modified_yml}}",
          "name": "print",
          "desc": "show the modified yml content registered"
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
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "mock_yml": "tom:\n  sex: male\n  age: 23\njason:\n  sex: male\n  age: 35\nemily:\n  sex: female\n  age: 32\n",
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "",
        ErrMsg: ""
      }),
      "new_yml": "tom:\n  sex: male\n  age: 23\njason:\n  age: 35\nemily:\n  sex: female\n  age: 32\n"
    }
    
    
    sad_franklin8: overall final exec vars:
    
    (*core.Cache)({
      "mock_yml": "tom:\n  sex: male\n  age: 23\njason:\n  sex: male\n  age: 35\nemily:\n  sex: female\n  age: 32\n",
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "",
        ErrMsg: ""
      }),
      "new_yml": "tom:\n  sex: male\n  age: 23\njason:\n  age: 35\nemily:\n  sex: female\n  age: 32\n"
    })
    
    map[path:jason.sex refdir:/tmp reg:modified_yml verbose:vvvv ymlfile:mock_yml.yml]
    ~SubStep1: [yml_delete:  ]
    yml modified:
    
    "tom:\n  sex: male\n  age: 23\njason:\n  age: 35\nemily:\n  sex: female\n  age: 32\n"
    
    {{.modified_yml}}
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
