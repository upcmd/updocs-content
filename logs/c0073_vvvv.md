---
title: "c0073_vvvv"
date: 2020-06-25T01:55:49+66:00
draft: false
weight: 10733

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
                 Verbose -> vvvv
              ModuleName -> distracted_elion9
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0073
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [distracted_elion9] instance id: [dev]
    merged[ dev ] runtime vars:
    {
      "my_interesting_story4": "hello\nworld",
      "my_interesting_story5": "hello world",
      "my_interesting_story6": "hello\nworld\n\n\n",
      "my_interesting_story1": "hello\nworld\n",
      "my_interesting_story2": "hello world",
      "my_interesting_story3": "hello world\n"
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
          "cmd": "[{{.my_interesting_story1}}]",
          "name": "print",
          "desc": "literal style, there will be a line break"
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
          "desc": "literal style strip, the end line break is removed",
          "cmd": "[{{.my_interesting_story4}}]",
          "name": "print"
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
      VarsFile: ""
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
    
    distracted_elion9: overall final exec vars:
    
    (*core.Cache)({
      "my_interesting_story1": "hello\nworld\n",
      "my_interesting_story2": "hello world",
      "my_interesting_story3": "hello world\n",
      "my_interesting_story4": "hello\nworld",
      "my_interesting_story5": "hello world",
      "my_interesting_story6": "hello\nworld\n\n\n"
    })
    
    ~SubStep1: [print: literal style, there will be a line break ]
    [hello
    world
    ]
    ~SubStep2: [print: there will be no a line break ]
    [hello world]
    ~SubStep3: [print: folded style ]
    [hello world
    ]
    ~SubStep4: [print: literal style strip, the end line break is removed ]
    [hello
    world]
    ~SubStep5: [reg:  ]
    ~SubStep6: [reg:  ]
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
      VarsFile: ""
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "newstory_with_blank_space_front_and_tail": " same old story ",
      "newstory_clean": "same old story",
      "my_interesting_story3": "hello world\n",
      "my_interesting_story4": "hello\nworld",
      "my_interesting_story5": "hello world",
      "my_interesting_story6": "hello\nworld\n\n\n",
      "my_interesting_story1": "hello\nworld\n",
      "my_interesting_story2": "hello world"
    })
    
    distracted_elion9: overall final exec vars:
    
    (*core.Cache)({
      "my_interesting_story1": "hello\nworld\n",
      "my_interesting_story2": "hello world",
      "newstory_with_blank_space_front_and_tail": " same old story ",
      "newstory_clean": "same old story",
      "my_interesting_story3": "hello world\n",
      "my_interesting_story4": "hello\nworld",
      "my_interesting_story5": "hello world",
      "my_interesting_story6": "hello\nworld\n\n\n"
    })
    
    cmd( 1):
    echo "[{{.my_interesting_story3}}]"
    
     \_ echo "[hello world
    ]"
    [hello world
    ]
     .. ok
    cmd( 2):
    echo [{{.my_interesting_story5}}]
    
     \_ echo [hello world]
    [hello world]
     .. ok
    cmd( 3):
    echo "[{{.my_interesting_story6}}]"
    
     \_ echo "[hello
    world
    
    
    ]"
    [hello
    world
    
    
    ]
     .. ok
    cmd( 4):
    echo "[{{.newstory_with_blank_space_front_and_tail}}]"
    
     \_ echo "[ same old story ]"
    [ same old story ]
     .. ok
    cmd( 5):
    echo "[{{.newstory_clean}}]"
    
     \_ echo "[same old story]"
    [same old story]
     .. ok
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
