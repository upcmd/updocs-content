---
title: "c0023_vvvv"
date: 2020-10-07T00:11:04+1010:00
draft: false
weight: 10233

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0023
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
    loading [Task]:  ./tests/functests/c0023
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
      "school": "Sydney Grammar",
      "a1": "a1->{{.b2}}",
      "b2": "b2->{{.c3}}",
      "c3": "c3->{{.d4}}",
      "d4": "d4->{{.student}}",
      "student": "Tom",
      "gender": "Male"
    })
    
    -------runtime global final merged with dvars-------
    
    (*core.Cache)({
      "gender": "Male",
      "a1": "a1->{{.b2}}",
      "b2": "b2->{{.c3}}",
      "d4": "d4->{{.student}}",
      "multple_render_var_level3_with_expand2": "multple-render-var-> b2->c3->{{.d4}}",
      "multple_render_var_level5": "multple-render-var-> a1->b2->c3->d4->Tom",
      "student": "Tom",
      "dependon_var_and_dvar": "Tom-Male",
      "multple_render_var_level3_with_expand3": "multple-render-var-> b2->c3->d4->{{.student}}",
      "school": "Sydney Grammar",
      "dependon_vars": "Male",
      "multple_render_var_level3": "multple-render-var-> b2->{{.c3}}",
      "multple_render_var_level3_with_expand4": "multple-render-var-> b2->c3->d4->Tom",
      "from": "Sydney Grammar",
      "sex": "Male",
      "c3": "c3->{{.d4}}"
    })
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "gender": "Male",
      "multple_render_var_level3": "multple-render-var-> b2->{{.c3}}",
      "d4": "d4->{{.student}}",
      "school": "Sydney Grammar",
      "dependon_var_and_dvar": "Tom-Male",
      "multple_render_var_level3_with_expand4": "multple-render-var-> b2->c3->d4->Tom",
      "multple_render_var_level5": "multple-render-var-> a1->b2->c3->d4->Tom",
      "sex": "Male",
      "up_runtime_task_layer_number": 0,
      "a1": "a1->{{.b2}}",
      "multple_render_var_level3_with_expand2": "multple-render-var-> b2->c3->{{.d4}}",
      "from": "Sydney Grammar",
      "student": "Tom",
      "c3": "c3->{{.d4}}",
      "multple_render_var_level3_with_expand3": "multple-render-var-> b2->c3->d4->{{.student}}",
      "dependon_vars": "Male",
      "b2": "b2->{{.c3}}"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "from": "Sydney Grammar",
      "b2": "b2->{{.c3}}",
      "sex": "Male",
      "up_runtime_task_layer_number": 0,
      "multple_render_var_level5": "multple-render-var-> a1->b2->c3->d4->Tom",
      "multple_render_var_level3_with_expand3": "multple-render-var-> b2->c3->d4->{{.student}}",
      "multple_render_var_level3": "multple-render-var-> b2->{{.c3}}",
      "gender": "Male",
      "c3": "c3->{{.d4}}",
      "a1": "a1->{{.b2}}",
      "dependon_vars": "Male",
      "dependon_var_and_dvar": "Tom-Male",
      "multple_render_var_level3_with_expand4": "multple-render-var-> b2->c3->d4->Tom",
      "student": "Tom",
      "multple_render_var_level3_with_expand2": "multple-render-var-> b2->c3->{{.d4}}",
      "d4": "d4->{{.student}}",
      "school": "Sydney Grammar"
    })
    
    cmd( 1):
    echo "student=>{{.student}}"
    
    cmd=>:
    echo "student=>Tom"
    -
    student=>Tom
    
    -
     .. ok
    cmd( 2):
    echo "a1=> a1->{{.b2}}"
    
    cmd=>:
    echo "a1=> a1->b2->{{.c3}}"
    -
    a1=> a1->b2->{{.c3}}
    
    -
     .. ok
    cmd( 3):
    echo "from->{{.from}}"
    
    cmd=>:
    echo "from->Sydney Grammar"
    -
    from->Sydney Grammar
    
    -
     .. ok
    cmd( 4):
    echo "sex->{{.sex}}"
    
    cmd=>:
    echo "sex->Male"
    -
    sex->Male
    
    -
     .. ok
    cmd( 5):
    echo "dependon_vars->{{.dependon_vars}}"
    
    cmd=>:
    echo "dependon_vars->Male"
    -
    dependon_vars->Male
    
    -
     .. ok
    cmd( 6):
    echo "dependon_var_and_dvar->{{.dependon_var_and_dvar}}"
    
    cmd=>:
    echo "dependon_var_and_dvar->Tom-Male"
    -
    dependon_var_and_dvar->Tom-Male
    
    -
     .. ok
    cmd( 7):
    echo "multple_render_var_level3->{{.multple_render_var_level3}}"
    
    cmd=>:
    echo "multple_render_var_level3->multple-render-var-> b2->{{.c3}}"
    -
    multple_render_var_level3->multple-render-var-> b2->{{.c3}}
    
    -
     .. ok
    cmd( 8):
    echo "multple_render_var_level4->{{.multple_render_var_level4}}"
    
    cmd=>:
    echo "multple_render_var_level4-><no value>"
    -
    multple_render_var_level4-><no value>
    
    -
     .. ok
    . ok
    
```

##### Logs with different verbose level
* [c0023 log - verbose level v](../../logs/c0023_v)
* [c0023 log - verbose level vv](../../logs/c0023_vv)
* [c0023 log - verbose level vvv](../../logs/c0023_vvv)
* [c0023 log - verbose level vvvv](../../logs/c0023_vvvv)
* [c0023 log - verbose level vvvvv](../../logs/c0023_vvvvv)

##### References
* [Related Chapter](../../dvars/c0023)
