---
title: "c0073_vvvv"
date: 2020-10-06T23:46:03+1010:00
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
               EntryTask -> task
      ModRepoUsernameRef -> 
      ModRepoPasswordRef -> 
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
    
    global: (*core.Cache)({
    })
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    (*core.Cache)({
      "my_interesting_story3": "hello world\n",
      "my_interesting_story4": "hello\nworld",
      "my_interesting_story5": "hello world",
      "my_interesting_story6": "hello\nworld\n\n\n",
      "my_interesting_story1": "hello\nworld\n",
      "my_interesting_story2": "hello world"
    })
    
    -------runtime global final merged with dvars-------
    
    (*core.Cache)({
      "my_interesting_story6": "hello\nworld\n\n\n",
      "my_interesting_story1": "hello\nworld\n",
      "my_interesting_story2": "hello world",
      "my_interesting_story3": "hello world\n",
      "my_interesting_story4": "hello\nworld",
      "my_interesting_story5": "hello world"
    })
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "my_interesting_story3": "hello world\n",
      "my_interesting_story4": "hello\nworld",
      "up_runtime_task_layer_number": 0,
      "isnew": false,
      "my_interesting_story5": "hello world",
      "my_interesting_story6": "hello\nworld\n\n\n",
      "my_interesting_story1": "hello\nworld\n",
      "my_interesting_story2": "hello world"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "my_interesting_story1": "hello\nworld\n",
      "my_interesting_story2": "hello world",
      "my_interesting_story3": "hello world\n",
      "my_interesting_story4": "hello\nworld",
      "up_runtime_task_layer_number": 0,
      "isnew": false,
      "my_interesting_story5": "hello world",
      "my_interesting_story6": "hello\nworld\n\n\n"
    })
    
    ~SubStep1: [print:  ]
    bb
    ~SubStep2: [print: literal style, there will be a line break ]
    [hello
    world
    ]
    ~SubStep3: [print: there will be no a line break ]
    [hello world]
    ~SubStep4: [print: folded style ]
    [hello world
    ]
    ~SubStep5: [print: literal style strip, the end line break is removed ]
    [hello
    world]
    ~SubStep6: [reg:  ]
    ~SubStep7: [reg:  ]
    -Step2:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "my_interesting_story3": "hello world\n",
      "newstory_with_blank_space_front_and_tail": " same old story ",
      "my_interesting_story1": "hello\nworld\n",
      "my_interesting_story2": "hello world",
      "newstory_clean": "same old story",
      "my_interesting_story5": "hello world",
      "my_interesting_story6": "hello\nworld\n\n\n",
      "my_interesting_story4": "hello\nworld"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "my_interesting_story1": "hello\nworld\n",
      "my_interesting_story3": "hello world\n",
      "up_runtime_task_layer_number": 0,
      "my_interesting_story2": "hello world",
      "my_interesting_story5": "hello world",
      "my_interesting_story6": "hello\nworld\n\n\n",
      "my_interesting_story4": "hello\nworld",
      "newstory_with_blank_space_front_and_tail": " same old story ",
      "newstory_clean": "same old story"
    })
    
    cmd( 1):
    echo "[{{.my_interesting_story3}}]"
    
    cmd=>:
    echo "[hello world
    ]"
    -
    [hello world
    ]
    
    -
     .. ok
    cmd( 2):
    echo [{{.my_interesting_story5}}]
    
    cmd=>:
    echo [hello world]
    -
    [hello world]
    
    -
     .. ok
    cmd( 3):
    echo "[{{.my_interesting_story6}}]"
    
    cmd=>:
    echo "[hello
    world
    
    
    ]"
    -
    [hello
    world
    
    
    ]
    
    -
     .. ok
    cmd( 4):
    echo "[{{.newstory_with_blank_space_front_and_tail}}]"
    
    cmd=>:
    echo "[ same old story ]"
    -
    [ same old story ]
    
    -
     .. ok
    cmd( 5):
    echo "[{{.newstory_clean}}]"
    
    cmd=>:
    echo "[same old story]"
    -
    [same old story]
    
    -
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
