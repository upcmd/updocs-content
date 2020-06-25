---
title: "c0042_vvvvv"
date: 2020-06-25T01:55:43+66:00
draft: false
weight: 10424

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
                 Verbose -> vvvvv
              ModuleName -> goofy_rosalind8
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0042
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001eb400)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [goofy_rosalind8] instance id: [dev]
    merged[ dev ] runtime vars:
    {
    }
    
    (core.Cache) {
    }
    
    [runtime global] dvar expanded result:
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
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
    }
    
    
    goofy_rosalind8: overall final exec vars:
    
    (*core.Cache)({
    })
    
    cmd( 1):
    echo tom
    
     \_ echo tom
    tom
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=3) "tom",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo hanks
    
     \_ echo hanks
    hanks
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=5) "hanks",
     ErrMsg: (string) ""
    }
    
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
    
    [local] dvar expanded result:
    {
      "reg_hello": "hello: \n"
    }
    
    
    scope[local] merged: {
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "hanks",
        ErrMsg: ""
      }),
      "reg_hello": "hello: \n"
    }
    
    
    goofy_rosalind8: overall final exec vars:
    
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
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=10) "<no value>",
     ErrMsg: (string) ""
    }
    
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
    
    [local] dvar expanded result:
    {
      "reg_hello": "\n"
    }
    
    
    scope[local] merged: {
      "reg_hello": "\n",
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "<no value>",
        ErrMsg: ""
      }),
      "hellomsg": "hanks"
    }
    
    
    goofy_rosalind8: overall final exec vars:
    
    (*core.Cache)({
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "<no value>",
        ErrMsg: ""
      }),
      "hellomsg": "hanks",
      "reg_hello": "\n"
    })
    
    cmd( 1):
    echo "{{.hellomsg}}"
    
     \_ echo "hanks"
    hanks
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=5) "hanks",
     ErrMsg: (string) ""
    }
    
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
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "hanks",
        ErrMsg: ""
      })
    }
    
    
    goofy_rosalind8: overall final exec vars:
    
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
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=10) "<no value>",
     ErrMsg: (string) ""
    }
    
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
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "<no value>",
        ErrMsg: ""
      })
    }
    
    
    goofy_rosalind8: overall final exec vars:
    
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
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=10) "<no value>",
     ErrMsg: (string) ""
    }
    
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
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "iamvoid": "something",
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "<no value>",
        ErrMsg: ""
      })
    }
    
    
    goofy_rosalind8: overall final exec vars:
    
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
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=9) "something",
     ErrMsg: (string) ""
    }
    
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
