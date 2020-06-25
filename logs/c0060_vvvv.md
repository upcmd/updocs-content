---
title: "c0060_vvvv"
date: 2020-06-25T01:55:46+66:00
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
              ModuleName -> happy_newton8
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0060
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [happy_newton8] instance id: [dev]
    merged[ dev ] runtime vars:
    {
      "classes": {
        "1k",
        "2b",
        "3j",
        "4s"
      },
      "student_name": "tom"
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
    
    loading [flow ref]:  ./tests/functests/c0060-task-ref.yml
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    {
      Name: "",
      Do: {
        "echo \"task step 1\"",
        "echo \"task step 2\""
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
      "student_name": "tom",
      "classes": {
        "1k",
        "2b",
        "3j",
        "4s"
      }
    })
    
    happy_newton8: overall final exec vars:
    
    (*core.Cache)({
      "classes": {
        "1k",
        "2b",
        "3j",
        "4s"
      },
      "student_name": "tom"
    })
    
    cmd( 1):
    echo "task step 1"
    
     \_ echo "task step 1"
    task step 1
     .. ok
    cmd( 2):
    echo "task step 2"
    
     \_ echo "task step 2"
    task step 2
     .. ok
    . ok
    -Step2:
    {
      Name: "",
      Do: {
        "task_a",
        "task_c",
        "task_a"
      },
      Dox: <nil>,
      Func: "call",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "",
      Reg: "",
      Flags: <nil>,
      If: "{{eq .student_name \"tom\"}}",
      Else: <nil>,
      Loop: <nil>,
      Until: "",
      RefDir: "",
      VarsFile: ""
    }
    
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
        Code: 0,
        Output: "task step 2",
        ErrMsg: ""
      })
    })
    
    happy_newton8: overall final exec vars:
    
    (*core.Cache)({
      "classes": {
        "1k",
        "2b",
        "3j",
        "4s"
      },
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "task step 2",
        ErrMsg: ""
      }),
      "student_name": "tom"
    })
    
      located task-> 2 [task_a]: 
    =Task2: [task ==> task_a:  ]
    Executing task stack layer: 2
    
    --Step1:
    {
      Name: "",
      Do: {
        "echo \"task_a_step1\""
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
      "classes": {
        "1k",
        "2b",
        "3j",
        "4s"
      },
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "task step 2",
        ErrMsg: ""
      }),
      "student_name": "tom",
      "up_runtime_task_layer_number": 1
    })
    
    happy_newton8: overall final exec vars:
    
    (*core.Cache)({
      "classes": {
        "1k",
        "2b",
        "3j",
        "4s"
      },
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "task step 2",
        ErrMsg: ""
      }),
      "student_name": "tom",
      "up_runtime_task_layer_number": 1
    })
    
    cmd( 1):
    echo "task_a_step1"
    
     \_ echo "task_a_step1"
    task_a_step1
     .. ok
    . ok
      located task-> 3 [task_c]: 
    =Task3: [task ==> task_c:  ]
    Executing task stack layer: 2
    
    --Step1:
    {
      Name: "",
      Do: {
        "echo \"task_c_step1\""
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
      "student_name": "tom",
      "classes": {
        "1k",
        "2b",
        "3j",
        "4s"
      },
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "task_a_step1",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1
    })
    
    happy_newton8: overall final exec vars:
    
    (*core.Cache)({
      "classes": {
        "1k",
        "2b",
        "3j",
        "4s"
      },
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "task_a_step1",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1,
      "student_name": "tom"
    })
    
    cmd( 1):
    echo "task_c_step1"
    
     \_ echo "task_c_step1"
    task_c_step1
     .. ok
    . ok
      located task-> 2 [task_a]: 
    =Task2: [task ==> task_a:  ]
    Executing task stack layer: 2
    
    --Step1:
    {
      Name: "",
      Do: {
        "echo \"task_a_step1\""
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
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "task_c_step1",
        ErrMsg: ""
      }),
      "student_name": "tom",
      "up_runtime_task_layer_number": 1,
      "classes": {
        "1k",
        "2b",
        "3j",
        "4s"
      }
    })
    
    happy_newton8: overall final exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "classes": {
        "1k",
        "2b",
        "3j",
        "4s"
      },
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "task_c_step1",
        ErrMsg: ""
      }),
      "student_name": "tom"
    })
    
    cmd( 1):
    echo "task_a_step1"
    
     \_ echo "task_a_step1"
    task_a_step1
     .. ok
    . ok
    -Step3:
    {
      Name: "",
      Do: {
        "task_b"
      },
      Dox: <nil>,
      Func: "call",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "",
      Reg: "",
      Flags: <nil>,
      If: "{{eq .student_name \"tom\"}}",
      Else: <nil>,
      Loop: "classes",
      Until: "",
      RefDir: "",
      VarsFile: ""
    }
    
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
        Code: 0,
        Output: "task step 2",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1
    })
    
    happy_newton8: overall final exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "task step 2",
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
    
      located task-> 4 [task_b]: 
    =Task4: [task ==> task_b:  ]
    Executing task stack layer: 2
    
    --Step1:
    {
      Name: "",
      Do: {
        "echo \"task_b_step1\"",
        "echo \"{{.loopindex}} -> student nameed {{.student_name}} has been in class [{{.loopitem}}]\""
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
      "loopindex1": 1,
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "task step 2",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1,
      "student_name": "tom",
      "classes": {
        "1k",
        "2b",
        "3j",
        "4s"
      },
      "loopitem": "1k",
      "loopindex": 0
    })
    
    happy_newton8: overall final exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
      "student_name": "tom",
      "classes": {
        "1k",
        "2b",
        "3j",
        "4s"
      },
      "loopitem": "1k",
      "loopindex": 0,
      "loopindex1": 1,
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "task step 2",
        ErrMsg: ""
      })
    })
    
    cmd( 1):
    echo "task_b_step1"
    
     \_ echo "task_b_step1"
    task_b_step1
     .. ok
    cmd( 2):
    echo "{{.loopindex}} -> student nameed {{.student_name}} has been in class [{{.loopitem}}]"
    
     \_ echo "0 -> student nameed tom has been in class [1k]"
    0 -> student nameed tom has been in class [1k]
     .. ok
    . ok
      located task-> 4 [task_b]: 
    =Task4: [task ==> task_b:  ]
    Executing task stack layer: 2
    
    --Step1:
    {
      Name: "",
      Do: {
        "echo \"task_b_step1\"",
        "echo \"{{.loopindex}} -> student nameed {{.student_name}} has been in class [{{.loopitem}}]\""
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
      "classes": {
        "1k",
        "2b",
        "3j",
        "4s"
      },
      "loopitem": "2b",
      "loopindex": 1,
      "loopindex1": 2,
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "0 -> student nameed tom has been in class [1k]",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1,
      "student_name": "tom"
    })
    
    happy_newton8: overall final exec vars:
    
    (*core.Cache)({
      "loopitem": "2b",
      "loopindex": 1,
      "loopindex1": 2,
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "0 -> student nameed tom has been in class [1k]",
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
    
    cmd( 1):
    echo "task_b_step1"
    
     \_ echo "task_b_step1"
    task_b_step1
     .. ok
    cmd( 2):
    echo "{{.loopindex}} -> student nameed {{.student_name}} has been in class [{{.loopitem}}]"
    
     \_ echo "1 -> student nameed tom has been in class [2b]"
    1 -> student nameed tom has been in class [2b]
     .. ok
    . ok
      located task-> 4 [task_b]: 
    =Task4: [task ==> task_b:  ]
    Executing task stack layer: 2
    
    --Step1:
    {
      Name: "",
      Do: {
        "echo \"task_b_step1\"",
        "echo \"{{.loopindex}} -> student nameed {{.student_name}} has been in class [{{.loopitem}}]\""
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
      "loopindex1": 3,
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "1 -> student nameed tom has been in class [2b]",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1,
      "student_name": "tom",
      "classes": {
        "1k",
        "2b",
        "3j",
        "4s"
      },
      "loopitem": "3j",
      "loopindex": 2
    })
    
    happy_newton8: overall final exec vars:
    
    (*core.Cache)({
      "classes": {
        "1k",
        "2b",
        "3j",
        "4s"
      },
      "loopitem": "3j",
      "loopindex": 2,
      "loopindex1": 3,
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "1 -> student nameed tom has been in class [2b]",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1,
      "student_name": "tom"
    })
    
    cmd( 1):
    echo "task_b_step1"
    
     \_ echo "task_b_step1"
    task_b_step1
     .. ok
    cmd( 2):
    echo "{{.loopindex}} -> student nameed {{.student_name}} has been in class [{{.loopitem}}]"
    
     \_ echo "2 -> student nameed tom has been in class [3j]"
    2 -> student nameed tom has been in class [3j]
     .. ok
    . ok
      located task-> 4 [task_b]: 
    =Task4: [task ==> task_b:  ]
    Executing task stack layer: 2
    
    --Step1:
    {
      Name: "",
      Do: {
        "echo \"task_b_step1\"",
        "echo \"{{.loopindex}} -> student nameed {{.student_name}} has been in class [{{.loopitem}}]\""
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
      "loopitem": "4s",
      "loopindex": 3,
      "loopindex1": 4,
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "2 -> student nameed tom has been in class [3j]",
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
    
    happy_newton8: overall final exec vars:
    
    (*core.Cache)({
      "student_name": "tom",
      "classes": {
        "1k",
        "2b",
        "3j",
        "4s"
      },
      "loopitem": "4s",
      "loopindex": 3,
      "loopindex1": 4,
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "2 -> student nameed tom has been in class [3j]",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1
    })
    
    cmd( 1):
    echo "task_b_step1"
    
     \_ echo "task_b_step1"
    task_b_step1
     .. ok
    cmd( 2):
    echo "{{.loopindex}} -> student nameed {{.student_name}} has been in class [{{.loopitem}}]"
    
     \_ echo "3 -> student nameed tom has been in class [4s]"
    3 -> student nameed tom has been in class [4s]
     .. ok
    . ok
    -Step4:
    {
      Name: "",
      Do: {
        "echo \"task step 3\"",
        "echo \"task step 4\""
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
      "student_name": "tom",
      "classes": {
        "1k",
        "2b",
        "3j",
        "4s"
      },
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "task step 2",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1
    })
    
    happy_newton8: overall final exec vars:
    
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
        Code: 0,
        Output: "task step 2",
        ErrMsg: ""
      })
    })
    
    cmd( 1):
    echo "task step 3"
    
     \_ echo "task step 3"
    task step 3
     .. ok
    cmd( 2):
    echo "task step 4"
    
     \_ echo "task step 4"
    task step 4
     .. ok
    . ok
    -Step5:
    {
      Name: "",
      Do: {
        "a_very_complicated_task"
      },
      Dox: <nil>,
      Func: "call",
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
      "student_name": "tom",
      "classes": {
        "1k",
        "2b",
        "3j",
        "4s"
      },
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "task step 4",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1
    })
    
    happy_newton8: overall final exec vars:
    
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
        Code: 0,
        Output: "task step 4",
        ErrMsg: ""
      })
    })
    
      located task-> 5 [a_very_complicated_task]: 
    =Task5: [task ==> a_very_complicated_task: a_very_complicated_task ]
    Executing task stack layer: 2
    
    --Step1:
    {
      Name: "",
      Do: {
        "echo \"i am a very complicated flow of step1\"",
        "echo \"i am a very complicated flow of step2\"",
        "echo \"i am a very complicated flow of step3\""
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
      "classes": {
        "1k",
        "2b",
        "3j",
        "4s"
      },
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "task step 4",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1,
      "student_name": "tom"
    })
    
    happy_newton8: overall final exec vars:
    
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
        Code: 0,
        Output: "task step 4",
        ErrMsg: ""
      })
    })
    
    cmd( 1):
    echo "i am a very complicated flow of step1"
    
     \_ echo "i am a very complicated flow of step1"
    i am a very complicated flow of step1
     .. ok
    cmd( 2):
    echo "i am a very complicated flow of step2"
    
     \_ echo "i am a very complicated flow of step2"
    i am a very complicated flow of step2
     .. ok
    cmd( 3):
    echo "i am a very complicated flow of step3"
    
     \_ echo "i am a very complicated flow of step3"
    i am a very complicated flow of step3
     .. ok
    . ok
    --Step2:
    {
      Name: "",
      Do: {
        "echo \"i am a very complicated flow of step4\"",
        "echo \"{{.student_name}}\""
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
      "up_runtime_task_layer_number": 1,
      "student_name": "tom",
      "classes": {
        "1k",
        "2b",
        "3j",
        "4s"
      },
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "i am a very complicated flow of step3",
        ErrMsg: ""
      })
    })
    
    happy_newton8: overall final exec vars:
    
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
        Code: 0,
        Output: "i am a very complicated flow of step3",
        ErrMsg: ""
      })
    })
    
    cmd( 1):
    echo "i am a very complicated flow of step4"
    
     \_ echo "i am a very complicated flow of step4"
    i am a very complicated flow of step4
     .. ok
    cmd( 2):
    echo "{{.student_name}}"
    
     \_ echo "tom"
    tom
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