---
title: "c0073_vvvvv"
date: 2020-08-09T01:36:09+88:00
draft: false
weight: 10734

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0073
                 Verbose -> vvvvv
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
                 Timeout -> 3600000
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0073
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc0002044e0)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    {
      "my_interesting_story5": "hello world",
      "my_interesting_story6": "hello\nworld\n\n\n",
      "my_interesting_story1": "hello\nworld\n",
      "my_interesting_story2": "hello world",
      "my_interesting_story3": "hello world\n",
      "my_interesting_story4": "hello\nworld"
    }
    
    (core.Cache) (len=6) {
     (string) (len=21) "my_interesting_story6": (string) (len=14) "hello\nworld\n\n\n",
     (string) (len=21) "my_interesting_story1": (string) (len=12) "hello\nworld\n",
     (string) (len=21) "my_interesting_story2": (string) (len=11) "hello world",
     (string) (len=21) "my_interesting_story3": (string) (len=12) "hello world\n",
     (string) (len=21) "my_interesting_story4": (string) (len=11) "hello\nworld",
     (string) (len=21) "my_interesting_story5": (string) (len=11) "hello world"
    }
    
    [runtime global] dvar expanded result:
    {
    }
    
    
    -------runtime global final merged with dvars-------
    
    {
      "my_interesting_story3": "hello world\n",
      "my_interesting_story4": "hello\nworld",
      "my_interesting_story5": "hello world",
      "my_interesting_story6": "hello\nworld\n\n\n",
      "my_interesting_story1": "hello\nworld\n",
      "my_interesting_story2": "hello world"
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "desc": "literal style, there will be a line break",
          "cmd": "[{{.my_interesting_story1}}]"
        },
        {
          "name": "print",
          "desc": "there will be no a line break",
          "cmd": "[{{.my_interesting_story2}}]"
        },
        {
          "cmd": "[{{.my_interesting_story3}}]",
          "name": "print",
          "desc": "folded style"
        },
        {
          "name": "print",
          "desc": "literal style strip, the end line break is removed",
          "cmd": "[{{.my_interesting_story4}}]"
        },
        {
          "name": "reg",
          "cmd": {
            "name": "newstory_with_blank_space_front_and_tail",
            "desc": "you can't remove the empty space because it is from the folded feature of yaml",
            "value": "{{if .isnew }} this is a new story {{else}} same old story {{end}}"
          }
        },
        {
          "name": "reg",
          "cmd": {
            "name": "newstory_clean",
            "value": "{{if .isnew}}this is a new story{{else}}same old story{{end}}"
          }
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: {
        "isnew": false
      },
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
      "my_interesting_story5": "hello world",
      "my_interesting_story6": "hello\nworld\n\n\n",
      "my_interesting_story1": "hello\nworld\n",
      "my_interesting_story2": "hello world",
      "my_interesting_story3": "hello world\n",
      "my_interesting_story4": "hello\nworld"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "my_interesting_story2": "hello world",
      "my_interesting_story3": "hello world\n",
      "my_interesting_story4": "hello\nworld",
      "my_interesting_story5": "hello world",
      "my_interesting_story6": "hello\nworld\n\n\n",
      "my_interesting_story1": "hello\nworld\n"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "my_interesting_story3": "hello world\n",
      "my_interesting_story4": "hello\nworld",
      "my_interesting_story5": "hello world",
      "my_interesting_story6": "hello\nworld\n\n\n",
      "my_interesting_story1": "hello\nworld\n",
      "my_interesting_story2": "hello world"
    })
    
    [{{.my_interesting_story1}}]
    ~SubStep1: [print: literal style, there will be a line break ]
    [hello
    world
    ]
    [{{.my_interesting_story2}}]
    ~SubStep2: [print: there will be no a line break ]
    [hello world]
    [{{.my_interesting_story3}}]
    ~SubStep3: [print: folded style ]
    [hello world
    ]
    [{{.my_interesting_story4}}]
    ~SubStep4: [print: literal style strip, the end line break is removed ]
    [hello
    world]
    map[desc:you can't remove the empty space because it is from the folded feature of yaml name:newstory_with_blank_space_front_and_tail value:{{if .isnew }} this is a new story {{else}} same old story {{end}}]
    ~SubStep5: [reg:  ]
    after reg the var - contextual global:
    
    (*core.Cache)({
      "my_interesting_story3": "hello world\n",
      "my_interesting_story4": "hello\nworld",
      "newstory_with_blank_space_front_and_tail": " same old story ",
      "my_interesting_story5": "hello world",
      "my_interesting_story6": "hello\nworld\n\n\n",
      "my_interesting_story1": "hello\nworld\n",
      "my_interesting_story2": "hello world"
    })
    
    after reg the var - local:
    
    (*core.Cache)({
      "newstory_with_blank_space_front_and_tail": " same old story ",
      "my_interesting_story5": "hello world",
      "my_interesting_story6": "hello\nworld\n\n\n",
      "my_interesting_story1": "hello\nworld\n",
      "my_interesting_story2": "hello world",
      "my_interesting_story3": "hello world\n",
      "my_interesting_story4": "hello\nworld"
    })
    
    map[name:newstory_clean value:{{if .isnew}}this is a new story{{else}}same old story{{end}}]
    ~SubStep6: [reg:  ]
    after reg the var - contextual global:
    
    (*core.Cache)({
      "newstory_with_blank_space_front_and_tail": " same old story ",
      "newstory_clean": "same old story",
      "my_interesting_story5": "hello world",
      "my_interesting_story6": "hello\nworld\n\n\n",
      "my_interesting_story1": "hello\nworld\n",
      "my_interesting_story2": "hello world",
      "my_interesting_story3": "hello world\n",
      "my_interesting_story4": "hello\nworld"
    })
    
    after reg the var - local:
    
    (*core.Cache)({
      "my_interesting_story1": "hello\nworld\n",
      "my_interesting_story2": "hello world",
      "my_interesting_story3": "hello world\n",
      "my_interesting_story4": "hello\nworld",
      "newstory_with_blank_space_front_and_tail": " same old story ",
      "newstory_clean": "same old story",
      "my_interesting_story5": "hello world",
      "my_interesting_story6": "hello\nworld\n\n\n"
    })
    
    -Step2:
    {
      Name: "",
      Do: {
        "echo \"[{{.my_interesting_story3}}]\"",
        "echo [{{.my_interesting_story5}}]",
        "echo \"[{{.my_interesting_story6}}]\"",
        "echo \"[{{.newstory_with_blank_space_front_and_tail}}]\"",
        "echo \"[{{.newstory_clean}}]\""
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
      "my_interesting_story6": "hello\nworld\n\n\n",
      "my_interesting_story1": "hello\nworld\n",
      "my_interesting_story2": "hello world",
      "my_interesting_story3": "hello world\n",
      "my_interesting_story4": "hello\nworld",
      "newstory_with_blank_space_front_and_tail": " same old story ",
      "newstory_clean": "same old story",
      "my_interesting_story5": "hello world"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "my_interesting_story5": "hello world",
      "my_interesting_story6": "hello\nworld\n\n\n",
      "my_interesting_story1": "hello\nworld\n",
      "my_interesting_story2": "hello world",
      "my_interesting_story3": "hello world\n",
      "my_interesting_story4": "hello\nworld",
      "newstory_with_blank_space_front_and_tail": " same old story ",
      "newstory_clean": "same old story"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "newstory_with_blank_space_front_and_tail": " same old story ",
      "newstory_clean": "same old story",
      "my_interesting_story5": "hello world",
      "my_interesting_story6": "hello\nworld\n\n\n",
      "my_interesting_story1": "hello\nworld\n",
      "my_interesting_story2": "hello world",
      "my_interesting_story3": "hello world\n",
      "my_interesting_story4": "hello\nworld"
    })
    
    cmd( 1):
    echo "[{{.my_interesting_story3}}]"
    
    cmd=>:
    echo "[hello world
    ]"<=
    [hello world
    ]
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=21) "echo \"[hello world\n]\"",
     Code: (int) 0,
     Output: (string) (len=14) "[hello world\n]",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo [{{.my_interesting_story5}}]
    
    cmd=>:
    echo [hello world]<=
    [hello world]
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=18) "echo [hello world]",
     Code: (int) 0,
     Output: (string) (len=13) "[hello world]",
     ErrMsg: (string) ""
    }
    
    cmd( 3):
    echo "[{{.my_interesting_story6}}]"
    
    cmd=>:
    echo "[hello
    world
    
    
    ]"<=
    [hello
    world
    
    
    ]
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=23) "echo \"[hello\nworld\n\n\n]\"",
     Code: (int) 0,
     Output: (string) (len=16) "[hello\nworld\n\n\n]",
     ErrMsg: (string) ""
    }
    
    cmd( 4):
    echo "[{{.newstory_with_blank_space_front_and_tail}}]"
    
    cmd=>:
    echo "[ same old story ]"<=
    [ same old story ]
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=25) "echo \"[ same old story ]\"",
     Code: (int) 0,
     Output: (string) (len=18) "[ same old story ]",
     ErrMsg: (string) ""
    }
    
    cmd( 5):
    echo "[{{.newstory_clean}}]"
    
    cmd=>:
    echo "[same old story]"<=
    [same old story]
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=23) "echo \"[same old story]\"",
     Code: (int) 0,
     Output: (string) (len=16) "[same old story]",
     ErrMsg: (string) ""
    }
    
    . ok
    
```

##### Logs with different verbose level
* [c0073 log - verbose level v](../../logs/c0073_v)
* [c0073 log - verbose level vv](../../logs/c0073_vv)
* [c0073 log - verbose level vvv](../../logs/c0073_vvv)
* [c0073 log - verbose level vvvv](../../logs/c0073_vvvv)
* [c0073 log - verbose level vvvvv](../../logs/c0073_vvvvv)

##### References
* [Related Chapter](../../syntax/c0073)
