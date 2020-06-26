---
title: "c0042_vvvv"
date: 2020-06-27T03:09:19+66:00
draft: false
weight: 10423

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0042
                 Verbose -> vvvv
              ModuleName -> high_payne8
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0042
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [high_payne8] instance id: [dev]
    merged[ dev ] runtime vars:
    {
    }
    
    -------runtime global final merged with dvars-------
    
    {
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task: test the exit scenarios due to different types of validation ]
    Executing task stack layer: 1
    
    -Step1: [: step1 ]
    {
      Name: "",
      Do: {
        "echo tom",
        "echo hanks"
      },
      Dox: <nil>,
      Func: "shell",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "step1",
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
    })
    
    high_payne8: overall final exec vars:
    
    (*core.Cache)({
    })
    
    cmd( 1):
    echo tom
    
     \_ echo tom
    tom
     .. ok
    cmd( 2):
    echo hanks
    
     \_ echo hanks
    hanks
     .. ok
    . ok
    -Step2: [: the last result of hanks will be registered as varname: hellomsg
    however this will be availabe at the next step
    as when it enters this step, it has already got a copied immutable var stack
     ]
    {
      Name: "",
      Do: {
        "echo \"{{.hellomsg}}\""
      },
      Dox: <nil>,
      Func: "shell",
      Vars: <nil>,
      Dvars: {
        {
          Name: "reg_hello",
          Value: "hello: {{.last_result.Output |reg \"hellomsg\" }}\n",
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
      Desc: "the last result of hanks will be registered as varname: hellomsg\nhowever this will be availabe at the next step\nas when it enters this step, it has already got a copied immutable var stack\n",
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
        Output: "hanks",
        ErrMsg: ""
      })
    })
    
    high_payne8: overall final exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "hanks",
        ErrMsg: ""
      }),
      "reg_hello": "hello: \n"
    })
    
    cmd( 1):
    echo "{{.hellomsg}}"
    
     \_ echo "<no value>"
    <no value>
     .. ok
    . ok
    -Step3: [: the hellomsg will be still availabe in this step
    it is removed but will be unavailabe in the next step
     ]
    {
      Name: "",
      Do: {
        "echo \"{{.hellomsg}}\""
      },
      Dox: <nil>,
      Func: "shell",
      Vars: <nil>,
      Dvars: {
        {
          Name: "reg_hello",
          Value: "{{dereg \"hellomsg\" }}\n",
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
      Desc: "the hellomsg will be still availabe in this step\nit is removed but will be unavailabe in the next step\n",
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
        Output: "<no value>",
        ErrMsg: ""
      }),
      "hellomsg": "hanks"
    })
    
    high_payne8: overall final exec vars:
    
    (*core.Cache)({
      "reg_hello": "\n",
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "<no value>",
        ErrMsg: ""
      }),
      "hellomsg": "hanks"
    })
    
    cmd( 1):
    echo "{{.hellomsg}}"
    
     \_ echo "hanks"
    hanks
     .. ok
    . ok
    -Step4: [: now the hellomsg should be <no value>
     ]
    {
      Name: "",
      Do: {
        "echo \"{{.hellomsg}}\""
      },
      Dox: <nil>,
      Func: "shell",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "now the hellomsg should be <no value>\n",
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
        Output: "hanks",
        ErrMsg: ""
      })
    })
    
    high_payne8: overall final exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "hanks",
        ErrMsg: ""
      })
    })
    
    cmd( 1):
    echo "{{.hellomsg}}"
    
     \_ echo "<no value>"
    <no value>
     .. ok
    . ok
    -Step5:
    {
      Name: "",
      Do: {
        "echo '{{.iamvoid}}'"
      },
      Dox: <nil>,
      Func: "shell",
      Vars: <nil>,
      Dvars: {
        {
          Name: "void",
          Value: "hello: {{ print \"something\" |reg \"iamvoid\" }}",
          Desc: "now this var name will not be shown in local automatically\nor in global if you register it as it the reg template func\nis more like a action and return sensible value\n",
          Expand: 0,
          Flags: {
            "vvv"
          },
          Rendered: "",
          Secure: (*utils.SecureSetting)(<nil>),
          Ref: "",
          RefDir: "",
          DataKey: "",
          DataPath: "",
          DataTemplate: ""
        }
      },
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
        Output: "<no value>",
        ErrMsg: ""
      })
    })
    
    dvar> void:
    "hello: "
    
    high_payne8: overall final exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "<no value>",
        ErrMsg: ""
      })
    })
    
    cmd( 1):
    echo '{{.iamvoid}}'
    
     \_ echo '<no value>'
    <no value>
     .. ok
    . ok
    -Step6:
    {
      Name: "",
      Do: {
        "echo '{{.iamvoid}}'"
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
        Output: "<no value>",
        ErrMsg: ""
      }),
      "iamvoid": "something"
    })
    
    high_payne8: overall final exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "<no value>",
        ErrMsg: ""
      }),
      "iamvoid": "something"
    })
    
    cmd( 1):
    echo '{{.iamvoid}}'
    
     \_ echo 'something'
    something
     .. ok
    . ok
    
```

##### Logs with different verbose level
* [c0042 log - verbose level v](../../logs/c0042_v)
* [c0042 log - verbose level vv](../../logs/c0042_vv)
* [c0042 log - verbose level vvv](../../logs/c0042_vvv)
* [c0042 log - verbose level vvvv](../../logs/c0042_vvvv)
* [c0042 log - verbose level vvvvv](../../logs/c0042_vvvvv)

##### References
* [Related Chapter](../../template/c0042)
