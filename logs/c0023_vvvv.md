---
title: "c0023_vvvv"
date: 2020-06-25T01:55:40+66:00
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
              ModuleName -> serene_curie8
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0023
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [serene_curie8] instance id: [dev]
    merged[ dev ] runtime vars:
    {
      "a1": "a1->{{.b2}}",
      "b2": "b2->{{.c3}}",
      "c3": "c3->{{.d4}}",
      "d4": "d4->{{.student}}",
      "student": "Tom",
      "gender": "Male",
      "school": "Sydney Grammar"
    }
    
    -------runtime global final merged with dvars-------
    
    {
      "c3": "c3->{{.d4}}",
      "gender": "Male",
      "from": "Sydney Grammar",
      "dependon_var_and_dvar": "Tom-Male",
      "multple_render_var_level5": "multple-render-var-> a1->b2->c3->d4->Tom",
      "multple_render_var_level3_with_expand2": "multple-render-var-> b2->c3->{{.d4}}",
      "multple_render_var_level3_with_expand4": "multple-render-var-> b2->c3->d4->Tom",
      "school": "Sydney Grammar",
      "a1": "a1->{{.b2}}",
      "b2": "b2->{{.c3}}",
      "d4": "d4->{{.student}}",
      "student": "Tom",
      "sex": "Male",
      "dependon_vars": "Male",
      "multple_render_var_level3": "multple-render-var-> b2->{{.c3}}",
      "multple_render_var_level3_with_expand3": "multple-render-var-> b2->c3->d4->{{.student}}"
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    {
      Name: "",
      Do: {
        "echo \"student=>{{.student}}\"",
        "echo \"a1=> a1->{{.b2}}\"",
        "echo \"from->{{.from}}\"",
        "echo \"sex->{{.sex}}\"",
        "echo \"dependon_vars->{{.dependon_vars}}\"",
        "echo \"dependon_var_and_dvar->{{.dependon_var_and_dvar}}\"",
        "echo \"multple_render_var_level3->{{.multple_render_var_level3}}\"",
        "echo \"multple_render_var_level4->{{.multple_render_var_level4}}\""
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
      "multple_render_var_level3_with_expand2": "multple-render-var-> b2->c3->{{.d4}}",
      "sex": "Male",
      "dependon_vars": "Male",
      "b2": "b2->{{.c3}}",
      "d4": "d4->{{.student}}",
      "student": "Tom",
      "multple_render_var_level5": "multple-render-var-> a1->b2->c3->d4->Tom",
      "gender": "Male",
      "multple_render_var_level3_with_expand4": "multple-render-var-> b2->c3->d4->Tom",
      "c3": "c3->{{.d4}}",
      "from": "Sydney Grammar",
      "multple_render_var_level3_with_expand3": "multple-render-var-> b2->c3->d4->{{.student}}",
      "multple_render_var_level3": "multple-render-var-> b2->{{.c3}}",
      "dependon_var_and_dvar": "Tom-Male",
      "school": "Sydney Grammar",
      "a1": "a1->{{.b2}}"
    })
    
    serene_curie8: overall final exec vars:
    
    (*core.Cache)({
      "multple_render_var_level3_with_expand2": "multple-render-var-> b2->c3->{{.d4}}",
      "dependon_vars": "Male",
      "b2": "b2->{{.c3}}",
      "gender": "Male",
      "a1": "a1->{{.b2}}",
      "d4": "d4->{{.student}}",
      "student": "Tom",
      "multple_render_var_level5": "multple-render-var-> a1->b2->c3->d4->Tom",
      "multple_render_var_level3_with_expand4": "multple-render-var-> b2->c3->d4->Tom",
      "multple_render_var_level3_with_expand3": "multple-render-var-> b2->c3->d4->{{.student}}",
      "dependon_var_and_dvar": "Tom-Male",
      "sex": "Male",
      "multple_render_var_level3": "multple-render-var-> b2->{{.c3}}",
      "school": "Sydney Grammar",
      "c3": "c3->{{.d4}}",
      "from": "Sydney Grammar"
    })
    
    cmd( 1):
    echo "student=>{{.student}}"
    
     \_ echo "student=>Tom"
    student=>Tom
     .. ok
    cmd( 2):
    echo "a1=> a1->{{.b2}}"
    
     \_ echo "a1=> a1->b2->{{.c3}}"
    a1=> a1->b2->{{.c3}}
     .. ok
    cmd( 3):
    echo "from->{{.from}}"
    
     \_ echo "from->Sydney Grammar"
    from->Sydney Grammar
     .. ok
    cmd( 4):
    echo "sex->{{.sex}}"
    
     \_ echo "sex->Male"
    sex->Male
     .. ok
    cmd( 5):
    echo "dependon_vars->{{.dependon_vars}}"
    
     \_ echo "dependon_vars->Male"
    dependon_vars->Male
     .. ok
    cmd( 6):
    echo "dependon_var_and_dvar->{{.dependon_var_and_dvar}}"
    
     \_ echo "dependon_var_and_dvar->Tom-Male"
    dependon_var_and_dvar->Tom-Male
     .. ok
    cmd( 7):
    echo "multple_render_var_level3->{{.multple_render_var_level3}}"
    
     \_ echo "multple_render_var_level3->multple-render-var-> b2->{{.c3}}"
    multple_render_var_level3->multple-render-var-> b2->{{.c3}}
     .. ok
    cmd( 8):
    echo "multple_render_var_level4->{{.multple_render_var_level4}}"
    
     \_ echo "multple_render_var_level4-><no value>"
    multple_render_var_level4-><no value>
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
