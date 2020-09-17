---
title: "c0061_vvvv"
date: 2020-09-18T01:27:30+99:00
draft: false
weight: 10613

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0061
                 Verbose -> vvvv
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
                 Timeout -> 3600000
     MaxModuelCallLayers -> 256
               EntryTask -> task
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0061
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    {
      "student_name": "tom",
      "classes": {
        "1k",
        "2b",
        "3j",
        "4s"
      }
    }
    
    -------runtime global final merged with dvars-------
    
    {
      "student_name": "tom",
      "classes": {
        "1k",
        "2b",
        "3j",
        "4s"
      }
    }
    
    loading [flow ref]:  ./tests/functests/c0061-task-main.yml
    loading [flow ref]:  ./tests/functests/c0061-task-complicate.yml
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "student_name": "tom",
      "classes": {
        "1k",
        "2b",
        "3j",
        "4s"
      },
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "student_name": "tom",
      "classes": {
        "1k",
        "2b",
        "3j",
        "4s"
      },
      "up_runtime_task_layer_number": 0
    })
    
    cmd( 1):
    echo "task step 1"
    
    cmd=>:
    echo "task step 1"
    -
    task step 1
    
    -
     .. ok
    cmd( 2):
    echo "task step 2"
    
    cmd=>:
    echo "task step 2"
    -
    task step 2
    
    -
     .. ok
    . ok
    -Step2:
    current exec runtime vars:
    (*core.Cache)({
      "student_name": "tom",
      "classes": {
        "1k",
        "2b",
        "3j",
        "4s"
      },
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"task step 2\"",
        Code: 0,
        Output: "task step 2",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "student_name": "tom",
      "classes": {
        "1k",
        "2b",
        "3j",
        "4s"
      },
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"task step 2\"",
        Code: 0,
        Output: "task step 2",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0
    })
    
      located task-> 3 [task_a]: 
    =Task3: [task ==> task_a:  ]
    Executing task stack layer: 2
    
    --Step1:
    current exec runtime vars:
    (*core.Cache)({
      "student_name": "tom",
      "classes": {
        "1k",
        "2b",
        "3j",
        "4s"
      },
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"task step 2\"",
        Code: 0,
        Output: "task step 2",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "student_name": "tom",
      "classes": {
        "1k",
        "2b",
        "3j",
        "4s"
      },
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"task step 2\"",
        Code: 0,
        Output: "task step 2",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1
    })
    
    cmd( 1):
    echo "task_a_step1"
    
    cmd=>:
    echo "task_a_step1"
    -
    task_a_step1
    
    -
     .. ok
    . ok
      located task-> 4 [task_c]: 
    =Task4: [task ==> task_c:  ]
    Executing task stack layer: 2
    
    --Step1:
    current exec runtime vars:
    (*core.Cache)({
      "student_name": "tom",
      "classes": {
        "1k",
        "2b",
        "3j",
        "4s"
      },
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"task_a_step1\"",
        Code: 0,
        Output: "task_a_step1",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "student_name": "tom",
      "classes": {
        "1k",
        "2b",
        "3j",
        "4s"
      },
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"task_a_step1\"",
        Code: 0,
        Output: "task_a_step1",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1
    })
    
    cmd( 1):
    echo "task_c_step1"
    
    cmd=>:
    echo "task_c_step1"
    -
    task_c_step1
    
    -
     .. ok
    . ok
      located task-> 3 [task_a]: 
    =Task3: [task ==> task_a:  ]
    Executing task stack layer: 2
    
    --Step1:
    current exec runtime vars:
    (*core.Cache)({
      "student_name": "tom",
      "classes": {
        "1k",
        "2b",
        "3j",
        "4s"
      },
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"task_c_step1\"",
        Code: 0,
        Output: "task_c_step1",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "student_name": "tom",
      "classes": {
        "1k",
        "2b",
        "3j",
        "4s"
      },
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"task_c_step1\"",
        Code: 0,
        Output: "task_c_step1",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1
    })
    
    cmd( 1):
    echo "task_a_step1"
    
    cmd=>:
    echo "task_a_step1"
    -
    task_a_step1
    
    -
     .. ok
    . ok
    -Step3:
    current exec runtime vars:
    (*core.Cache)({
      "student_name": "tom",
      "classes": {
        "1k",
        "2b",
        "3j",
        "4s"
      },
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"task step 2\"",
        Code: 0,
        Output: "task step 2",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "student_name": "tom",
      "classes": {
        "1k",
        "2b",
        "3j",
        "4s"
      },
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"task step 2\"",
        Code: 0,
        Output: "task step 2",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1
    })
    
      located task-> 5 [task_b]: 
    =Task5: [task ==> task_b:  ]
    Executing task stack layer: 2
    
    --Step1:
    current exec runtime vars:
    (*core.Cache)({
      "classes": {
        "1k",
        "2b",
        "3j",
        "4s"
      },
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"task step 2\"",
        Code: 0,
        Output: "task step 2",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1,
      "loopitem": "1k",
      "loopindex": 0,
      "loopindex1": 1,
      "student_name": "tom"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "student_name": "tom",
      "classes": {
        "1k",
        "2b",
        "3j",
        "4s"
      },
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"task step 2\"",
        Code: 0,
        Output: "task step 2",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1,
      "loopitem": "1k",
      "loopindex": 0,
      "loopindex1": 1
    })
    
    cmd( 1):
    echo "task_b_step1"
    
    cmd=>:
    echo "task_b_step1"
    -
    task_b_step1
    
    -
     .. ok
    cmd( 2):
    echo "{{.loopindex}} -> student nameed {{.student_name}} has been in class [{{.loopitem}}]"
    
    cmd=>:
    echo "0 -> student nameed tom has been in class [1k]"
    -
    0 -> student nameed tom has been in class [1k]
    
    -
     .. ok
    . ok
      located task-> 5 [task_b]: 
    =Task5: [task ==> task_b:  ]
    Executing task stack layer: 2
    
    --Step1:
    current exec runtime vars:
    (*core.Cache)({
      "loopitem": "2b",
      "loopindex": 1,
      "loopindex1": 2,
      "student_name": "tom",
      "classes": {
        "1k",
        "2b",
        "3j",
        "4s"
      },
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"0 -> student nameed tom has been in class [1k]\"",
        Code: 0,
        Output: "0 -> student nameed tom has been in class [1k]",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex1": 2,
      "student_name": "tom",
      "classes": {
        "1k",
        "2b",
        "3j",
        "4s"
      },
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"0 -> student nameed tom has been in class [1k]\"",
        Code: 0,
        Output: "0 -> student nameed tom has been in class [1k]",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1,
      "loopitem": "2b",
      "loopindex": 1
    })
    
    cmd( 1):
    echo "task_b_step1"
    
    cmd=>:
    echo "task_b_step1"
    -
    task_b_step1
    
    -
     .. ok
    cmd( 2):
    echo "{{.loopindex}} -> student nameed {{.student_name}} has been in class [{{.loopitem}}]"
    
    cmd=>:
    echo "1 -> student nameed tom has been in class [2b]"
    -
    1 -> student nameed tom has been in class [2b]
    
    -
     .. ok
    . ok
      located task-> 5 [task_b]: 
    =Task5: [task ==> task_b:  ]
    Executing task stack layer: 2
    
    --Step1:
    current exec runtime vars:
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"1 -> student nameed tom has been in class [2b]\"",
        Code: 0,
        Output: "1 -> student nameed tom has been in class [2b]",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1,
      "loopitem": "3j",
      "loopindex": 2,
      "loopindex1": 3,
      "student_name": "tom",
      "classes": {
        "1k",
        "2b",
        "3j",
        "4s"
      }
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopindex": 2,
      "loopindex1": 3,
      "student_name": "tom",
      "classes": {
        "1k",
        "2b",
        "3j",
        "4s"
      },
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"1 -> student nameed tom has been in class [2b]\"",
        Code: 0,
        Output: "1 -> student nameed tom has been in class [2b]",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1,
      "loopitem": "3j"
    })
    
    cmd( 1):
    echo "task_b_step1"
    
    cmd=>:
    echo "task_b_step1"
    -
    task_b_step1
    
    -
     .. ok
    cmd( 2):
    echo "{{.loopindex}} -> student nameed {{.student_name}} has been in class [{{.loopitem}}]"
    
    cmd=>:
    echo "2 -> student nameed tom has been in class [3j]"
    -
    2 -> student nameed tom has been in class [3j]
    
    -
     .. ok
    . ok
      located task-> 5 [task_b]: 
    =Task5: [task ==> task_b:  ]
    Executing task stack layer: 2
    
    --Step1:
    current exec runtime vars:
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"2 -> student nameed tom has been in class [3j]\"",
        Code: 0,
        Output: "2 -> student nameed tom has been in class [3j]",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1,
      "loopitem": "4s",
      "loopindex": 3,
      "loopindex1": 4,
      "student_name": "tom",
      "classes": {
        "1k",
        "2b",
        "3j",
        "4s"
      }
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "loopitem": "4s",
      "loopindex": 3,
      "loopindex1": 4,
      "student_name": "tom",
      "classes": {
        "1k",
        "2b",
        "3j",
        "4s"
      },
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"2 -> student nameed tom has been in class [3j]\"",
        Code: 0,
        Output: "2 -> student nameed tom has been in class [3j]",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1
    })
    
    cmd( 1):
    echo "task_b_step1"
    
    cmd=>:
    echo "task_b_step1"
    -
    task_b_step1
    
    -
     .. ok
    cmd( 2):
    echo "{{.loopindex}} -> student nameed {{.student_name}} has been in class [{{.loopitem}}]"
    
    cmd=>:
    echo "3 -> student nameed tom has been in class [4s]"
    -
    3 -> student nameed tom has been in class [4s]
    
    -
     .. ok
    . ok
    -Step4:
    current exec runtime vars:
    (*core.Cache)({
      "classes": {
        "1k",
        "2b",
        "3j",
        "4s"
      },
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"task step 2\"",
        Code: 0,
        Output: "task step 2",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1,
      "student_name": "tom"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "student_name": "tom",
      "classes": {
        "1k",
        "2b",
        "3j",
        "4s"
      },
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"task step 2\"",
        Code: 0,
        Output: "task step 2",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1
    })
    
    cmd( 1):
    echo "task step 3"
    
    cmd=>:
    echo "task step 3"
    -
    task step 3
    
    -
     .. ok
    cmd( 2):
    echo "task step 4"
    
    cmd=>:
    echo "task step 4"
    -
    task step 4
    
    -
     .. ok
    . ok
    -Step5:
    current exec runtime vars:
    (*core.Cache)({
      "classes": {
        "1k",
        "2b",
        "3j",
        "4s"
      },
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"task step 4\"",
        Code: 0,
        Output: "task step 4",
        ErrMsg: ""
      }),
      "student_name": "tom",
      "up_runtime_task_layer_number": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "classes": {
        "1k",
        "2b",
        "3j",
        "4s"
      },
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"task step 4\"",
        Code: 0,
        Output: "task step 4",
        ErrMsg: ""
      }),
      "student_name": "tom",
      "up_runtime_task_layer_number": 1
    })
    
      located task-> 2 [a_very_complicated_task]: 
    =Task2: [task ==> a_very_complicated_task: a_very_complicated_task ]
    Executing task stack layer: 2
    
    --Step1:
    current exec runtime vars:
    (*core.Cache)({
      "classes": {
        "1k",
        "2b",
        "3j",
        "4s"
      },
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"task step 4\"",
        Code: 0,
        Output: "task step 4",
        ErrMsg: ""
      }),
      "student_name": "tom",
      "up_runtime_task_layer_number": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "classes": {
        "1k",
        "2b",
        "3j",
        "4s"
      },
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"task step 4\"",
        Code: 0,
        Output: "task step 4",
        ErrMsg: ""
      }),
      "student_name": "tom",
      "up_runtime_task_layer_number": 1
    })
    
    cmd( 1):
    echo "i am a very complicated flow of step1"
    
    cmd=>:
    echo "i am a very complicated flow of step1"
    -
    i am a very complicated flow of step1
    
    -
     .. ok
    cmd( 2):
    echo "i am a very complicated flow of step2"
    
    cmd=>:
    echo "i am a very complicated flow of step2"
    -
    i am a very complicated flow of step2
    
    -
     .. ok
    cmd( 3):
    echo "i am a very complicated flow of step3"
    
    cmd=>:
    echo "i am a very complicated flow of step3"
    -
    i am a very complicated flow of step3
    
    -
     .. ok
    . ok
    --Step2:
    current exec runtime vars:
    (*core.Cache)({
      "classes": {
        "1k",
        "2b",
        "3j",
        "4s"
      },
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"i am a very complicated flow of step3\"",
        Code: 0,
        Output: "i am a very complicated flow of step3",
        ErrMsg: ""
      }),
      "student_name": "tom",
      "up_runtime_task_layer_number": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "classes": {
        "1k",
        "2b",
        "3j",
        "4s"
      },
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"i am a very complicated flow of step3\"",
        Code: 0,
        Output: "i am a very complicated flow of step3",
        ErrMsg: ""
      }),
      "student_name": "tom",
      "up_runtime_task_layer_number": 1
    })
    
    cmd( 1):
    echo "i am a very complicated flow of step4"
    
    cmd=>:
    echo "i am a very complicated flow of step4"
    -
    i am a very complicated flow of step4
    
    -
     .. ok
    cmd( 2):
    echo "{{.student_name}}"
    
    cmd=>:
    echo "tom"
    -
    tom
    
    -
     .. ok
    . ok
    
```

##### Logs with different verbose level
* [c0061 log - verbose level v](../../logs/c0061_v)
* [c0061 log - verbose level vv](../../logs/c0061_vv)
* [c0061 log - verbose level vvv](../../logs/c0061_vvv)
* [c0061 log - verbose level vvvv](../../logs/c0061_vvvv)
* [c0061 log - verbose level vvvvv](../../logs/c0061_vvvvv)

##### References
* [Related Chapter](../../organization/c0061)
