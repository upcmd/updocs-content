---
title: "c0046_vvvvv"
date: 2020-10-07T00:11:08+1010:00
draft: false
weight: 10464

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
    loading [Task]:  ./tests/functests/c0046
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001bf4a0)((len=1 cap=1) {
     (impl.Scope) {
      Name: (string) (len=6) "global",
      Ref: (string) "",
      RefDir: (string) "",
      Members: ([]string) <nil>,
      Vars: (core.Cache) <nil>,
      Dvars: (impl.Dvars) (len=2 cap=2) {
       (impl.Dvar) {
        Name: (string) (len=12) "student_name",
        Value: (string) (len=45) "{{ env \"STUDENT_NAME\" |default \"Tom Hanks\" }}",
        Desc: (string) "",
        Expand: (int) 0,
        Flags: ([]string) <nil>,
        Rendered: (string) "",
        Secure: (*utils.SecureSetting)(<nil>),
        Ref: (string) "",
        RefDir: (string) "",
        DataKey: (string) "",
        DataPath: (string) "",
        DataTemplate: (string) ""
       },
       (impl.Dvar) {
        Name: (string) (len=11) "student_age",
        Value: (string) (len=35) "{{ env \"STUDENT_AGE\" |default 28 }}",
        Desc: (string) "",
        Expand: (int) 0,
        Flags: ([]string) <nil>,
        Rendered: (string) "",
        Secure: (*utils.SecureSetting)(<nil>),
        Ref: (string) "",
        RefDir: (string) "",
        DataKey: (string) "",
        DataPath: (string) "",
        DataTemplate: (string) ""
       }
      }
     }
    })
    
    [global] dvar expanded result:
    {
      "student_name": "Tom Hanks",
      "student_age": "28"
    }
    
    
    scope[global] merged: {
      "student_name": "Tom Hanks",
      "student_age": "28"
    }
    
    
    ---------group vars----------
    
    global: (*core.Cache)({
      "student_age": "28",
      "student_name": "Tom Hanks"
    })
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    (*core.Cache)({
      "student_name": "Tom Hanks",
      "student_age": "28"
    })
    
    (*core.Cache)(0xc00000e980)((len=2) {
     (string) (len=12) "student_name": (string) (len=9) "Tom Hanks",
     (string) (len=11) "student_age": (string) (len=2) "28"
    })
    
    [runtime global] dvar expanded result:
    {
      "cli": "echo \"\"\"\nstudent details:\nname: Tom Hanks\nage: 28\n\"\"\"\n"
    }
    
    
    -------runtime global final merged with dvars-------
    
    (*core.Cache)({
      "student_age": "28",
      "cli": "echo \"\"\"\nstudent details:\nname: Tom Hanks\nage: 28\n\"\"\"\n",
      "student_name": "Tom Hanks"
    })
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1: [: this show an example of the empty value is mapped to None ]
    {
      Name: "",
      Do: "echo \"{{.someone}}\"\necho \"{{.i_am_empty}}\"\necho \"{{.empty_env_var}}\"\n",
      Dox: <nil>,
      Func: "shell",
      Vars: {
        "person": ""
      },
      Dvars: {
        {
          Name: "someone",
          Value: "{{ .person }}",
          Desc: "",
          Expand: 0,
          Flags: <nil>,
          Rendered: "",
          Secure: (*utils.SecureSetting)(<nil>),
          Ref: "",
          RefDir: "",
          DataKey: "",
          DataPath: "",
          DataTemplate: ""
        },
        {
          Name: "i_am_empty",
          Value: "{{ \"\" }}",
          Desc: "",
          Expand: 0,
          Flags: <nil>,
          Rendered: "",
          Secure: (*utils.SecureSetting)(<nil>),
          Ref: "",
          RefDir: "",
          DataKey: "",
          DataPath: "",
          DataTemplate: ""
        },
        {
          Name: "empty_env_var",
          Value: "{{ env \"EMPTY_VAR\" }}",
          Desc: "",
          Expand: 0,
          Flags: <nil>,
          Rendered: "",
          Secure: (*utils.SecureSetting)(<nil>),
          Ref: "",
          RefDir: "",
          DataKey: "",
          DataPath: "",
          DataTemplate: ""
        }
      },
      Desc: "this show an example of the empty value is mapped to None",
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
      "student_age": "28",
      "cli": "echo \"\"\"\nstudent details:\nname: Tom Hanks\nage: 28\n\"\"\"\n",
      "student_name": "Tom Hanks",
      "up_runtime_task_layer_number": 0,
      "person": ""
    })
    
    [local] dvar expanded result:
    {
      "someone": "None",
      "i_am_empty": "None",
      "empty_env_var": "None"
    }
    
    
    scope[local] merged: {
      "up_runtime_task_layer_number": 0,
      "person": "",
      "student_age": "28",
      "cli": "echo \"\"\"\nstudent details:\nname: Tom Hanks\nage: 28\n\"\"\"\n",
      "student_name": "Tom Hanks",
      "i_am_empty": "None",
      "empty_env_var": "None",
      "someone": "None"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "empty_env_var": "None",
      "someone": "None",
      "student_age": "28",
      "cli": "echo \"\"\"\nstudent details:\nname: Tom Hanks\nage: 28\n\"\"\"\n",
      "student_name": "Tom Hanks",
      "up_runtime_task_layer_number": 0,
      "person": "",
      "i_am_empty": "None"
    })
    
    cmd( 1):
    echo "{{.someone}}"
    echo "{{.i_am_empty}}"
    echo "{{.empty_env_var}}"
    
    
    cmd=>:
    echo "None"
    echo "None"
    echo "None"
    
    -
    None
    None
    None
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=36) "echo \"None\"\necho \"None\"\necho \"None\"\n",
     Code: (int) 0,
     Output: (string) (len=14) "None\nNone\nNone",
     ErrMsg: (string) ""
    }
    
    . ok
    -Step2:
    {
      Name: "",
      Do: {
        {
          "name": "inspect",
          "cmd": {
            "exec_vars",
            "exec_base_vars"
          }
        }
      },
      Dox: <nil>,
      Func: "cmd",
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
      "cli": "echo \"\"\"\nstudent details:\nname: Tom Hanks\nage: 28\n\"\"\"\n",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"None\"\necho \"None\"\necho \"None\"\n",
        Code: 0,
        Output: "None\nNone\nNone",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0,
      "student_name": "Tom Hanks",
      "student_age": "28"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"None\"\necho \"None\"\necho \"None\"\n",
        Code: 0,
        Output: "None\nNone\nNone",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0,
      "student_name": "Tom Hanks",
      "student_age": "28",
      "cli": "echo \"\"\"\nstudent details:\nname: Tom Hanks\nage: 28\n\"\"\"\n"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "cli": "echo \"\"\"\nstudent details:\nname: Tom Hanks\nage: 28\n\"\"\"\n",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"None\"\necho \"None\"\necho \"None\"\n",
        Code: 0,
        Output: "None\nNone\nNone",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0,
      "student_name": "Tom Hanks",
      "student_age": "28"
    })
    
    [exec_vars exec_base_vars]
    ~SubStep1: [inspect:  ]
     1: inspect[exec_vars]
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"None\"\necho \"None\"\necho \"None\"\n",
        Code: 0,
        Output: "None\nNone\nNone",
        ErrMsg: ""
      }),
      "up_runtime_task_layer_number": 0,
      "student_name": "Tom Hanks",
      "student_age": "28",
      "cli": "echo \"\"\"\nstudent details:\nname: Tom Hanks\nage: 28\n\"\"\"\n"
    })
    
     2: inspect[exec_base_vars]
    {
      "student_name": "Tom Hanks",
      "student_age": "28",
      "cli": "echo \"\"\"\nstudent details:\nname: Tom Hanks\nage: 28\n\"\"\"\n",
      "last_result": (*utils.ExecResult)({
        Cmd: "echo \"None\"\necho \"None\"\necho \"None\"\n",
        Code: 0,
        Output: "None\nNone\nNone",
        ErrMsg: ""
      })
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
