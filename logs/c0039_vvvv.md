---
title: "c0039_vvvv"
date: 2020-10-07T00:11:07+1010:00
draft: false
weight: 10393

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0039
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
    loading [Task]:  ./tests/functests/c0039
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
      "age": 34,
      "ha": true,
      "admins": {
        "tom",
        "jason",
        "alice"
      },
      "template_def_consume_dynamic_t2": "{{define \"T2\"}}TWO: {{.}}{{end}}",
      "old": 54,
      "template_def_consume_dynamic_t1": "{{define \"T1\"}}ONE: {{.}}{{end}}\n",
      "student": {
        "name": "Tom",
        "gender": "Male",
        "teachers": {
          "tom",
          "jason",
          "alice"
        },
        "address": {
          "school": "Sydney Grammar",
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "cbd": true
          }
        }
      },
      "nobody": <nil>,
      "template_def_consume_dynamic_main": "{{.template_def_consume_dynamic_t1}}\n{{.template_def_consume_dynamic_t2}}\n{{.template_def_consume_dynamic_t3}}\n{{template \"T3\" .student}}\n",
      "template_def_consume_dynamic_t3": "{{define \"T3\"}}student:\n  name: {{template \"T1\" .name}}\n  gender: {{template \"T2\" .gender}}{{end}}\n{{template \"T3\" .student}}\n",
      "ns": "prod",
      "managers": {
        "tom",
        "jason",
        "alice"
      },
      "pod_name": "web_app"
    })
    
    dvar> usage_of_with:
    "  student name: Tom\n  school name: Sydney Grammar\n  Male\n  "
    
    -
      student name: Tom
      school name: Sydney Grammar
      Male
      
    dvar> usage_of_with_else:
    "  i am somebody  "
    
    -
      i am somebody  
    dvar> template_def_plain:
    "\n\n\nONE TWO\"\n"
    
    -
    
    
    
    ONE TWO"
    
    dvar> template_def_consume:
    "\nshow example of how you can define reusable template\nand how you can pass in the parameters\n\n\n\n\nstudent:\n  name: ONE: Tom\n  gender: TWO: Male\n"
    
    -
    
    show example of how you can define reusable template
    and how you can pass in the parameters
    
    
    
    
    student:
      name: ONE: Tom
      gender: TWO: Male
    
          template rendering -> template: .:4:11: executing "." at <{{template "T3" .student}}>: template "T3" not defined
    WARN:
        1:{{.template_def_consume_dynamic_t1}}
        2:{{.template_def_consume_dynamic_t2}}
        3:{{.template_def_consume_dynamic_t3}}
        4:{{template "T3" .student}}
        5:
        6:
    
    trouble shooting tips:
    <incompatible types for comparison>: the variable might not be registered, use -v vvv to see the cache, or use inspect cmd to debug
    
    dvar> template_def_consume_dynamic:
    "\n\n\n\nstudent:\n  name: ONE: Tom\n  gender: TWO: Male\n\n"
    
    -
    
    
    
    
    student:
      name: ONE: Tom
      gender: TWO: Male
    
    
    dvar> template_use_block:
    "\n\nstudent:\n  name: ONE: Tom\ngender: TWO: Male\n\n"
    
    -
    
    
    student:
      name: ONE: Tom
    gender: TWO: Male
    
    
    -------runtime global final merged with dvars-------
    
    (*core.Cache)({
      "ha": true,
      "template_def_consume_dynamic_t3": "{{define \"T3\"}}student:\n  name: {{template \"T1\" .name}}\n  gender: {{template \"T2\" .gender}}{{end}}\n{{template \"T3\" .student}}\n",
      "admins": {
        "tom",
        "jason",
        "alice"
      },
      "usage_of_with": "  student name: Tom\n  school name: Sydney Grammar\n  Male\n  ",
      "nobody": <nil>,
      "template_def_consume_dynamic_t2": "{{define \"T2\"}}TWO: {{.}}{{end}}",
      "template_use_block": "\n\nstudent:\n  name: ONE: Tom\ngender: TWO: Male\n\n",
      "template_def_consume_dynamic": "\n\n\n\nstudent:\n  name: ONE: Tom\n  gender: TWO: Male\n\n",
      "usage_of_with_else": "  i am somebody  ",
      "template_def_consume_dynamic_main": "{{.template_def_consume_dynamic_t1}}\n{{.template_def_consume_dynamic_t2}}\n{{.template_def_consume_dynamic_t3}}\n{{template \"T3\" .student}}\n",
      "template_def_consume_dynamic_t1": "{{define \"T1\"}}ONE: {{.}}{{end}}\n",
      "template_def_plain": "\n\n\nONE TWO\"\n",
      "old": 54,
      "template_def_consume": "\nshow example of how you can define reusable template\nand how you can pass in the parameters\n\n\n\n\nstudent:\n  name: ONE: Tom\n  gender: TWO: Male\n",
      "pod_name": "web_app",
      "student": {
        "address": {
          "suburb": {
            "postcode": 2000,
            "cbd": true,
            "name": "sydney"
          },
          "school": "Sydney Grammar"
        },
        "name": "Tom",
        "gender": "Male",
        "teachers": {
          "tom",
          "jason",
          "alice"
        }
      },
      "managers": {
        "tom",
        "jason",
        "alice"
      },
      "age": 34,
      "ns": "prod"
    })
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "ha": true,
      "template_def_consume_dynamic_t3": "{{define \"T3\"}}student:\n  name: {{template \"T1\" .name}}\n  gender: {{template \"T2\" .gender}}{{end}}\n{{template \"T3\" .student}}\n",
      "ns": "prod",
      "usage_of_with": "  student name: Tom\n  school name: Sydney Grammar\n  Male\n  ",
      "template_def_consume_dynamic": "\n\n\n\nstudent:\n  name: ONE: Tom\n  gender: TWO: Male\n\n",
      "template_def_plain": "\n\n\nONE TWO\"\n",
      "up_runtime_task_layer_number": 0,
      "template_def_consume_dynamic_t2": "{{define \"T2\"}}TWO: {{.}}{{end}}",
      "pod_name": "web_app",
      "usage_of_with_else": "  i am somebody  ",
      "old": 54,
      "nobody": <nil>,
      "student": {
        "address": {
          "school": "Sydney Grammar",
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "cbd": true
          }
        },
        "name": "Tom",
        "gender": "Male",
        "teachers": {
          "tom",
          "jason",
          "alice"
        }
      },
      "template_def_consume_dynamic_t1": "{{define \"T1\"}}ONE: {{.}}{{end}}\n",
      "template_def_consume": "\nshow example of how you can define reusable template\nand how you can pass in the parameters\n\n\n\n\nstudent:\n  name: ONE: Tom\n  gender: TWO: Male\n",
      "admins": {
        "tom",
        "jason",
        "alice"
      },
      "template_def_consume_dynamic_main": "{{.template_def_consume_dynamic_t1}}\n{{.template_def_consume_dynamic_t2}}\n{{.template_def_consume_dynamic_t3}}\n{{template \"T3\" .student}}\n",
      "template_use_block": "\n\nstudent:\n  name: ONE: Tom\ngender: TWO: Male\n\n",
      "managers": {
        "tom",
        "jason",
        "alice"
      },
      "age": 34
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "student": {
        "name": "Tom",
        "gender": "Male",
        "teachers": {
          "tom",
          "jason",
          "alice"
        },
        "address": {
          "suburb": {
            "name": "sydney",
            "postcode": 2000,
            "cbd": true
          },
          "school": "Sydney Grammar"
        }
      },
      "ha": true,
      "pod_name": "web_app",
      "template_def_consume_dynamic": "\n\n\n\nstudent:\n  name: ONE: Tom\n  gender: TWO: Male\n\n",
      "template_def_plain": "\n\n\nONE TWO\"\n",
      "up_runtime_task_layer_number": 0,
      "nobody": <nil>,
      "old": 54,
      "usage_of_with": "  student name: Tom\n  school name: Sydney Grammar\n  Male\n  ",
      "admins": {
        "tom",
        "jason",
        "alice"
      },
      "template_def_consume_dynamic_main": "{{.template_def_consume_dynamic_t1}}\n{{.template_def_consume_dynamic_t2}}\n{{.template_def_consume_dynamic_t3}}\n{{template \"T3\" .student}}\n",
      "template_def_consume_dynamic_t1": "{{define \"T1\"}}ONE: {{.}}{{end}}\n",
      "template_def_consume_dynamic_t3": "{{define \"T3\"}}student:\n  name: {{template \"T1\" .name}}\n  gender: {{template \"T2\" .gender}}{{end}}\n{{template \"T3\" .student}}\n",
      "age": 34,
      "template_def_consume_dynamic_t2": "{{define \"T2\"}}TWO: {{.}}{{end}}",
      "template_use_block": "\n\nstudent:\n  name: ONE: Tom\ngender: TWO: Male\n\n",
      "managers": {
        "tom",
        "jason",
        "alice"
      },
      "template_def_consume": "\nshow example of how you can define reusable template\nand how you can pass in the parameters\n\n\n\n\nstudent:\n  name: ONE: Tom\n  gender: TWO: Male\n",
      "ns": "prod",
      "usage_of_with_else": "  i am somebody  "
    })
    
    cmd( 1):
    echo "value\n {{.usage_of_with}}"
    
    cmd=>:
    echo "value\n   student name: Tom
      school name: Sydney Grammar
      Male
      "
    -
    value\n   student name: Tom
      school name: Sydney Grammar
      Male
      
    
    -
     .. ok
    cmd( 2):
    echo "{{.usage_of_template}}"
    
    cmd=>:
    echo "<no value>"
    -
    <no value>
    
    -
     .. ok
    cmd( 3):
    echo "{{.template_def_consume}}"
    
    cmd=>:
    echo "
    show example of how you can define reusable template
    and how you can pass in the parameters
    
    
    
    
    student:
      name: ONE: Tom
      gender: TWO: Male
    "
    -
    
    show example of how you can define reusable template
    and how you can pass in the parameters
    
    
    
    
    student:
      name: ONE: Tom
      gender: TWO: Male
    
    
    -
     .. ok
    cmd( 4):
    echo "{{.template_def_consume_dynamic_t1}}"
    
    cmd=>:
    echo "{{define "T1"}}ONE: {{.}}{{end}}
    "
    -
    {{define T1}}ONE: {{.}}{{end}}
    
    
    -
     .. ok
    cmd( 5):
    echo "{{.template_def_consume_dynamic_t2}}"
    
    cmd=>:
    echo "{{define "T2"}}TWO: {{.}}{{end}}"
    -
    {{define T2}}TWO: {{.}}{{end}}
    
    -
     .. ok
    cmd( 6):
    echo "{{.template_def_consume_dynamic_t3}}"
    
    cmd=>:
    echo "{{define "T3"}}student:
      name: {{template "T1" .name}}
      gender: {{template "T2" .gender}}{{end}}
    {{template "T3" .student}}
    "
    -
    {{define T3}}student:
      name: {{template T1 .name}}
      gender: {{template T2 .gender}}{{end}}
    {{template T3 .student}}
    
    
    -
     .. ok
    cmd( 7):
    echo "{{.template_def_consume_dynamic}}"
    
    cmd=>:
    echo "
    
    
    
    student:
      name: ONE: Tom
      gender: TWO: Male
    
    "
    -
    
    
    
    
    student:
      name: ONE: Tom
      gender: TWO: Male
    
    
    
    -
     .. ok
    cmd( 8):
    echo "{{.template_use_block}}"
    
    cmd=>:
    echo "
    
    student:
      name: ONE: Tom
    gender: TWO: Male
    
    "
    -
    
    
    student:
      name: ONE: Tom
    gender: TWO: Male
    
    
    
    -
     .. ok
    . ok
    
```

##### Logs with different verbose level
* [c0039 log - verbose level v](../../logs/c0039_v)
* [c0039 log - verbose level vv](../../logs/c0039_vv)
* [c0039 log - verbose level vvv](../../logs/c0039_vvv)
* [c0039 log - verbose level vvvv](../../logs/c0039_vvvv)
* [c0039 log - verbose level vvvvv](../../logs/c0039_vvvvv)

##### References
* [Related Chapter](../../template/c0039)
