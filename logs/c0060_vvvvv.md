---
title: "c0060_vvvvv"
date: 2020-10-07T00:11:10+1010:00
draft: false
weight: 10604

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
    loading [Task]:  ./tests/functests/c0060
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc000098b40)(<nil>)
    
    ---------group vars----------
    
    global: (*core.Cache)({
    })
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    (*core.Cache)({
      "student_name": "tom",
      "classes": {
        "1k",
        "2b",
        "3j",
        "4s"
      }
    })
    
    (*core.Cache)(0xc0000c8148)((len=2) {
     (string) (len=7) "classes": ([]interface {}) (len=4 cap=4) {
      (string) (len=2) "1k",
      (string) (len=2) "2b",
      (string) (len=2) "3j",
      (string) (len=2) "4s"
     },
     (string) (len=12) "student_name": (string) (len=3) "tom"
    })
    
    [runtime global] dvar expanded result:
    {
    }
    
    
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
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "classes": {
        "1k",
        "2b",
        "3j",
        "4s"
      },
      "up_runtime_task_layer_number": 0,
      "student_name": "tom"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "classes": {
        "1k",
        "2b",
        "3j",
        "4s"
      },
      "up_runtime_task_layer_number": 0,
      "student_name": "tom"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "classes": {
        "1k",
        "2b",
        "3j",
        "4s"
      },
      "up_runtime_task_layer_number": 0,
      "student_name": "tom"
    })
    
    cmd( 1):
    echo "task step 1"
    
    cmd=>:
    echo "task step 1"
    -
    task step 1
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=18) "echo \"task step 1\"",
     Code: (int) 0,
     Output: (string) (len=11) "task step 1",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo "task step 2"
    
    cmd=>:
    echo "task step 2"
    -
    task step 2
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=18) "echo \"task step 2\"",
     Code: (int) 0,
     Output: (string) (len=11) "task step 2",
     ErrMsg: (string) ""
    }
    
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
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
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
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
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
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
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
    
    caller's vars to task (task_a)::
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
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
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
        Cmd: "echo \"task step 2\"",
        Code: 0,
        Output: "task step 2",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
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
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"task step 2\"",
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
    
    cmd( 1):
    echo "task_a_step1"
    
    cmd=>:
    echo "task_a_step1"
    -
    task_a_step1
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=19) "echo \"task_a_step1\"",
     Code: (int) 0,
     Output: (string) (len=12) "task_a_step1",
     ErrMsg: (string) ""
    }
    
    . ok
    caller's vars to task (task_c)::
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
      "up_runtime_task_layer_number": 0
    })
    
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
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
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
        Cmd: "echo \"task_a_step1\"",
        Code: 0,
        Output: "task_a_step1",
        ErrMsg: ""
      })
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
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
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"task_a_step1\"",
        Code: 0,
        Output: "task_a_step1",
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
    echo "task_c_step1"
    
    cmd=>:
    echo "task_c_step1"
    -
    task_c_step1
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=19) "echo \"task_c_step1\"",
     Code: (int) 0,
     Output: (string) (len=12) "task_c_step1",
     ErrMsg: (string) ""
    }
    
    . ok
    caller's vars to task (task_a)::
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
      "up_runtime_task_layer_number": 0
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
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
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
        Cmd: "echo \"task_c_step1\"",
        Code: 0,
        Output: "task_c_step1",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
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
    }
    
    
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
        Cmd: "echo \"task_c_step1\"",
        Code: 0,
        Output: "task_c_step1",
        ErrMsg: ""
      })
    })
    
    cmd( 1):
    echo "task_a_step1"
    
    cmd=>:
    echo "task_a_step1"
    -
    task_a_step1
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=19) "echo \"task_a_step1\"",
     Code: (int) 0,
     Output: (string) (len=12) "task_a_step1",
     ErrMsg: (string) ""
    }
    
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
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
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
        Cmd: "echo \"task step 2\"",
        Code: 0,
        Output: "task step 2",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"task step 2\"",
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
    }
    
    
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
    
    caller's vars to task (task_b)::
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
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
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
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
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
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
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
    
    cmd=>:
    echo "task_b_step1"
    -
    task_b_step1
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=19) "echo \"task_b_step1\"",
     Code: (int) 0,
     Output: (string) (len=12) "task_b_step1",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo "{{.loopindex}} -> student nameed {{.student_name}} has been in class [{{.loopitem}}]"
    
    cmd=>:
    echo "0 -> student nameed tom has been in class [1k]"
    -
    0 -> student nameed tom has been in class [1k]
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=53) "echo \"0 -> student nameed tom has been in class [1k]\"",
     Code: (int) 0,
     Output: (string) (len=46) "0 -> student nameed tom has been in class [1k]",
     ErrMsg: (string) ""
    }
    
    . ok
    caller's vars to task (task_b)::
    (*core.Cache)({
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
      "loopindex": 1,
      "loopindex1": 2
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
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
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
        Cmd: "echo \"0 -> student nameed tom has been in class [1k]\"",
        Code: 0,
        Output: "0 -> student nameed tom has been in class [1k]",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1,
      "loopitem": "2b",
      "loopindex": 1,
      "loopindex1": 2
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
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
      "up_runtime_task_layer_number": 1,
      "loopitem": "2b"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "up_runtime_task_layer_number": 1,
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
      })
    })
    
    cmd( 1):
    echo "task_b_step1"
    
    cmd=>:
    echo "task_b_step1"
    -
    task_b_step1
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=19) "echo \"task_b_step1\"",
     Code: (int) 0,
     Output: (string) (len=12) "task_b_step1",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo "{{.loopindex}} -> student nameed {{.student_name}} has been in class [{{.loopitem}}]"
    
    cmd=>:
    echo "1 -> student nameed tom has been in class [2b]"
    -
    1 -> student nameed tom has been in class [2b]
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=53) "echo \"1 -> student nameed tom has been in class [2b]\"",
     Code: (int) 0,
     Output: (string) (len=46) "1 -> student nameed tom has been in class [2b]",
     ErrMsg: (string) ""
    }
    
    . ok
    caller's vars to task (task_b)::
    (*core.Cache)({
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
      "loopitem": "3j",
      "loopindex": 2
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
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
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
        Cmd: "echo \"1 -> student nameed tom has been in class [2b]\"",
        Code: 0,
        Output: "1 -> student nameed tom has been in class [2b]",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1,
      "loopitem": "3j",
      "loopindex": 2,
      "loopindex1": 3
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
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
    }
    
    
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
        Cmd: "echo \"1 -> student nameed tom has been in class [2b]\"",
        Code: 0,
        Output: "1 -> student nameed tom has been in class [2b]",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1,
      "loopitem": "3j",
      "loopindex": 2,
      "loopindex1": 3
    })
    
    cmd( 1):
    echo "task_b_step1"
    
    cmd=>:
    echo "task_b_step1"
    -
    task_b_step1
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=19) "echo \"task_b_step1\"",
     Code: (int) 0,
     Output: (string) (len=12) "task_b_step1",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo "{{.loopindex}} -> student nameed {{.student_name}} has been in class [{{.loopitem}}]"
    
    cmd=>:
    echo "2 -> student nameed tom has been in class [3j]"
    -
    2 -> student nameed tom has been in class [3j]
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=53) "echo \"2 -> student nameed tom has been in class [3j]\"",
     Code: (int) 0,
     Output: (string) (len=46) "2 -> student nameed tom has been in class [3j]",
     ErrMsg: (string) ""
    }
    
    . ok
    caller's vars to task (task_b)::
    (*core.Cache)({
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
      "up_runtime_task_layer_number": 1,
      "loopitem": "4s",
      "loopindex": 3
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
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
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
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
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
    }
    
    
    self: final context exec vars:
    
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
    
    cmd( 1):
    echo "task_b_step1"
    
    cmd=>:
    echo "task_b_step1"
    -
    task_b_step1
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=19) "echo \"task_b_step1\"",
     Code: (int) 0,
     Output: (string) (len=12) "task_b_step1",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo "{{.loopindex}} -> student nameed {{.student_name}} has been in class [{{.loopitem}}]"
    
    cmd=>:
    echo "3 -> student nameed tom has been in class [4s]"
    -
    3 -> student nameed tom has been in class [4s]
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=53) "echo \"3 -> student nameed tom has been in class [4s]\"",
     Code: (int) 0,
     Output: (string) (len=46) "3 -> student nameed tom has been in class [4s]",
     ErrMsg: (string) ""
    }
    
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
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
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
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
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
      }),
      "student_name": "tom"
    }
    
    
    self: final context exec vars:
    
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
    
    cmd( 1):
    echo "task step 3"
    
    cmd=>:
    echo "task step 3"
    -
    task step 3
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=18) "echo \"task step 3\"",
     Code: (int) 0,
     Output: (string) (len=11) "task step 3",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo "task step 4"
    
    cmd=>:
    echo "task step 4"
    -
    task step 4
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=18) "echo \"task step 4\"",
     Code: (int) 0,
     Output: (string) (len=11) "task step 4",
     ErrMsg: (string) ""
    }
    
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
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
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
        Cmd: "echo \"task step 4\"",
        Code: 0,
        Output: "task step 4",
        ErrMsg: ""
      })
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
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
    }
    
    
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
    
    caller's vars to task (a_very_complicated_task)::
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
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
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
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
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
    }
    
    
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
    
    cmd( 1):
    echo "i am a very complicated flow of step1"
    
    cmd=>:
    echo "i am a very complicated flow of step1"
    -
    i am a very complicated flow of step1
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=44) "echo \"i am a very complicated flow of step1\"",
     Code: (int) 0,
     Output: (string) (len=37) "i am a very complicated flow of step1",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo "i am a very complicated flow of step2"
    
    cmd=>:
    echo "i am a very complicated flow of step2"
    -
    i am a very complicated flow of step2
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=44) "echo \"i am a very complicated flow of step2\"",
     Code: (int) 0,
     Output: (string) (len=37) "i am a very complicated flow of step2",
     ErrMsg: (string) ""
    }
    
    cmd( 3):
    echo "i am a very complicated flow of step3"
    
    cmd=>:
    echo "i am a very complicated flow of step3"
    -
    i am a very complicated flow of step3
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=44) "echo \"i am a very complicated flow of step3\"",
     Code: (int) 0,
     Output: (string) (len=37) "i am a very complicated flow of step3",
     ErrMsg: (string) ""
    }
    
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
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
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
        Cmd: "echo \"i am a very complicated flow of step3\"",
        Code: 0,
        Output: "i am a very complicated flow of step3",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 1
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
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
    }
    
    
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
    (utils.ExecResult) {
     Cmd: (string) (len=44) "echo \"i am a very complicated flow of step4\"",
     Code: (int) 0,
     Output: (string) (len=37) "i am a very complicated flow of step4",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo "{{.student_name}}"
    
    cmd=>:
    echo "tom"
    -
    tom
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=10) "echo \"tom\"",
     Code: (int) 0,
     Output: (string) (len=3) "tom",
     ErrMsg: (string) ""
    }
    
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
