---
title: "c0060_vvvv"
date: 2020-10-07T00:11:10+1010:00
draft: false
weight: 10603

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0060
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
    loading [Task]:  ./tests/functests/c0060
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
      "classes": {
        "1k",
        "2b",
        "3j",
        "4s"
      },
      "student_name": "tom"
    })
    
    -------runtime global final merged with dvars-------
    
    (*core.Cache)({
      "student_name": "tom",
      "classes": {
        "1k",
        "2b",
        "3j",
        "4s"
      }
    })
    
    loading [flow ref]:  ./tests/functests/c0060-task-ref.yml
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
      "up_runtime_task_layer_number": 0,
      "student_name": "tom",
      "classes": {
        "1k",
        "2b",
        "3j",
        "4s"
      }
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
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"task step 2\"",
        Code: 0,
        Output: "task step 2",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0,
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
    
      located task-> 2 [task_a]: 
    =Task2: [task ==> task_a:  ]
    Executing task stack layer: 2
    
    --Step1:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
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
      })
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
      located task-> 3 [task_c]: 
    =Task3: [task ==> task_c:  ]
    Executing task stack layer: 2
    
    --Step1:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
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
      })
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
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
      })
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
      located task-> 2 [task_a]: 
    =Task2: [task ==> task_a:  ]
    Executing task stack layer: 2
    
    --Step1:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
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
      })
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
      "student_name": "tom",
      "up_runtime_task_layer_number": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "student_name": "tom",
      "up_runtime_task_layer_number": 1,
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
      })
    })
    
      located task-> 4 [task_b]: 
    =Task4: [task ==> task_b:  ]
    Executing task stack layer: 2
    
    --Step1:
    current exec runtime vars:
    (*core.Cache)({
      "loopindex": 0,
      "loopindex1": 1,
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
      "student_name": "tom",
      "up_runtime_task_layer_number": 1,
      "loopitem": "1k"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"task step 2\"",
        Code: 0,
        Output: "task step 2",
        ErrMsg: ""
      }),
      "student_name": "tom",
      "up_runtime_task_layer_number": 1,
      "loopitem": "1k",
      "loopindex": 0,
      "loopindex1": 1,
      "classes": {
        "1k",
        "2b",
        "3j",
        "4s"
      }
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
      located task-> 4 [task_b]: 
    =Task4: [task ==> task_b:  ]
    Executing task stack layer: 2
    
    --Step1:
    current exec runtime vars:
    (*core.Cache)({
      "loopitem": "2b",
      "loopindex": 1,
      "loopindex1": 2,
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
        Cmd: "echo \"0 -> student nameed tom has been in class [1k]\"",
        Code: 0,
        Output: "0 -> student nameed tom has been in class [1k]",
        ErrMsg: ""
      }),
      "student_name": "tom",
      "up_runtime_task_layer_number": 1,
      "loopitem": "2b",
      "loopindex": 1,
      "loopindex1": 2
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
      located task-> 4 [task_b]: 
    =Task4: [task ==> task_b:  ]
    Executing task stack layer: 2
    
    --Step1:
    current exec runtime vars:
    (*core.Cache)({
      "loopitem": "3j",
      "loopindex": 2,
      "loopindex1": 3,
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
      "student_name": "tom",
      "up_runtime_task_layer_number": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"1 -> student nameed tom has been in class [2b]\"",
        Code: 0,
        Output: "1 -> student nameed tom has been in class [2b]",
        ErrMsg: ""
      }),
      "student_name": "tom",
      "up_runtime_task_layer_number": 1,
      "loopitem": "3j",
      "loopindex": 2,
      "loopindex1": 3,
      "classes": {
        "1k",
        "2b",
        "3j",
        "4s"
      }
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
      located task-> 4 [task_b]: 
    =Task4: [task ==> task_b:  ]
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
        Cmd: "echo \"2 -> student nameed tom has been in class [3j]\"",
        Code: 0,
        Output: "2 -> student nameed tom has been in class [3j]",
        ErrMsg: ""
      }),
      "student_name": "tom",
      "up_runtime_task_layer_number": 1,
      "loopitem": "4s",
      "loopindex": 3,
      "loopindex1": 4
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "loopitem": "4s",
      "loopindex": 3,
      "loopindex1": 4,
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
      "student_name": "tom"
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
      "student_name": "tom",
      "up_runtime_task_layer_number": 1,
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
      })
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "student_name": "tom",
      "up_runtime_task_layer_number": 1,
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
      })
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
      "student_name": "tom",
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
      "up_runtime_task_layer_number": 1
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"task step 4\"",
        Code: 0,
        Output: "task step 4",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1,
      "student_name": "tom",
      "classes": {
        "1k",
        "2b",
        "3j",
        "4s"
      }
    })
    
      located task-> 5 [a_very_complicated_task]: 
    =Task5: [task ==> a_very_complicated_task: a_very_complicated_task ]
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
      "up_runtime_task_layer_number": 1,
      "student_name": "tom"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "student_name": "tom",
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
      })
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
      "student_name": "tom",
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
        Cmd: "echo \"i am a very complicated flow of step3\"",
        Code: 0,
        Output: "i am a very complicated flow of step3",
        ErrMsg: ""
      }),
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
* [c0060 log - verbose level v](../../logs/c0060_v)
* [c0060 log - verbose level vv](../../logs/c0060_vv)
* [c0060 log - verbose level vvv](../../logs/c0060_vvv)
* [c0060 log - verbose level vvvv](../../logs/c0060_vvvv)
* [c0060 log - verbose level vvvvv](../../logs/c0060_vvvvv)

##### References
* [Related Chapter](../../organization/c0060)
