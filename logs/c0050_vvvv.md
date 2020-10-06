---
title: "c0050_vvvv"
date: 2020-10-06T23:45:59+1010:00
draft: false
weight: 10503

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0050
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
    loading [Task]:  ./tests/functests/c0050
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
      "school": "Sydney Grammar"
    })
    
    -------runtime global final merged with dvars-------
    
    (*core.Cache)({
      "j": "j=>m=>n=>Sydney Grammar",
      "o": "o=><no value>",
      "z": "i am zzz",
      "yv": "y->i am zzz",
      "x": "x=>y->i am zzz",
      "school": "Sydney Grammar",
      "nv": "n=>Sydney Grammar",
      "m": "m=>n=>Sydney Grammar"
    })
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "up_runtime_task_layer_number": 0,
      "nv": "n=>Sydney Grammar",
      "o": "o=><no value>",
      "school": "Sydney Grammar",
      "z": "i am zzz",
      "yv": "y->i am zzz",
      "m": "m=>n=>Sydney Grammar",
      "j": "j=>m=>n=>Sydney Grammar",
      "x": "x=>y->i am zzz"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "j": "j=>m=>n=>Sydney Grammar",
      "x": "x=>y->i am zzz",
      "yv": "y->i am zzz",
      "m": "m=>n=>Sydney Grammar",
      "o": "o=><no value>",
      "school": "Sydney Grammar",
      "z": "i am zzz",
      "up_runtime_task_layer_number": 0,
      "nv": "n=>Sydney Grammar"
    })
    
    cmd( 1):
    echo "n->{{.nv}}"
    
    cmd=>:
    echo "n->n=>Sydney Grammar"
    -
    n->n=>Sydney Grammar
    
    -
     .. ok
    cmd( 2):
    echo "m->{{.m}}"
    
    cmd=>:
    echo "m->m=>n=>Sydney Grammar"
    -
    m->m=>n=>Sydney Grammar
    
    -
     .. ok
    cmd( 3):
    echo "j->{{.j}}"
    
    cmd=>:
    echo "j->j=>m=>n=>Sydney Grammar"
    -
    j->j=>m=>n=>Sydney Grammar
    
    -
     .. ok
    cmd( 4):
    echo "o->{{.o}}"
    
    cmd=>:
    echo "o->o=><no value>"
    -
    o->o=><no value>
    
    -
     .. ok
    cmd( 5):
    echo "z->{{.z}}"
    
    cmd=>:
    echo "z->i am zzz"
    -
    z->i am zzz
    
    -
     .. ok
    cmd( 6):
    echo "y->{{.yv}}"
    
    cmd=>:
    echo "y->y->i am zzz"
    -
    y->y->i am zzz
    
    -
     .. ok
    cmd( 7):
    echo "x->{{.x}}"
    
    cmd=>:
    echo "x->x=>y->i am zzz"
    -
    x->x=>y->i am zzz
    
    -
     .. ok
    . ok
    
```

##### Logs with different verbose level
* [c0050 log - verbose level v](../../logs/c0050_v)
* [c0050 log - verbose level vv](../../logs/c0050_vv)
* [c0050 log - verbose level vvv](../../logs/c0050_vvv)
* [c0050 log - verbose level vvvv](../../logs/c0050_vvvv)
* [c0050 log - verbose level vvvvv](../../logs/c0050_vvvvv)

##### References
* [Related Chapter](../../dvars/c0050)
