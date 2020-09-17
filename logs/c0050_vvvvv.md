---
title: "c0050_vvvvv"
date: 2020-09-18T01:27:28+99:00
draft: false
weight: 10504

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
                 Verbose -> vvvvv
              ModuleName -> self
               ShellType -> /bin/sh
           MaxCallLayers -> 8
                 Timeout -> 3600000
     MaxModuelCallLayers -> 256
               EntryTask -> task
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0050
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    -------full vars in scopes------
    (*impl.Scopes)(0xc00022c460)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    {
      "school": "Sydney Grammar"
    }
    
    (core.Cache) (len=1) {
     (string) (len=6) "school": (string) (len=14) "Sydney Grammar"
    }
    
    [runtime global] dvar expanded result:
    {
      "yv": "y->i am zzz",
      "x": "x=>y->i am zzz",
      "nv": "n=>Sydney Grammar",
      "m": "m=>n=>Sydney Grammar",
      "j": "j=>m=>n=>Sydney Grammar",
      "o": "o=><no value>",
      "z": "i am zzz"
    }
    
    
    -------runtime global final merged with dvars-------
    
    {
      "j": "j=>m=>n=>Sydney Grammar",
      "o": "o=><no value>",
      "z": "i am zzz",
      "yv": "y->i am zzz",
      "x": "x=>y->i am zzz",
      "nv": "n=>Sydney Grammar",
      "school": "Sydney Grammar",
      "m": "m=>n=>Sydney Grammar"
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
      VarsFile: "",
      Timeout: 0,
      Finally: <nil>,
      Rescue: false
    }
    
    current exec runtime vars:
    (*core.Cache)({
      "o": "o=><no value>",
      "z": "i am zzz",
      "yv": "y->i am zzz",
      "up_runtime_task_layer_number": 0,
      "j": "j=>m=>n=>Sydney Grammar",
      "nv": "n=>Sydney Grammar",
      "school": "Sydney Grammar",
      "m": "m=>n=>Sydney Grammar",
      "x": "x=>y->i am zzz"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "j": "j=>m=>n=>Sydney Grammar",
      "o": "o=><no value>",
      "z": "i am zzz",
      "m": "m=>n=>Sydney Grammar",
      "nv": "n=>Sydney Grammar",
      "school": "Sydney Grammar",
      "up_runtime_task_layer_number": 0,
      "x": "x=>y->i am zzz",
      "yv": "y->i am zzz"
    }
    
    
    self: final context exec vars:
    
    (*core.Cache)({
      "yv": "y->i am zzz",
      "up_runtime_task_layer_number": 0,
      "j": "j=>m=>n=>Sydney Grammar",
      "o": "o=><no value>",
      "z": "i am zzz",
      "m": "m=>n=>Sydney Grammar",
      "x": "x=>y->i am zzz",
      "nv": "n=>Sydney Grammar",
      "school": "Sydney Grammar"
    })
    
    cmd( 1):
    echo "n->{{.nv}}"
    
    cmd=>:
    echo "n->n=>Sydney Grammar"
    -
    n->n=>Sydney Grammar
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=27) "echo \"n->n=>Sydney Grammar\"",
     Code: (int) 0,
     Output: (string) (len=20) "n->n=>Sydney Grammar",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo "m->{{.m}}"
    
    cmd=>:
    echo "m->m=>n=>Sydney Grammar"
    -
    m->m=>n=>Sydney Grammar
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=30) "echo \"m->m=>n=>Sydney Grammar\"",
     Code: (int) 0,
     Output: (string) (len=23) "m->m=>n=>Sydney Grammar",
     ErrMsg: (string) ""
    }
    
    cmd( 3):
    echo "j->{{.j}}"
    
    cmd=>:
    echo "j->j=>m=>n=>Sydney Grammar"
    -
    j->j=>m=>n=>Sydney Grammar
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=33) "echo \"j->j=>m=>n=>Sydney Grammar\"",
     Code: (int) 0,
     Output: (string) (len=26) "j->j=>m=>n=>Sydney Grammar",
     ErrMsg: (string) ""
    }
    
    cmd( 4):
    echo "o->{{.o}}"
    
    cmd=>:
    echo "o->o=><no value>"
    -
    o->o=><no value>
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=23) "echo \"o->o=><no value>\"",
     Code: (int) 0,
     Output: (string) (len=16) "o->o=><no value>",
     ErrMsg: (string) ""
    }
    
    cmd( 5):
    echo "z->{{.z}}"
    
    cmd=>:
    echo "z->i am zzz"
    -
    z->i am zzz
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=18) "echo \"z->i am zzz\"",
     Code: (int) 0,
     Output: (string) (len=11) "z->i am zzz",
     ErrMsg: (string) ""
    }
    
    cmd( 6):
    echo "y->{{.yv}}"
    
    cmd=>:
    echo "y->y->i am zzz"
    -
    y->y->i am zzz
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=21) "echo \"y->y->i am zzz\"",
     Code: (int) 0,
     Output: (string) (len=14) "y->y->i am zzz",
     ErrMsg: (string) ""
    }
    
    cmd( 7):
    echo "x->{{.x}}"
    
    cmd=>:
    echo "x->x=>y->i am zzz"
    -
    x->x=>y->i am zzz
    
    -
     .. ok
    (utils.ExecResult) {
     Cmd: (string) (len=24) "echo \"x->x=>y->i am zzz\"",
     Code: (int) 0,
     Output: (string) (len=17) "x->x=>y->i am zzz",
     ErrMsg: (string) ""
    }
    
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
