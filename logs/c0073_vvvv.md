---
title: "c0073_vvvv"
date: 2020-08-09T01:36:09+88:00
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
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
                 Timeout -> 3600000
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0073
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
      "my_interesting_story6": "hello\nworld\n\n\n",
      "my_interesting_story1": "hello\nworld\n",
      "my_interesting_story2": "hello world",
      "my_interesting_story3": "hello world\n",
      "my_interesting_story4": "hello\nworld",
      "my_interesting_story5": "hello world"
    }
    
    -------runtime global final merged with dvars-------
    
    {
      "my_interesting_story2": "hello world",
      "my_interesting_story3": "hello world\n",
      "my_interesting_story4": "hello\nworld",
      "my_interesting_story5": "hello world",
      "my_interesting_story6": "hello\nworld\n\n\n",
      "my_interesting_story1": "hello\nworld\n"
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "my_interesting_story6": "hello\nworld\n\n\n",
      "my_interesting_story1": "hello\nworld\n",
      "my_interesting_story2": "hello world",
      "my_interesting_story3": "hello world\n",
      "my_interesting_story4": "hello\nworld",
      "my_interesting_story5": "hello world"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "my_interesting_story4": "hello\nworld",
      "my_interesting_story5": "hello world",
      "my_interesting_story6": "hello\nworld\n\n\n",
      "my_interesting_story1": "hello\nworld\n",
      "my_interesting_story2": "hello world",
      "my_interesting_story3": "hello world\n"
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
    current exec runtime vars:
    (*core.Cache)({
      "my_interesting_story4": "hello\nworld",
      "my_interesting_story5": "hello world",
      "my_interesting_story6": "hello\nworld\n\n\n",
      "my_interesting_story1": "hello\nworld\n",
      "newstory_with_blank_space_front_and_tail": " same old story ",
      "newstory_clean": "same old story",
      "my_interesting_story2": "hello world",
      "my_interesting_story3": "hello world\n"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "my_interesting_story3": "hello world\n",
      "my_interesting_story4": "hello\nworld",
      "my_interesting_story5": "hello world",
      "my_interesting_story6": "hello\nworld\n\n\n",
      "my_interesting_story1": "hello\nworld\n",
      "newstory_with_blank_space_front_and_tail": " same old story ",
      "newstory_clean": "same old story",
      "my_interesting_story2": "hello world"
    })
    
    cmd( 1):
    echo "[{{.my_interesting_story3}}]"
    
    cmd=>:
    echo "[hello world
    ]"<=
    [hello world
    ]
     .. ok
    cmd( 2):
    echo [{{.my_interesting_story5}}]
    
    cmd=>:
    echo [hello world]<=
    [hello world]
     .. ok
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
    cmd( 4):
    echo "[{{.newstory_with_blank_space_front_and_tail}}]"
    
    cmd=>:
    echo "[ same old story ]"<=
    [ same old story ]
     .. ok
    cmd( 5):
    echo "[{{.newstory_clean}}]"
    
    cmd=>:
    echo "[same old story]"<=
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
