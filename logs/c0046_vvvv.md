---
title: "c0046_vvvv"
date: 2020-08-09T01:36:05+88:00
draft: false
weight: 10463

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0046
                 Verbose -> vvvv
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
                 Timeout -> 3600000
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0046
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    ---------group vars----------
    
    global: {
      "student_age": "28",
      "student_name": "Tom Hanks"
    }
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    {
      "student_name": "Tom Hanks",
      "student_age": "28"
    }
    
    -------runtime global final merged with dvars-------
    
    {
      "student_name": "Tom Hanks",
      "student_age": "28",
      "cli": "echo \"\"\"\nstudent details:\nname: Tom Hanks\nage: 28\n\"\"\"\n"
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1: [: this show an example of the empty value is mapped to None ]
    current exec runtime vars:
    (*core.Cache)({
      "student_name": "Tom Hanks",
      "student_age": "28",
      "cli": "echo \"\"\"\nstudent details:\nname: Tom Hanks\nage: 28\n\"\"\"\n"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "cli": "echo \"\"\"\nstudent details:\nname: Tom Hanks\nage: 28\n\"\"\"\n",
      "someone": "None",
      "i_am_empty": "None",
      "empty_env_var": "None",
      "student_name": "Tom Hanks",
      "student_age": "28"
    })
    
    cmd( 1):
    echo "{{.someone}}"
    echo "{{.i_am_empty}}"
    echo "{{.empty_env_var}}"
    
    
    cmd=>:
    echo "None"
    echo "None"
    echo "None"
    <=
    None
    None
    None
     .. ok
    . ok
    -Step2:
    current exec runtime vars:
    (*core.Cache)({
      "cli": "echo \"\"\"\nstudent details:\nname: Tom Hanks\nage: 28\n\"\"\"\n",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"None\"\necho \"None\"\necho \"None\"\n",
        Code: 0,
        Output: "None\nNone\nNone",
        ErrMsg: ""
      }),
      "student_name": "Tom Hanks",
      "student_age": "28"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "cli": "echo \"\"\"\nstudent details:\nname: Tom Hanks\nage: 28\n\"\"\"\n",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"None\"\necho \"None\"\necho \"None\"\n",
        Code: 0,
        Output: "None\nNone\nNone",
        ErrMsg: ""
      }),
      "student_name": "Tom Hanks",
      "student_age": "28"
    })
    
    ~SubStep1: [inspect:  ]
     1: inspect[exec_vars]
    (*core.Cache)({
      "student_age": "28",
      "cli": "echo \"\"\"\nstudent details:\nname: Tom Hanks\nage: 28\n\"\"\"\n",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"None\"\necho \"None\"\necho \"None\"\n",
        Code: 0,
        Output: "None\nNone\nNone",
        ErrMsg: ""
      }),
      "student_name": "Tom Hanks"
    })
    
     2: inspect[exec_base_vars]
    {
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"None\"\necho \"None\"\necho \"None\"\n",
        Code: 0,
        Output: "None\nNone\nNone",
        ErrMsg: ""
      }),
      "student_name": "Tom Hanks",
      "student_age": "28",
      "cli": "echo \"\"\"\nstudent details:\nname: Tom Hanks\nage: 28\n\"\"\"\n"
    }
    
    
```

##### Logs with different verbose level
* [c0046 log - verbose level v](../../logs/c0046_v)
* [c0046 log - verbose level vv](../../logs/c0046_vv)
* [c0046 log - verbose level vvv](../../logs/c0046_vvv)
* [c0046 log - verbose level vvvv](../../logs/c0046_vvvv)
* [c0046 log - verbose level vvvvv](../../logs/c0046_vvvvv)

##### References
* [Related Chapter](../../env-vars/c0046)
