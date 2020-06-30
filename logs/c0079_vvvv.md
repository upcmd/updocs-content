---
title: "c0079_vvvv"
date: 2020-07-01T15:34:31+77:00
draft: false
weight: 10793

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
                 Verbose -> vvvv
              ModuleName -> sick_perlman6
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0079
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [sick_perlman6] instance id: [dev]
    merged[ dev ] runtime vars:
    {
      "complex_data_structure_template": "school:\n  name: '{{.school_name}}'\n  address: '{{.school_address}}'\nprincipals:\n{{- range $_, $p :=.schoo_principals }}\n  - {{$p}}\n{{- end}}\nranking: '{{.schoo_ranking}}'\n"
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
          "name": "print",
          "cmd": "{{.school_string}}"
        }
      },
      Dox: <nil>,
      Func: "cmd",
      Vars: {
        "school_address": "1 fox road, sydney, nsw 2000",
        "schoo_principals": {
          "peter",
          "tom",
          "jane"
        },
        "schoo_ranking": "No 5",
        "school_name": "sydney grammar"
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
      "school_name": "sydney grammar",
      "school_address": "1 fox road, sydney, nsw 2000",
      "schoo_principals": {
        "peter",
        "tom",
        "jane"
      },
      "schoo_ranking": "No 5",
      "complex_data_structure_template": "school:\n  name: '{{.school_name}}'\n  address: '{{.school_address}}'\nprincipals:\n{{- range $_, $p :=.schoo_principals }}\n  - {{$p}}\n{{- end}}\nranking: '{{.schoo_ranking}}'\n",
      "intest": "false"
    })
    
    sick_perlman6: overall final exec vars:
    
    (*core.Cache)({
      "school_string": "school:\n  name: '{{.school_name}}'\n  address: '{{.school_address}}'\nprincipals:\n{{- range $_, $p :=.schoo_principals }}\n  - {{$p}}\n{{- end}}\nranking: '{{.schoo_ranking}}'\n",
      "complex_data_structure_template": "school:\n  name: '{{.school_name}}'\n  address: '{{.school_address}}'\nprincipals:\n{{- range $_, $p :=.schoo_principals }}\n  - {{$p}}\n{{- end}}\nranking: '{{.schoo_ranking}}'\n",
      "intest": "false",
      "school_name": "sydney grammar",
      "school_address": "1 fox road, sydney, nsw 2000",
      "schoo_principals": {
        "peter",
        "tom",
        "jane"
      },
      "schoo_ranking": "No 5"
    })
    
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
        "schoo_ranking": "No 5",
        "school_name": "sydney grammar",
        "school_address": "1 fox road, sydney, nsw 2000",
        "schoo_principals": {
          "peter",
          "tom",
          "jane"
        }
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
      "complex_data_structure_template": "school:\n  name: '{{.school_name}}'\n  address: '{{.school_address}}'\nprincipals:\n{{- range $_, $p :=.schoo_principals }}\n  - {{$p}}\n{{- end}}\nranking: '{{.schoo_ranking}}'\n",
      "intest": "false",
      "schoo_principals": {
        "peter",
        "tom",
        "jane"
      },
      "schoo_ranking": "No 5",
      "school_name": "sydney grammar",
      "school_address": "1 fox road, sydney, nsw 2000"
    })
    
    sick_perlman6: overall final exec vars:
    
    (*core.Cache)({
      "school_address": "1 fox road, sydney, nsw 2000",
      "complex_data_structure_template": "school:\n  name: '{{.school_name}}'\n  address: '{{.school_address}}'\nprincipals:\n{{- range $_, $p :=.schoo_principals }}\n  - {{$p}}\n{{- end}}\nranking: '{{.schoo_ranking}}'\n",
      "intest": "false",
      "schoo_principals": {
        "peter",
        "tom",
        "jane"
      },
      "schoo_ranking": "No 5",
      "school_name": "sydney grammar",
      "school_yml": "school:\n  name: 'sydney grammar'\n  address: '1 fox road, sydney, nsw 2000'\nprincipals:\n  - peter\n  - tom\n  - jane\nranking: 'No 5'\n"
    })
    
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
      "intest": "false",
      "school_yml": "school:\n  name: 'sydney grammar'\n  address: '1 fox road, sydney, nsw 2000'\nprincipals:\n  - peter\n  - tom\n  - jane\nranking: 'No 5'\n",
      "complex_data_structure_template": "school:\n  name: '{{.school_name}}'\n  address: '{{.school_address}}'\nprincipals:\n{{- range $_, $p :=.schoo_principals }}\n  - {{$p}}\n{{- end}}\nranking: '{{.schoo_ranking}}'\n"
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
    
    sick_perlman6: overall final exec vars:
    
    (*core.Cache)({
      "intest": "false",
      "school_yml": "school:\n  name: 'sydney grammar'\n  address: '1 fox road, sydney, nsw 2000'\nprincipals:\n  - peter\n  - tom\n  - jane\nranking: 'No 5'\n",
      "complex_data_structure_template": "school:\n  name: '{{.school_name}}'\n  address: '{{.school_address}}'\nprincipals:\n{{- range $_, $p :=.schoo_principals }}\n  - {{$p}}\n{{- end}}\nranking: '{{.schoo_ranking}}'\n",
      "school_details": "school:\n  name: 'sydney grammar'\n  address: '1 fox road, sydney, nsw 2000'\nprincipals:\n  - peter\n  - tom\n  - jane\nranking: 'No 5'\n",
      "school_details_object": {
        "school": {
          "address": "1 fox road, sydney, nsw 2000",
          "name": "sydney grammar"
        },
        "principals": {
          "peter",
          "tom",
          "jane"
        },
        "ranking": "No 5"
      }
    })
    
    ~SubStep1: [print:  ]
    school:
      name: 'sydney grammar'
      address: '1 fox road, sydney, nsw 2000'
    principals:
      - peter
      - tom
      - jane
    ranking: 'No 5'
    
    ~SubStep2: [printobj:  ]
    (string) (len=14) "school_details"
    
    object:
     school_details: "school:\n  name: 'sydney grammar'\n  address: '1 fox road, sydney, nsw 2000'\nprincipals:\n  - peter\n  - tom\n  - jane\nranking: 'No 5'\n"
    
    ~SubStep3: [print:  ]
    school:
      name: 'sydney grammar'
      address: '1 fox road, sydney, nsw 2000'
    principals:
      - peter
      - tom
      - jane
    ranking: 'No 5'
    
    ~SubStep4: [printobj:  ]
    (string) (len=21) "school_details_object"
    
    object:
     school_details_object: {
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
      "complex_data_structure_template": "school:\n  name: '{{.school_name}}'\n  address: '{{.school_address}}'\nprincipals:\n{{- range $_, $p :=.schoo_principals }}\n  - {{$p}}\n{{- end}}\nranking: '{{.schoo_ranking}}'\n",
      "intest": "false"
    })
    
    sick_perlman6: overall final exec vars:
    
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
      "school_details": "school:\n  name: 'sydney grammar'\n  address: '1 fox road, sydney, nsw 2000'\nprincipals:\n  - peter\n  - tom\n  - jane\nranking: 'No 5'\n"
    })
    
    cmd( 1):
    echo "?intest ->  {{.intest}}"
    
     \_ echo "?intest ->  false"
    ?intest ->  false
     .. ok
    cmd( 2):
    pwd
    
     \_ pwd
    /up_project/up
     .. ok
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
    
    sick_perlman6: overall final exec vars:
    
    (*core.Cache)({
      "intest": "false",
      "school_yml": "school:\n  name: 'sydney grammar'\n  address: '1 fox road, sydney, nsw 2000'\nprincipals:\n  - peter\n  - tom\n  - jane\nranking: 'No 5'\n",
      "school_details_object": {
        "ranking": "No 5",
        "school": {
          "address": "1 fox road, sydney, nsw 2000",
          "name": "sydney grammar"
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
      "complex_data_structure_template": "school:\n  name: '{{.school_name}}'\n  address: '{{.school_address}}'\nprincipals:\n{{- range $_, $p :=.schoo_principals }}\n  - {{$p}}\n{{- end}}\nranking: '{{.schoo_ranking}}'\n"
    })
    
    ~SubStep1: [print:  ]
    intest is: [false]
    ~SubStep2: [reg:  ]
    -Step6:
    {
      Name: "",
      Do: {
        {
          "name": "print",
          "cmd": "root dir is: [{{.register_task_root.Output}}]"
        },
        {
          "cmd": "correct working dir is: [{{.correct_working_dir}}]",
          "name": "print"
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
      }),
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "correct_working_dir": "/up_project/up",
      "complex_data_structure_template": "school:\n  name: '{{.school_name}}'\n  address: '{{.school_address}}'\nprincipals:\n{{- range $_, $p :=.schoo_principals }}\n  - {{$p}}\n{{- end}}\nranking: '{{.schoo_ranking}}'\n"
    })
    
    sick_perlman6: overall final exec vars:
    
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
    
    ~SubStep1: [print:  ]
    root dir is: [/up_project/up]
    ~SubStep2: [print:  ]
    correct working dir is: [/up_project/up]
    -Step7: [: render final result using template ]
    {
      Name: "",
      Do: {
        {
          "desc": "render the template file using above dynamic variable from defined var",
          "cmd": {
            "src": "{{.correct_working_dir}}/tests/functests/d0079.template",
            "dest": "/tmp/myschool.txt",
            "datakey": "school_details_object"
          },
          "name": "template"
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
    
    sick_perlman6: overall final exec vars:
    
    (*core.Cache)({
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
      }),
      "last_result": (*utils.ExecResult)({
        Code: 0,
        Output: "/up_project/up",
        ErrMsg: ""
      }),
      "correct_working_dir": "/up_project/up",
      "complex_data_structure_template": "school:\n  name: '{{.school_name}}'\n  address: '{{.school_address}}'\nprincipals:\n{{- range $_, $p :=.schoo_principals }}\n  - {{$p}}\n{{- end}}\nranking: '{{.schoo_ranking}}'\n"
    })
    
    sick_perlman6: overall final exec vars:
    
    (*core.Cache)({
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
      }
    })
    
    ~SubStep1: [readfile: read content of a file and register it to a var ]
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
