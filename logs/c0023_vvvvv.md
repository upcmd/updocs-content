---
title: "c0023_vvvvv"
date: 2020-07-01T15:34:23+77:00
draft: false
weight: 10234

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
                 Verbose -> vvvvv
              ModuleName -> sharp_cray5
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0023
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001ef060)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [sharp_cray5] instance id: [dev]
    merged[ dev ] runtime vars:
    {
      "b2": "b2->{{.c3}}",
      "c3": "c3->{{.d4}}",
      "d4": "d4->{{.student}}",
      "student": "Tom",
      "gender": "Male",
      "school": "Sydney Grammar",
      "a1": "a1->{{.b2}}"
    }
    
    (core.Cache) (len=7) {
     (string) (len=2) "a1": (string) (len=11) "a1->{{.b2}}",
     (string) (len=2) "b2": (string) (len=11) "b2->{{.c3}}",
     (string) (len=2) "c3": (string) (len=11) "c3->{{.d4}}",
     (string) (len=2) "d4": (string) (len=16) "d4->{{.student}}",
     (string) (len=7) "student": (string) (len=3) "Tom",
     (string) (len=6) "gender": (string) (len=4) "Male",
     (string) (len=6) "school": (string) (len=14) "Sydney Grammar"
    }
    
    [runtime global] dvar expanded result:
    {
      "multple_render_var_level3_with_expand2": "multple-render-var-> b2->c3->{{.d4}}",
      "multple_render_var_level3_with_expand3": "multple-render-var-> b2->c3->d4->{{.student}}",
      "multple_render_var_level3_with_expand4": "multple-render-var-> b2->c3->d4->Tom",
      "from": "Sydney Grammar",
      "sex": "Male",
      "dependon_vars": "Male",
      "dependon_var_and_dvar": "Tom-Male",
      "multple_render_var_level3": "multple-render-var-> b2->{{.c3}}",
      "multple_render_var_level5": "multple-render-var-> a1->b2->c3->d4->Tom"
    }
    
    
    -------runtime global final merged with dvars-------
    
    {
      "multple_render_var_level3": "multple-render-var-> b2->{{.c3}}",
      "multple_render_var_level5": "multple-render-var-> a1->b2->c3->d4->Tom",
      "c3": "c3->{{.d4}}",
      "gender": "Male",
      "b2": "b2->{{.c3}}",
      "dependon_var_and_dvar": "Tom-Male",
      "from": "Sydney Grammar",
      "multple_render_var_level3_with_expand4": "multple-render-var-> b2->c3->d4->Tom",
      "d4": "d4->{{.student}}",
      "student": "Tom",
      "dependon_vars": "Male",
      "multple_render_var_level3_with_expand2": "multple-render-var-> b2->c3->{{.d4}}",
      "multple_render_var_level3_with_expand3": "multple-render-var-> b2->c3->d4->{{.student}}",
      "school": "Sydney Grammar",
      "a1": "a1->{{.b2}}",
      "sex": "Male"
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
      "from": "Sydney Grammar",
      "multple_render_var_level3_with_expand2": "multple-render-var-> b2->c3->{{.d4}}",
      "a1": "a1->{{.b2}}",
      "dependon_var_and_dvar": "Tom-Male",
      "dependon_vars": "Male",
      "sex": "Male",
      "gender": "Male",
      "b2": "b2->{{.c3}}",
      "d4": "d4->{{.student}}",
      "multple_render_var_level3_with_expand3": "multple-render-var-> b2->c3->d4->{{.student}}",
      "multple_render_var_level3_with_expand4": "multple-render-var-> b2->c3->d4->Tom",
      "school": "Sydney Grammar",
      "multple_render_var_level5": "multple-render-var-> a1->b2->c3->d4->Tom",
      "c3": "c3->{{.d4}}",
      "multple_render_var_level3": "multple-render-var-> b2->{{.c3}}",
      "student": "Tom"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "dependon_var_and_dvar": "Tom-Male",
      "multple_render_var_level3_with_expand3": "multple-render-var-> b2->c3->d4->{{.student}}",
      "c3": "c3->{{.d4}}",
      "from": "Sydney Grammar",
      "a1": "a1->{{.b2}}",
      "gender": "Male",
      "multple_render_var_level3_with_expand4": "multple-render-var-> b2->c3->d4->Tom",
      "school": "Sydney Grammar",
      "student": "Tom",
      "dependon_vars": "Male",
      "sex": "Male",
      "b2": "b2->{{.c3}}",
      "d4": "d4->{{.student}}",
      "multple_render_var_level3": "multple-render-var-> b2->{{.c3}}",
      "multple_render_var_level3_with_expand2": "multple-render-var-> b2->c3->{{.d4}}",
      "multple_render_var_level5": "multple-render-var-> a1->b2->c3->d4->Tom"
    }
    
    
    sharp_cray5: overall final exec vars:
    
    (*core.Cache)({
      "multple_render_var_level3_with_expand2": "multple-render-var-> b2->c3->{{.d4}}",
      "multple_render_var_level5": "multple-render-var-> a1->b2->c3->d4->Tom",
      "c3": "c3->{{.d4}}",
      "dependon_var_and_dvar": "Tom-Male",
      "multple_render_var_level3_with_expand3": "multple-render-var-> b2->c3->d4->{{.student}}",
      "gender": "Male",
      "multple_render_var_level3_with_expand4": "multple-render-var-> b2->c3->d4->Tom",
      "school": "Sydney Grammar",
      "student": "Tom",
      "from": "Sydney Grammar",
      "a1": "a1->{{.b2}}",
      "b2": "b2->{{.c3}}",
      "d4": "d4->{{.student}}",
      "multple_render_var_level3": "multple-render-var-> b2->{{.c3}}",
      "dependon_vars": "Male",
      "sex": "Male"
    })
    
    cmd( 1):
    echo "student=>{{.student}}"
    
     \_ echo "student=>Tom"
    student=>Tom
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=12) "student=>Tom",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    echo "a1=> a1->{{.b2}}"
    
     \_ echo "a1=> a1->b2->{{.c3}}"
    a1=> a1->b2->{{.c3}}
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=20) "a1=> a1->b2->{{.c3}}",
     ErrMsg: (string) ""
    }
    
    cmd( 3):
    echo "from->{{.from}}"
    
     \_ echo "from->Sydney Grammar"
    from->Sydney Grammar
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=20) "from->Sydney Grammar",
     ErrMsg: (string) ""
    }
    
    cmd( 4):
    echo "sex->{{.sex}}"
    
     \_ echo "sex->Male"
    sex->Male
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=9) "sex->Male",
     ErrMsg: (string) ""
    }
    
    cmd( 5):
    echo "dependon_vars->{{.dependon_vars}}"
    
     \_ echo "dependon_vars->Male"
    dependon_vars->Male
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=19) "dependon_vars->Male",
     ErrMsg: (string) ""
    }
    
    cmd( 6):
    echo "dependon_var_and_dvar->{{.dependon_var_and_dvar}}"
    
     \_ echo "dependon_var_and_dvar->Tom-Male"
    dependon_var_and_dvar->Tom-Male
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=31) "dependon_var_and_dvar->Tom-Male",
     ErrMsg: (string) ""
    }
    
    cmd( 7):
    echo "multple_render_var_level3->{{.multple_render_var_level3}}"
    
     \_ echo "multple_render_var_level3->multple-render-var-> b2->{{.c3}}"
    multple_render_var_level3->multple-render-var-> b2->{{.c3}}
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=59) "multple_render_var_level3->multple-render-var-> b2->{{.c3}}",
     ErrMsg: (string) ""
    }
    
    cmd( 8):
    echo "multple_render_var_level4->{{.multple_render_var_level4}}"
    
     \_ echo "multple_render_var_level4-><no value>"
    multple_render_var_level4-><no value>
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=37) "multple_render_var_level4-><no value>",
     ErrMsg: (string) ""
    }
    
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
