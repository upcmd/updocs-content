---
title: "c0050_vvvv"
date: 2020-06-25T01:55:45+66:00
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
              ModuleName -> modest_euclid6
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0050
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [modest_euclid6] instance id: [dev]
    merged[ dev ] runtime vars:
    {
      "school": "Sydney Grammar"
    }
    
    -------runtime global final merged with dvars-------
    
    {
      "x": "x=>y->i am zzz",
      "nv": "n=>Sydney Grammar",
      "m": "m=>n=>Sydney Grammar",
      "j": "j=>m=>n=>Sydney Grammar",
      "school": "Sydney Grammar",
      "o": "o=><no value>",
      "z": "i am zzz",
      "yv": "y->i am zzz"
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    {
      Name: "",
      Do: {
        "echo \"n->{{.nv}}\"",
        "echo \"m->{{.m}}\"",
        "echo \"j->{{.j}}\"",
        "echo \"o->{{.o}}\"",
        "echo \"z->{{.z}}\"",
        "echo \"y->{{.yv}}\"",
        "echo \"x->{{.x}}\""
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
      "yv": "y->i am zzz",
      "x": "x=>y->i am zzz",
      "nv": "n=>Sydney Grammar",
      "m": "m=>n=>Sydney Grammar",
      "j": "j=>m=>n=>Sydney Grammar",
      "school": "Sydney Grammar",
      "o": "o=><no value>",
      "z": "i am zzz"
    })
    
    modest_euclid6: overall final exec vars:
    
    (*core.Cache)({
      "x": "x=>y->i am zzz",
      "nv": "n=>Sydney Grammar",
      "m": "m=>n=>Sydney Grammar",
      "j": "j=>m=>n=>Sydney Grammar",
      "school": "Sydney Grammar",
      "o": "o=><no value>",
      "z": "i am zzz",
      "yv": "y->i am zzz"
    })
    
    cmd( 1):
    echo "n->{{.nv}}"
    
     \_ echo "n->n=>Sydney Grammar"
    n->n=>Sydney Grammar
     .. ok
    cmd( 2):
    echo "m->{{.m}}"
    
     \_ echo "m->m=>n=>Sydney Grammar"
    m->m=>n=>Sydney Grammar
     .. ok
    cmd( 3):
    echo "j->{{.j}}"
    
     \_ echo "j->j=>m=>n=>Sydney Grammar"
    j->j=>m=>n=>Sydney Grammar
     .. ok
    cmd( 4):
    echo "o->{{.o}}"
    
     \_ echo "o->o=><no value>"
    o->o=><no value>
     .. ok
    cmd( 5):
    echo "z->{{.z}}"
    
     \_ echo "z->i am zzz"
    z->i am zzz
     .. ok
    cmd( 6):
    echo "y->{{.yv}}"
    
     \_ echo "y->y->i am zzz"
    y->y->i am zzz
     .. ok
    cmd( 7):
    echo "x->{{.x}}"
    
     \_ echo "x->x=>y->i am zzz"
    x->x=>y->i am zzz
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