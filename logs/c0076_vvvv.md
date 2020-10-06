---
title: "c0076_vvvv"
date: 2020-10-07T00:11:13+1010:00
draft: false
weight: 10763

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0076
                 Verbose -> vvvv
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
                 Timeout -> 3600000
     MaxModuelCallLayers -> 256
               EntryTask -> task
      ModRepoUsernameRef -> 
      ModRepoPasswordRef -> 
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0076
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    ---------group vars----------
    
    global: (*core.Cache)({
    })
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    (*core.Cache)({
    })
    
    -------runtime global final merged with dvars-------
    
    (*core.Cache)({
    })
    
      located task-> 1 [task]: 
    Task1: [task ==> task: test the exit scenarios due to different types of validation ]
    Executing task stack layer: 1
    
    -Step1: [: step1 ]
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0
    })
    
    cmd( 1):
    echo hanks
    
    cmd=>:
    echo hanks
    -
    hanks
    
    -
     .. ok
    . ok
    -Step2: [
    test register a variable to global vars
    the reg_hello should be <no value> since this is a template action
    you should really use dvar name void instead
    ]
    current exec runtime vars:
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo hanks",
        Code: 0,
        Output: "hanks",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo hanks",
        Code: 0,
        Output: "hanks",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0,
      "hellomsg": "hanks",
      "reg_hello": "hanks\n\n"
    })
    
     WARN: [cmd] - [Not implemented or void for no action!]
    -Step3:
    current exec runtime vars:
    (*core.Cache)({
      "hellomsg": "hanks",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo hanks",
        Code: 0,
        Output: "hanks",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "hellomsg": "hanks",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo hanks",
        Code: 0,
        Output: "hanks",
        ErrMsg: ""
      })
    })
    
    cmd( 1):
    echo "{{.reg_hello}}"
    
    cmd=>:
    echo "<no value>"
    -
    <no value>
    
    -
     .. ok
    cmd( 2):
    echo "{{.hellomsg}}"
    
    cmd=>:
    echo "hanks"
    -
    hanks
    
    -
     .. ok
    . ok
    -Step4: [
    the reg_tom's value is a object, but since reg_tom is only a local, it
    will probably not very useful
    ]
    current exec runtime vars:
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hanks\"",
        Code: 0,
        Output: "hanks",
        ErrMsg: ""
      }),
      "hellomsg": "hanks",
      "up_runtime_task_layer_number": 0,
      "person": {
        "name": "tom",
        "age": 18
      }
    })
    
    dvar> local_tom:
    "my name is tom\nage: 18\nname: tom\n"
    
    -
    my name is tom
    age: 18
    name: tom
    
    self: final context exec vars:
    
    (*core.Cache)({
      "local_tom": "my name is tom\nage: 18\nname: tom\n",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hanks\"",
        Code: 0,
        Output: "hanks",
        ErrMsg: ""
      }),
      "hellomsg": "hanks",
      "up_runtime_task_layer_number": 0,
      "person": {
        "name": "tom",
        "age": 18
      },
      "tom": {
        "name": "tom",
        "age": 18
      }
    })
    
    ~SubStep1: [reg:  ]
    -Step5: [: debug the results ]
    current exec runtime vars:
    (*core.Cache)({
      "objname": "global_tom",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hanks\"",
        Code: 0,
        Output: "hanks",
        ErrMsg: ""
      }),
      "hellomsg": "hanks",
      "tom": {
        "name": "tom",
        "age": 18
      },
      "global_tom": "my name is tom\nage: 18\nname: tom\n",
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "hellomsg": "hanks",
      "tom": {
        "name": "tom",
        "age": 18
      },
      "global_tom": "my name is tom\nage: 18\nname: tom\n",
      "up_runtime_task_layer_number": 0,
      "objname": "global_tom",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"hanks\"",
        Code: 0,
        Output: "hanks",
        ErrMsg: ""
      })
    })
    
    ~SubStep1: [print: this local_tom should be <no value> as it is in scope of last step ]
    None
    ~SubStep2: [print: get the object from register global space ]
    map[age:18 name:tom]
    ~SubStep3: [printObj: dynamically reference to global_tom object registered ]
    (string) (len=12) "{{.objname}}"
    
    object:
     global_tom: "my name is tom\nage: 18\nname: tom\n"
    
    
```

##### Logs with different verbose level
* [c0076 log - verbose level v](../../logs/c0076_v)
* [c0076 log - verbose level vv](../../logs/c0076_vv)
* [c0076 log - verbose level vvv](../../logs/c0076_vvv)
* [c0076 log - verbose level vvvv](../../logs/c0076_vvvv)
* [c0076 log - verbose level vvvvv](../../logs/c0076_vvvvv)

##### References
* [Related Chapter](../../vars/c0076)
