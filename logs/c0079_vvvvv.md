---
title: "c0079_vvvvv"
date: 2020-06-25T01:55:50+66:00
draft: false
weight: 10794

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0079
                 Verbose -> vvvvv
              ModuleName -> stupefied_mayer5
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0079
    -------full vars in scopes------
    (*impl.Scopes)(0xc0001c7a60)(<nil>)
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [stupefied_mayer5] instance id: [dev]
    merged[ dev ] runtime vars:
    {
      "complex_data_structure_template": "school:\n  name: '{{.school_name}}'\n  address: '{{.school_address}}'\nprincipals:\n{{- range $_, $p :=.schoo_principals }}\n  - {{$p}}\n{{- end}}\nranking: '{{.schoo_ranking}}'\n"
    }
    
    (core.Cache) (len=1) {
     (string) (len=31) "complex_data_structure_template": (string) (len=171) "school:\n  name: '{{.school_name}}'\n  address: '{{.school_address}}'\nprincipals:\n{{- range $_, $p :=.schoo_principals }}\n  - {{$p}}\n{{- end}}\nranking: '{{.schoo_ranking}}'\n"
    }
    
    [runtime global] dvar expanded result:
    {
      "intest": "false"
    }
    
    
    -------runtime global final merged with dvars-------
    
    {
      "complex_data_structure_template": "school:\n  name: '{{.school_name}}'\n  address: '{{.school_address}}'\nprincipals:\n{{- range $_, $p :=.schoo_principals }}\n  - {{$p}}\n{{- end}}\nranking: '{{.schoo_ranking}}'\n",
      "intest": "false"
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    {
      Name: "",
      Do: {
        {
          "cmd": "{{.school_string}}",
          "name": "print"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: {
        "school_name": "sydney grammar",
        "school_address": "1 fox road, sydney, nsw 2000",
        "schoo_principals": {
          "peter",
          "tom",
          "jane"
        },
        "schoo_ranking": "No 5"
      },
      Dvars: {
        {
          Name: "school_string",
          Value: "{{.complex_data_structure_template}}",
          Desc: "use default expand == 1",
          Expand: 0,
          Flags: <nil>,
          Rendered: "",
          Secure: (*utils.SecureSetting)(<nil>),
          Ref: "",
          RefDir: "",
          DataKey: "",
          DataPath: "",
          DataTemplate: ""
        }
      },
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
      "intest": "false",
      "school_name": "sydney grammar",
      "school_address": "1 fox road, sydney, nsw 2000",
      "schoo_principals": {
        "peter",
        "tom",
        "jane"
      },
      "schoo_ranking": "No 5",
      "complex_data_structure_template": "school:\n  name: '{{.school_name}}'\n  address: '{{.school_address}}'\nprincipals:\n{{- range $_, $p :=.schoo_principals }}\n  - {{$p}}\n{{- end}}\nranking: '{{.schoo_ranking}}'\n"
    })
    
    [local] dvar expanded result:
    {
      "school_string": "school:\n  name: '{{.school_name}}'\n  address: '{{.school_address}}'\nprincipals:\n{{- range $_, $p :=.schoo_principals }}\n  - {{$p}}\n{{- end}}\nranking: '{{.schoo_ranking}}'\n"
    }
    
    
    scope[local] merged: {
      "complex_data_structure_template": "school:\n  name: '{{.school_name}}'\n  address: '{{.school_address}}'\nprincipals:\n{{- range $_, $p :=.schoo_principals }}\n  - {{$p}}\n{{- end}}\nranking: '{{.schoo_ranking}}'\n",
      "intest": "false",
      "school_name": "sydney grammar",
      "school_address": "1 fox road, sydney, nsw 2000",
      "schoo_principals": {
        "peter",
        "tom",
        "jane"
      },
      "schoo_ranking": "No 5",
      "school_string": "school:\n  name: '{{.school_name}}'\n  address: '{{.school_address}}'\nprincipals:\n{{- range $_, $p :=.schoo_principals }}\n  - {{$p}}\n{{- end}}\nranking: '{{.schoo_ranking}}'\n"
    }
    
    
    stupefied_mayer5: overall final exec vars:
    
    (*core.Cache)({
      "school_name": "sydney grammar",
      "school_address": "1 fox road, sydney, nsw 2000",
      "schoo_principals": {
        "peter",
        "tom",
        "jane"
      },
      "schoo_ranking": "No 5",
      "school_string": "school:\n  name: '{{.school_name}}'\n  address: '{{.school_address}}'\nprincipals:\n{{- range $_, $p :=.schoo_principals }}\n  - {{$p}}\n{{- end}}\nranking: '{{.schoo_ranking}}'\n",
      "complex_data_structure_template": "school:\n  name: '{{.school_name}}'\n  address: '{{.school_address}}'\nprincipals:\n{{- range $_, $p :=.schoo_principals }}\n  - {{$p}}\n{{- end}}\nranking: '{{.schoo_ranking}}'\n",
      "intest": "false"
    })
    
    {{.school_string}}
    ~SubStep1: [print:  ]
    school:
      name: '{{.school_name}}'
      address: '{{.school_address}}'
    principals:
    {{- range $_, $p :=.schoo_principals }}
      - {{$p}}
    {{- end}}
    ranking: '{{.schoo_ranking}}'
    
    -Step2:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "{{.school_yml}}"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: {
        "school_name": "sydney grammar",
        "school_address": "1 fox road, sydney, nsw 2000",
        "schoo_principals": {
          "peter",
          "tom",
          "jane"
        },
        "schoo_ranking": "No 5"
      },
      Dvars: {
        {
          Name: "school_yml",
          Value: "{{.complex_data_structure_template}}",
          Desc: "use dynamic expand == 2, so that the template will be rendered",
          Expand: 2,
          Flags: {
            "reg"
          },
          Rendered: "",
          Secure: (*utils.SecureSetting)(<nil>),
          Ref: "",
          RefDir: "",
          DataKey: "",
          DataPath: "",
          DataTemplate: ""
        }
      },
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
      "school_address": "1 fox road, sydney, nsw 2000",
      "schoo_principals": {
        "peter",
        "tom",
        "jane"
      },
      "schoo_ranking": "No 5",
      "intest": "false",
      "complex_data_structure_template": "school:\n  name: '{{.school_name}}'\n  address: '{{.school_address}}'\nprincipals:\n{{- range $_, $p :=.schoo_principals }}\n  - {{$p}}\n{{- end}}\nranking: '{{.schoo_ranking}}'\n",
      "school_name": "sydney grammar"
    })
    
    [local] dvar expanded result:
    {
      "school_yml": "school:\n  name: 'sydney grammar'\n  address: '1 fox road, sydney, nsw 2000'\nprincipals:\n  - peter\n  - tom\n  - jane\nranking: 'No 5'\n"
    }
    
    
    scope[local] merged: {
      "school_address": "1 fox road, sydney, nsw 2000",
      "schoo_principals": {
        "peter",
        "tom",
        "jane"
      },
      "schoo_ranking": "No 5",
      "intest": "false",
      "school_yml": "school:\n  name: 'sydney grammar'\n  address: '1 fox road, sydney, nsw 2000'\nprincipals:\n  - peter\n  - tom\n  - jane\nranking: 'No 5'\n",
      "complex_data_structure_template": "school:\n  name: '{{.school_name}}'\n  address: '{{.school_address}}'\nprincipals:\n{{- range $_, $p :=.schoo_principals }}\n  - {{$p}}\n{{- end}}\nranking: '{{.schoo_ranking}}'\n",
      "school_name": "sydney grammar"
    }
    
    
    stupefied_mayer5: overall final exec vars:
    
    (*core.Cache)({
      "school_address": "1 fox road, sydney, nsw 2000",
      "schoo_principals": {
        "peter",
        "tom",
        "jane"
      },
      "schoo_ranking": "No 5",
      "intest": "false",
      "school_yml": "school:\n  name: 'sydney grammar'\n  address: '1 fox road, sydney, nsw 2000'\nprincipals:\n  - peter\n  - tom\n  - jane\nranking: 'No 5'\n",
      "complex_data_structure_template": "school:\n  name: '{{.school_name}}'\n  address: '{{.school_address}}'\nprincipals:\n{{- range $_, $p :=.schoo_principals }}\n  - {{$p}}\n{{- end}}\nranking: '{{.schoo_ranking}}'\n",
      "school_name": "sydney grammar"
    })
    
    {{.school_yml}}
    ~SubStep1: [print:  ]
    school:
      name: 'sydney grammar'
      address: '1 fox road, sydney, nsw 2000'
    principals:
      - peter
      - tom
      - jane
    ranking: 'No 5'
    
    -Step3: [: show global school_yml var
    convert the yml to object so that it could be used in template later
     ]
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "{{.school_yml}}"
        },
        {
          "name": "printobj",
          "cmd": "school_details"
        },
        {
          "name": "print",
          "cmd": "{{.school_details}}"
        },
        {
          "name": "printobj",
          "cmd": "school_details_object"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: {
        {
          Name: "school_details",
          Value: "{{.school_yml}}",
          Desc: "use dynamic expand == 2, so that the template will be rendered",
          Expand: 0,
          Flags: {
            "vvv",
            "to_object",
            "reg"
          },
          Rendered: "",
          Secure: (*utils.SecureSetting)(<nil>),
          Ref: "",
          RefDir: "",
          DataKey: "",
          DataPath: "",
          DataTemplate: ""
        }
      },
      Desc: "show global school_yml var\nconvert the yml to object so that it could be used in template later\n",
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
      "complex_data_structure_template": "school:\n  name: '{{.school_name}}'\n  address: '{{.school_address}}'\nprincipals:\n{{- range $_, $p :=.schoo_principals }}\n  - {{$p}}\n{{- end}}\nranking: '{{.schoo_ranking}}'\n",
      "intest": "false",
      "school_yml": "school:\n  name: 'sydney grammar'\n  address: '1 fox road, sydney, nsw 2000'\nprincipals:\n  - peter\n  - tom\n  - jane\nranking: 'No 5'\n"
    })
    
    dvar> school_details:
    "school:\n  name: 'sydney grammar'\n  address: '1 fox road, sydney, nsw 2000'\nprincipals:\n  - peter\n  - tom\n  - jane\nranking: 'No 5'\n"
    
    dvar> school_details_object:
    {
      "school": {
        "name": "sydney grammar",
        "address": "1 fox road, sydney, nsw 2000"
      },
      "principals": {
        "peter",
        "tom",
        "jane"
      },
      "ranking": "No 5"
    }
    
    [local] dvar expanded result:
    {
      "school_details": "school:\n  name: 'sydney grammar'\n  address: '1 fox road, sydney, nsw 2000'\nprincipals:\n  - peter\n  - tom\n  - jane\nranking: 'No 5'\n",
      "school_details_object": {
        "ranking": "No 5",
        "school": {
          "name": "sydney grammar",
          "address": "1 fox road, sydney, nsw 2000"
        },
        "principals": {
          "peter",
          "tom",
          "jane"
        }
      }
    }
    
    
    scope[local] merged: {
      "school_details": "school:\n  name: 'sydney grammar'\n  address: '1 fox road, sydney, nsw 2000'\nprincipals:\n  - peter\n  - tom\n  - jane\nranking: 'No 5'\n",
      "school_details_object": {
        "school": {
          "name": "sydney grammar",
          "address": "1 fox road, sydney, nsw 2000"
        },
        "principals": {
          "peter",
          "tom",
          "jane"
        },
        "ranking": "No 5"
      },
      "complex_data_structure_template": "school:\n  name: '{{.school_name}}'\n  address: '{{.school_address}}'\nprincipals:\n{{- range $_, $p :=.schoo_principals }}\n  - {{$p}}\n{{- end}}\nranking: '{{.schoo_ranking}}'\n",
      "intest": "false",
      "school_yml": "school:\n  name: 'sydney grammar'\n  address: '1 fox road, sydney, nsw 2000'\nprincipals:\n  - peter\n  - tom\n  - jane\nranking: 'No 5'\n"
    }
    
    
    stupefied_mayer5: overall final exec vars:
    
    (*core.Cache)({
      "intest": "false",
      "school_yml": "school:\n  name: 'sydney grammar'\n  address: '1 fox road, sydney, nsw 2000'\nprincipals:\n  - peter\n  - tom\n  - jane\nranking: 'No 5'\n",
      "school_details": "school:\n  name: 'sydney grammar'\n  address: '1 fox road, sydney, nsw 2000'\nprincipals:\n  - peter\n  - tom\n  - jane\nranking: 'No 5'\n",
      "school_details_object": {
        "principals": {
          "peter",
          "tom",
          "jane"
        },
        "ranking": "No 5",
        "school": {
          "name": "sydney grammar",
          "address": "1 fox road, sydney, nsw 2000"
        }
      },
      "complex_data_structure_template": "school:\n  name: '{{.school_name}}'\n  address: '{{.school_address}}'\nprincipals:\n{{- range $_, $p :=.schoo_principals }}\n  - {{$p}}\n{{- end}}\nranking: '{{.schoo_ranking}}'\n"
    })
    
    {{.school_yml}}
    ~SubStep1: [print:  ]
    school:
      name: 'sydney grammar'
      address: '1 fox road, sydney, nsw 2000'
    principals:
      - peter
      - tom
      - jane
    ranking: 'No 5'
    
    school_details
    ~SubStep2: [printobj:  ]
    (string) (len=14) "school_details"
    
    object:
     school_details: "school:\n  name: 'sydney grammar'\n  address: '1 fox road, sydney, nsw 2000'\nprincipals:\n  - peter\n  - tom\n  - jane\nranking: 'No 5'\n"
    
    {{.school_details}}
    ~SubStep3: [print:  ]
    school:
      name: 'sydney grammar'
      address: '1 fox road, sydney, nsw 2000'
    principals:
      - peter
      - tom
      - jane
    ranking: 'No 5'
    
    school_details_object
    ~SubStep4: [printobj:  ]
    (string) (len=21) "school_details_object"
    
    object:
     school_details_object: {
      "ranking": "No 5",
      "school": {
        "name": "sydney grammar",
        "address": "1 fox road, sydney, nsw 2000"
      },
      "principals": {
        "peter",
        "tom",
        "jane"
      }
    }
    
    -Step4:
    {
      Name: "",
      Do: {
        "echo \"?intest ->  {{.intest}}\"",
        "pwd"
      },
      Dox: <nil>,
      Func: "shell",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "",
      Reg: "register_task_root",
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
      "school_details": "school:\n  name: 'sydney grammar'\n  address: '1 fox road, sydney, nsw 2000'\nprincipals:\n  - peter\n  - tom\n  - jane\nranking: 'No 5'\n",
      "complex_data_structure_template": "school:\n  name: '{{.school_name}}'\n  address: '{{.school_address}}'\nprincipals:\n{{- range $_, $p :=.schoo_principals }}\n  - {{$p}}\n{{- end}}\nranking: '{{.schoo_ranking}}'\n",
      "intest": "false",
      "school_yml": "school:\n  name: 'sydney grammar'\n  address: '1 fox road, sydney, nsw 2000'\nprincipals:\n  - peter\n  - tom\n  - jane\nranking: 'No 5'\n",
      "school_details_object": {
        "principals": {
          "peter",
          "tom",
          "jane"
        },
        "ranking": "No 5",
        "school": {
          "name": "sydney grammar",
          "address": "1 fox road, sydney, nsw 2000"
        }
      }
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "complex_data_structure_template": "school:\n  name: '{{.school_name}}'\n  address: '{{.school_address}}'\nprincipals:\n{{- range $_, $p :=.schoo_principals }}\n  - {{$p}}\n{{- end}}\nranking: '{{.schoo_ranking}}'\n",
      "intest": "false",
      "school_yml": "school:\n  name: 'sydney grammar'\n  address: '1 fox road, sydney, nsw 2000'\nprincipals:\n  - peter\n  - tom\n  - jane\nranking: 'No 5'\n",
      "school_details_object": {
        "ranking": "No 5",
        "school": {
          "name": "sydney grammar",
          "address": "1 fox road, sydney, nsw 2000"
        },
        "principals": {
          "peter",
          "tom",
          "jane"
        }
      },
      "school_details": "school:\n  name: 'sydney grammar'\n  address: '1 fox road, sydney, nsw 2000'\nprincipals:\n  - peter\n  - tom\n  - jane\nranking: 'No 5'\n"
    }
    
    
    stupefied_mayer5: overall final exec vars:
    
    (*core.Cache)({
      "complex_data_structure_template": "school:\n  name: '{{.school_name}}'\n  address: '{{.school_address}}'\nprincipals:\n{{- range $_, $p :=.schoo_principals }}\n  - {{$p}}\n{{- end}}\nranking: '{{.schoo_ranking}}'\n",
      "intest": "false",
      "school_yml": "school:\n  name: 'sydney grammar'\n  address: '1 fox road, sydney, nsw 2000'\nprincipals:\n  - peter\n  - tom\n  - jane\nranking: 'No 5'\n",
      "school_details_object": {
        "principals": {
          "peter",
          "tom",
          "jane"
        },
        "ranking": "No 5",
        "school": {
          "name": "sydney grammar",
          "address": "1 fox road, sydney, nsw 2000"
        }
      },
      "school_details": "school:\n  name: 'sydney grammar'\n  address: '1 fox road, sydney, nsw 2000'\nprincipals:\n  - peter\n  - tom\n  - jane\nranking: 'No 5'\n"
    })
    
    cmd( 1):
    echo "?intest ->  {{.intest}}"
    
     \_ echo "?intest ->  false"
    ?intest ->  false
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=17) "?intest ->  false",
     ErrMsg: (string) ""
    }
    
    cmd( 2):
    pwd
    
     \_ pwd
    /up_project/up
     .. ok
    (utils.ExecResult) {
     Code: (int) 0,
     Output: (string) (len=14) "/up_project/up",
     ErrMsg: (string) ""
    }
    
    . ok
    -Step5:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "intest is: [{{.intest}}]"
        },
        {
          "name": "reg",
          "cmd": {
            "value": "{{if eq .intest \"true\" }}{{.register_task_root.Output}}{{else}}{{.register_task_root.Output}}{{end}}",
            "name": "correct_working_dir",
            "desc": "the value of .intest is string but not bool so you can not simple use if .intest for condition"
          }
        }
      },
      Dox: <nil>,
      Func: "cmd",
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
      "school_yml": "school:\n  name: 'sydney grammar'\n  address: '1 fox road, sydney, nsw 2000'\nprincipals:\n  - peter\n  - tom\n  - jane\nranking: 'No 5'\n",
      "school_details_object": {
        "ranking": "No 5",
        "school": {
          "name": "sydney grammar",
          "address": "1 fox road, sydney, nsw 2000"
        },
        "principals": {
          "peter",
          "tom",
          "jane"
        }
      },
      "school_details": "school:\n  name: 'sydney grammar'\n  address: '1 fox road, sydney, nsw 2000'\nprincipals:\n  - peter\n  - tom\n  - jane\nranking: 'No 5'\n",
      "register_task_root": (*utils.ExecResult)({
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "complex_data_structure_template": "school:\n  name: '{{.school_name}}'\n  address: '{{.school_address}}'\nprincipals:\n{{- range $_, $p :=.schoo_principals }}\n  - {{$p}}\n{{- end}}\nranking: '{{.schoo_ranking}}'\n",
      "intest": "false"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "school_yml": "school:\n  name: 'sydney grammar'\n  address: '1 fox road, sydney, nsw 2000'\nprincipals:\n  - peter\n  - tom\n  - jane\nranking: 'No 5'\n",
      "school_details_object": {
        "ranking": "No 5",
        "school": {
          "name": "sydney grammar",
          "address": "1 fox road, sydney, nsw 2000"
        },
        "principals": {
          "peter",
          "tom",
          "jane"
        }
      },
      "school_details": "school:\n  name: 'sydney grammar'\n  address: '1 fox road, sydney, nsw 2000'\nprincipals:\n  - peter\n  - tom\n  - jane\nranking: 'No 5'\n",
      "register_task_root": (*utils.ExecResult)({
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "complex_data_structure_template": "school:\n  name: '{{.school_name}}'\n  address: '{{.school_address}}'\nprincipals:\n{{- range $_, $p :=.schoo_principals }}\n  - {{$p}}\n{{- end}}\nranking: '{{.schoo_ranking}}'\n",
      "intest": "false"
    }
    
    
    stupefied_mayer5: overall final exec vars:
    
    (*core.Cache)({
      "school_details_object": {
        "ranking": "No 5",
        "school": {
          "name": "sydney grammar",
          "address": "1 fox road, sydney, nsw 2000"
        },
        "principals": {
          "peter",
          "tom",
          "jane"
        }
      },
      "school_details": "school:\n  name: 'sydney grammar'\n  address: '1 fox road, sydney, nsw 2000'\nprincipals:\n  - peter\n  - tom\n  - jane\nranking: 'No 5'\n",
      "register_task_root": (*utils.ExecResult)({
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "complex_data_structure_template": "school:\n  name: '{{.school_name}}'\n  address: '{{.school_address}}'\nprincipals:\n{{- range $_, $p :=.schoo_principals }}\n  - {{$p}}\n{{- end}}\nranking: '{{.schoo_ranking}}'\n",
      "intest": "false",
      "school_yml": "school:\n  name: 'sydney grammar'\n  address: '1 fox road, sydney, nsw 2000'\nprincipals:\n  - peter\n  - tom\n  - jane\nranking: 'No 5'\n"
    })
    
    intest is: [{{.intest}}]
    ~SubStep1: [print:  ]
    intest is: [false]
    map[desc:the value of .intest is string but not bool so you can not simple use if .intest for condition name:correct_working_dir value:{{if eq .intest "true" }}{{.register_task_root.Output}}{{else}}{{.register_task_root.Output}}{{end}}]
    ~SubStep2: [reg:  ]
    after reg the var - contextual global:
    
    (*core.Cache)({
      "complex_data_structure_template": "school:\n  name: '{{.school_name}}'\n  address: '{{.school_address}}'\nprincipals:\n{{- range $_, $p :=.schoo_principals }}\n  - {{$p}}\n{{- end}}\nranking: '{{.schoo_ranking}}'\n",
      "intest": "false",
      "school_yml": "school:\n  name: 'sydney grammar'\n  address: '1 fox road, sydney, nsw 2000'\nprincipals:\n  - peter\n  - tom\n  - jane\nranking: 'No 5'\n",
      "school_details_object": {
        "school": {
          "name": "sydney grammar",
          "address": "1 fox road, sydney, nsw 2000"
        },
        "principals": {
          "peter",
          "tom",
          "jane"
        },
        "ranking": "No 5"
      },
      "school_details": "school:\n  name: 'sydney grammar'\n  address: '1 fox road, sydney, nsw 2000'\nprincipals:\n  - peter\n  - tom\n  - jane\nranking: 'No 5'\n",
      "register_task_root": (*utils.ExecResult)({
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "correct_working_dir": "/up_project/up"
    })
    
    after reg the var - local:
    
    (*core.Cache)({
      "complex_data_structure_template": "school:\n  name: '{{.school_name}}'\n  address: '{{.school_address}}'\nprincipals:\n{{- range $_, $p :=.schoo_principals }}\n  - {{$p}}\n{{- end}}\nranking: '{{.schoo_ranking}}'\n",
      "intest": "false",
      "school_yml": "school:\n  name: 'sydney grammar'\n  address: '1 fox road, sydney, nsw 2000'\nprincipals:\n  - peter\n  - tom\n  - jane\nranking: 'No 5'\n",
      "correct_working_dir": "/up_project/up",
      "school_details_object": {
        "ranking": "No 5",
        "school": {
          "name": "sydney grammar",
          "address": "1 fox road, sydney, nsw 2000"
        },
        "principals": {
          "peter",
          "tom",
          "jane"
        }
      },
      "school_details": "school:\n  name: 'sydney grammar'\n  address: '1 fox road, sydney, nsw 2000'\nprincipals:\n  - peter\n  - tom\n  - jane\nranking: 'No 5'\n",
      "register_task_root": (*utils.ExecResult)({
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      })
    })
    
    -Step6:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "root dir is: [{{.register_task_root.Output}}]"
        },
        {
          "name": "print",
          "cmd": "correct working dir is: [{{.correct_working_dir}}]"
        }
      },
      Dox: <nil>,
      Func: "cmd",
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
      "school_details_object": {
        "school": {
          "name": "sydney grammar",
          "address": "1 fox road, sydney, nsw 2000"
        },
        "principals": {
          "peter",
          "tom",
          "jane"
        },
        "ranking": "No 5"
      },
      "school_details": "school:\n  name: 'sydney grammar'\n  address: '1 fox road, sydney, nsw 2000'\nprincipals:\n  - peter\n  - tom\n  - jane\nranking: 'No 5'\n",
      "register_task_root": (*utils.ExecResult)({
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "correct_working_dir": "/up_project/up",
      "complex_data_structure_template": "school:\n  name: '{{.school_name}}'\n  address: '{{.school_address}}'\nprincipals:\n{{- range $_, $p :=.schoo_principals }}\n  - {{$p}}\n{{- end}}\nranking: '{{.schoo_ranking}}'\n",
      "intest": "false",
      "school_yml": "school:\n  name: 'sydney grammar'\n  address: '1 fox road, sydney, nsw 2000'\nprincipals:\n  - peter\n  - tom\n  - jane\nranking: 'No 5'\n"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "school_yml": "school:\n  name: 'sydney grammar'\n  address: '1 fox road, sydney, nsw 2000'\nprincipals:\n  - peter\n  - tom\n  - jane\nranking: 'No 5'\n",
      "school_details_object": {
        "school": {
          "name": "sydney grammar",
          "address": "1 fox road, sydney, nsw 2000"
        },
        "principals": {
          "peter",
          "tom",
          "jane"
        },
        "ranking": "No 5"
      },
      "school_details": "school:\n  name: 'sydney grammar'\n  address: '1 fox road, sydney, nsw 2000'\nprincipals:\n  - peter\n  - tom\n  - jane\nranking: 'No 5'\n",
      "register_task_root": (*utils.ExecResult)({
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "correct_working_dir": "/up_project/up",
      "complex_data_structure_template": "school:\n  name: '{{.school_name}}'\n  address: '{{.school_address}}'\nprincipals:\n{{- range $_, $p :=.schoo_principals }}\n  - {{$p}}\n{{- end}}\nranking: '{{.schoo_ranking}}'\n",
      "intest": "false"
    }
    
    
    stupefied_mayer5: overall final exec vars:
    
    (*core.Cache)({
      "register_task_root": (*utils.ExecResult)({
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "correct_working_dir": "/up_project/up",
      "complex_data_structure_template": "school:\n  name: '{{.school_name}}'\n  address: '{{.school_address}}'\nprincipals:\n{{- range $_, $p :=.schoo_principals }}\n  - {{$p}}\n{{- end}}\nranking: '{{.schoo_ranking}}'\n",
      "intest": "false",
      "school_yml": "school:\n  name: 'sydney grammar'\n  address: '1 fox road, sydney, nsw 2000'\nprincipals:\n  - peter\n  - tom\n  - jane\nranking: 'No 5'\n",
      "school_details_object": {
        "school": {
          "name": "sydney grammar",
          "address": "1 fox road, sydney, nsw 2000"
        },
        "principals": {
          "peter",
          "tom",
          "jane"
        },
        "ranking": "No 5"
      },
      "school_details": "school:\n  name: 'sydney grammar'\n  address: '1 fox road, sydney, nsw 2000'\nprincipals:\n  - peter\n  - tom\n  - jane\nranking: 'No 5'\n"
    })
    
    root dir is: [{{.register_task_root.Output}}]
    ~SubStep1: [print:  ]
    root dir is: [/up_project/up]
    correct working dir is: [{{.correct_working_dir}}]
    ~SubStep2: [print:  ]
    correct working dir is: [/up_project/up]
    -Step7: [: render final result using template ]
    {
      Name: "",
      Do: {
        {
          "name": "template",
          "desc": "render the template file using above dynamic variable from defined var",
          "cmd": {
            "src": "{{.correct_working_dir}}/tests/functests/d0079.template",
            "dest": "/tmp/myschool.txt",
            "datakey": "school_details_object"
          }
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: <nil>,
      Dvars: <nil>,
      Desc: "render final result using template",
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
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "correct_working_dir": "/up_project/up",
      "complex_data_structure_template": "school:\n  name: '{{.school_name}}'\n  address: '{{.school_address}}'\nprincipals:\n{{- range $_, $p :=.schoo_principals }}\n  - {{$p}}\n{{- end}}\nranking: '{{.schoo_ranking}}'\n",
      "intest": "false",
      "school_yml": "school:\n  name: 'sydney grammar'\n  address: '1 fox road, sydney, nsw 2000'\nprincipals:\n  - peter\n  - tom\n  - jane\nranking: 'No 5'\n",
      "school_details_object": {
        "principals": {
          "peter",
          "tom",
          "jane"
        },
        "ranking": "No 5",
        "school": {
          "name": "sydney grammar",
          "address": "1 fox road, sydney, nsw 2000"
        }
      },
      "school_details": "school:\n  name: 'sydney grammar'\n  address: '1 fox road, sydney, nsw 2000'\nprincipals:\n  - peter\n  - tom\n  - jane\nranking: 'No 5'\n",
      "register_task_root": (*utils.ExecResult)({
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      })
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "register_task_root": (*utils.ExecResult)({
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "correct_working_dir": "/up_project/up",
      "complex_data_structure_template": "school:\n  name: '{{.school_name}}'\n  address: '{{.school_address}}'\nprincipals:\n{{- range $_, $p :=.schoo_principals }}\n  - {{$p}}\n{{- end}}\nranking: '{{.schoo_ranking}}'\n",
      "intest": "false",
      "school_yml": "school:\n  name: 'sydney grammar'\n  address: '1 fox road, sydney, nsw 2000'\nprincipals:\n  - peter\n  - tom\n  - jane\nranking: 'No 5'\n",
      "school_details_object": {
        "principals": {
          "peter",
          "tom",
          "jane"
        },
        "ranking": "No 5",
        "school": {
          "address": "1 fox road, sydney, nsw 2000",
          "name": "sydney grammar"
        }
      },
      "school_details": "school:\n  name: 'sydney grammar'\n  address: '1 fox road, sydney, nsw 2000'\nprincipals:\n  - peter\n  - tom\n  - jane\nranking: 'No 5'\n"
    }
    
    
    stupefied_mayer5: overall final exec vars:
    
    (*core.Cache)({
      "register_task_root": (*utils.ExecResult)({
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "correct_working_dir": "/up_project/up",
      "complex_data_structure_template": "school:\n  name: '{{.school_name}}'\n  address: '{{.school_address}}'\nprincipals:\n{{- range $_, $p :=.schoo_principals }}\n  - {{$p}}\n{{- end}}\nranking: '{{.schoo_ranking}}'\n",
      "intest": "false",
      "school_yml": "school:\n  name: 'sydney grammar'\n  address: '1 fox road, sydney, nsw 2000'\nprincipals:\n  - peter\n  - tom\n  - jane\nranking: 'No 5'\n",
      "school_details_object": {
        "principals": {
          "peter",
          "tom",
          "jane"
        },
        "ranking": "No 5",
        "school": {
          "name": "sydney grammar",
          "address": "1 fox road, sydney, nsw 2000"
        }
      },
      "school_details": "school:\n  name: 'sydney grammar'\n  address: '1 fox road, sydney, nsw 2000'\nprincipals:\n  - peter\n  - tom\n  - jane\nranking: 'No 5'\n"
    })
    
    map[datakey:school_details_object dest:/tmp/myschool.txt src:{{.correct_working_dir}}/tests/functests/d0079.template]
    ~SubStep1: [template: render the template file using above dynamic variable from defined var ]
    -Step8:
    {
      Name: "",
      Do: {
        {
          "name": "readfile",
          "desc": "read content of a file and register it to a var",
          "cmd": {
            "filename": "myschool.txt",
            "dir": "/tmp",
            "reg": "my_school"
          }
        },
        {
          "name": "print",
          "cmd": "{{.my_school}}"
        }
      },
      Dox: <nil>,
      Func: "cmd",
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
      "register_task_root": (*utils.ExecResult)({
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "correct_working_dir": "/up_project/up",
      "complex_data_structure_template": "school:\n  name: '{{.school_name}}'\n  address: '{{.school_address}}'\nprincipals:\n{{- range $_, $p :=.schoo_principals }}\n  - {{$p}}\n{{- end}}\nranking: '{{.schoo_ranking}}'\n",
      "intest": "false",
      "school_yml": "school:\n  name: 'sydney grammar'\n  address: '1 fox road, sydney, nsw 2000'\nprincipals:\n  - peter\n  - tom\n  - jane\nranking: 'No 5'\n",
      "school_details_object": {
        "ranking": "No 5",
        "school": {
          "name": "sydney grammar",
          "address": "1 fox road, sydney, nsw 2000"
        },
        "principals": {
          "peter",
          "tom",
          "jane"
        }
      },
      "school_details": "school:\n  name: 'sydney grammar'\n  address: '1 fox road, sydney, nsw 2000'\nprincipals:\n  - peter\n  - tom\n  - jane\nranking: 'No 5'\n"
    })
    
    [local] dvar expanded result:
    {
    }
    
    
    scope[local] merged: {
      "school_details_object": {
        "principals": {
          "peter",
          "tom",
          "jane"
        },
        "ranking": "No 5",
        "school": {
          "name": "sydney grammar",
          "address": "1 fox road, sydney, nsw 2000"
        }
      },
      "school_details": "school:\n  name: 'sydney grammar'\n  address: '1 fox road, sydney, nsw 2000'\nprincipals:\n  - peter\n  - tom\n  - jane\nranking: 'No 5'\n",
      "register_task_root": (*utils.ExecResult)({
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "correct_working_dir": "/up_project/up",
      "complex_data_structure_template": "school:\n  name: '{{.school_name}}'\n  address: '{{.school_address}}'\nprincipals:\n{{- range $_, $p :=.schoo_principals }}\n  - {{$p}}\n{{- end}}\nranking: '{{.schoo_ranking}}'\n",
      "intest": "false",
      "school_yml": "school:\n  name: 'sydney grammar'\n  address: '1 fox road, sydney, nsw 2000'\nprincipals:\n  - peter\n  - tom\n  - jane\nranking: 'No 5'\n"
    }
    
    
    stupefied_mayer5: overall final exec vars:
    
    (*core.Cache)({
      "school_details_object": {
        "ranking": "No 5",
        "school": {
          "name": "sydney grammar",
          "address": "1 fox road, sydney, nsw 2000"
        },
        "principals": {
          "peter",
          "tom",
          "jane"
        }
      },
      "school_details": "school:\n  name: 'sydney grammar'\n  address: '1 fox road, sydney, nsw 2000'\nprincipals:\n  - peter\n  - tom\n  - jane\nranking: 'No 5'\n",
      "register_task_root": (*utils.ExecResult)({
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "correct_working_dir": "/up_project/up",
      "complex_data_structure_template": "school:\n  name: '{{.school_name}}'\n  address: '{{.school_address}}'\nprincipals:\n{{- range $_, $p :=.schoo_principals }}\n  - {{$p}}\n{{- end}}\nranking: '{{.schoo_ranking}}'\n",
      "intest": "false",
      "school_yml": "school:\n  name: 'sydney grammar'\n  address: '1 fox road, sydney, nsw 2000'\nprincipals:\n  - peter\n  - tom\n  - jane\nranking: 'No 5'\n"
    })
    
    map[dir:/tmp filename:myschool.txt reg:my_school]
    ~SubStep1: [readfile: read content of a file and register it to a var ]
    after reg the var - contextual global:
    
    (*core.Cache)({
      "intest": "false",
      "correct_working_dir": "/up_project/up",
      "my_school": "\n\nMy school name is: sydney grammar, it is located\nat 1 fox road, sydney, nsw 2000\n\n\nWe have got  peter,  tom,  jane,  as our principals\n\nOur school ranking last year is No 5\n",
      "school_details": "school:\n  name: 'sydney grammar'\n  address: '1 fox road, sydney, nsw 2000'\nprincipals:\n  - peter\n  - tom\n  - jane\nranking: 'No 5'\n",
      "register_task_root": (*utils.ExecResult)({
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "complex_data_structure_template": "school:\n  name: '{{.school_name}}'\n  address: '{{.school_address}}'\nprincipals:\n{{- range $_, $p :=.schoo_principals }}\n  - {{$p}}\n{{- end}}\nranking: '{{.schoo_ranking}}'\n",
      "school_yml": "school:\n  name: 'sydney grammar'\n  address: '1 fox road, sydney, nsw 2000'\nprincipals:\n  - peter\n  - tom\n  - jane\nranking: 'No 5'\n",
      "school_details_object": {
        "school": {
          "name": "sydney grammar",
          "address": "1 fox road, sydney, nsw 2000"
        },
        "principals": {
          "peter",
          "tom",
          "jane"
        },
        "ranking": "No 5"
      }
    })
    
    after reg the var - local:
    
    (*core.Cache)({
      "school_details": "school:\n  name: 'sydney grammar'\n  address: '1 fox road, sydney, nsw 2000'\nprincipals:\n  - peter\n  - tom\n  - jane\nranking: 'No 5'\n",
      "register_task_root": (*utils.ExecResult)({
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "complex_data_structure_template": "school:\n  name: '{{.school_name}}'\n  address: '{{.school_address}}'\nprincipals:\n{{- range $_, $p :=.schoo_principals }}\n  - {{$p}}\n{{- end}}\nranking: '{{.schoo_ranking}}'\n",
      "intest": "false",
      "my_school": "\n\nMy school name is: sydney grammar, it is located\nat 1 fox road, sydney, nsw 2000\n\n\nWe have got  peter,  tom,  jane,  as our principals\n\nOur school ranking last year is No 5\n",
      "school_yml": "school:\n  name: 'sydney grammar'\n  address: '1 fox road, sydney, nsw 2000'\nprincipals:\n  - peter\n  - tom\n  - jane\nranking: 'No 5'\n",
      "school_details_object": {
        "school": {
          "name": "sydney grammar",
          "address": "1 fox road, sydney, nsw 2000"
        },
        "principals": {
          "peter",
          "tom",
          "jane"
        },
        "ranking": "No 5"
      },
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "correct_working_dir": "/up_project/up"
    })
    
    {{.my_school}}
    ~SubStep2: [print:  ]
    
    
    My school name is: sydney grammar, it is located
    at 1 fox road, sydney, nsw 2000
    
    
    We have got  peter,  tom,  jane,  as our principals
    
    Our school ranking last year is No 5
    
    
```

##### Logs with different verbose level
* [c0079 log - verbose level v](../../logs/c0079_v)
* [c0079 log - verbose level vv](../../logs/c0079_vv)
* [c0079 log - verbose level vvv](../../logs/c0079_vvv)
* [c0079 log - verbose level vvvv](../../logs/c0079_vvvv)
* [c0079 log - verbose level vvvvv](../../logs/c0079_vvvvv)

##### References
* [Related Chapter](../../design-patterns/c0079)
