---
title: "c0039_vvvv"
date: 2020-06-25T01:55:43+66:00
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
              ModuleName -> kickass_bohr8
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0039
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [kickass_bohr8] instance id: [dev]
    merged[ dev ] runtime vars:
    {
      "ha": true,
      "old": 54,
      "managers": {
        "tom",
        "jason",
        "alice"
      },
      "template_def_consume_dynamic_t1": "{{define \"T1\"}}ONE: {{.}}{{end}}\n",
      "age": 34,
      "template_def_consume_dynamic_t3": "{{define \"T3\"}}student:\n  name: {{template \"T1\" .name}}\n  gender: {{template \"T2\" .gender}}{{end}}\n{{template \"T3\" .student}}\n",
      "admins": {
        "tom",
        "jason",
        "alice"
      },
      "ns": "prod",
      "pod_name": "web_app",
      "nobody": <nil>,
      "student": {
        "teachers": {
          "tom",
          "jason",
          "alice"
        },
        "address": {
          "suburb": {
            "cbd": true,
            "name": "sydney",
            "postcode": 2000
          },
          "school": "Sydney Grammar"
        },
        "name": "Tom",
        "gender": "Male"
      },
      "template_def_consume_dynamic_main": "{{.template_def_consume_dynamic_t1}}\n{{.template_def_consume_dynamic_t2}}\n{{.template_def_consume_dynamic_t3}}\n{{template \"T3\" .student}}\n",
      "template_def_consume_dynamic_t2": "{{define \"T2\"}}TWO: {{.}}{{end}}"
    }
    
    dvar> usage_of_with:
    "  student name: Tom\n  school name: Sydney Grammar\n  Male\n  "
    
    dvar> usage_of_with_else:
    "  i am somebody  "
    
    dvar> template_def_plain:
    "\n\n\nONE TWO\"\n"
    
    dvar> template_def_consume:
    "\nshow example of how you can define reusable template\nand how you can pass in the parameters\n\n\n\n\nstudent:\n  name: ONE: Tom\n  gender: TWO: Male\n"
    
          template rendering problem -> template: .:4:11: executing "." at <{{template "T3" .student}}>: template "T3" not defined
    WARN:
        1:{{.template_def_consume_dynamic_t1}}
        2:{{.template_def_consume_dynamic_t2}}
        3:{{.template_def_consume_dynamic_t3}}
        4:{{template "T3" .student}}
        5:
        6:
    
    -----trace for reference-----
    dvar> template_def_consume_dynamic:
    "\n\n\n\nstudent:\n  name: ONE: Tom\n  gender: TWO: Male\n\n"
    
    dvar> template_use_block:
    "\n\nstudent:\n  name: ONE: Tom\ngender: TWO: Male\n\n"
    
    -------runtime global final merged with dvars-------
    
    {
      "admins": {
        "tom",
        "jason",
        "alice"
      },
      "ns": "prod",
      "nobody": <nil>,
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
            "postcode": 2000,
            "cbd": true,
            "name": "sydney"
          },
          "school": "Sydney Grammar"
        }
      },
      "usage_of_with": "  student name: Tom\n  school name: Sydney Grammar\n  Male\n  ",
      "usage_of_with_else": "  i am somebody  ",
      "template_def_plain": "\n\n\nONE TWO\"\n",
      "template_def_consume_dynamic_t3": "{{define \"T3\"}}student:\n  name: {{template \"T1\" .name}}\n  gender: {{template \"T2\" .gender}}{{end}}\n{{template \"T3\" .student}}\n",
      "template_use_block": "\n\nstudent:\n  name: ONE: Tom\ngender: TWO: Male\n\n",
      "template_def_consume": "\nshow example of how you can define reusable template\nand how you can pass in the parameters\n\n\n\n\nstudent:\n  name: ONE: Tom\n  gender: TWO: Male\n",
      "template_def_consume_dynamic": "\n\n\n\nstudent:\n  name: ONE: Tom\n  gender: TWO: Male\n\n",
      "managers": {
        "tom",
        "jason",
        "alice"
      },
      "age": 34,
      "pod_name": "web_app",
      "template_def_consume_dynamic_t1": "{{define \"T1\"}}ONE: {{.}}{{end}}\n",
      "template_def_consume_dynamic_t2": "{{define \"T2\"}}TWO: {{.}}{{end}}",
      "old": 54,
      "template_def_consume_dynamic_main": "{{.template_def_consume_dynamic_t1}}\n{{.template_def_consume_dynamic_t2}}\n{{.template_def_consume_dynamic_t3}}\n{{template \"T3\" .student}}\n",
      "ha": true
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    {
      Name: "",
      Do: {
        "echo \"value\\n {{.usage_of_with}}\"",
        "echo \"{{.usage_of_template}}\"",
        "echo \"{{.template_def_consume}}\"",
        "echo \"{{.template_def_consume_dynamic_t1}}\"",
        "echo \"{{.template_def_consume_dynamic_t2}}\"",
        "echo \"{{.template_def_consume_dynamic_t3}}\"",
        "echo \"{{.template_def_consume_dynamic}}\"",
        "echo \"{{.template_use_block}}\""
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
      "template_def_consume_dynamic_t2": "{{define \"T2\"}}TWO: {{.}}{{end}}",
      "pod_name": "web_app",
      "nobody": <nil>,
      "managers": {
        "tom",
        "jason",
        "alice"
      },
      "template_def_consume_dynamic": "\n\n\n\nstudent:\n  name: ONE: Tom\n  gender: TWO: Male\n\n",
      "template_def_consume_dynamic_main": "{{.template_def_consume_dynamic_t1}}\n{{.template_def_consume_dynamic_t2}}\n{{.template_def_consume_dynamic_t3}}\n{{template \"T3\" .student}}\n",
      "template_def_consume_dynamic_t1": "{{define \"T1\"}}ONE: {{.}}{{end}}\n",
      "ns": "prod",
      "student": {
        "gender": "Male",
        "teachers": {
          "tom",
          "jason",
          "alice"
        },
        "address": {
          "suburb": {
            "cbd": true,
            "name": "sydney",
            "postcode": 2000
          },
          "school": "Sydney Grammar"
        },
        "name": "Tom"
      },
      "usage_of_with": "  student name: Tom\n  school name: Sydney Grammar\n  Male\n  ",
      "usage_of_with_else": "  i am somebody  ",
      "template_use_block": "\n\nstudent:\n  name: ONE: Tom\ngender: TWO: Male\n\n",
      "age": 34,
      "ha": true,
      "template_def_consume_dynamic_t3": "{{define \"T3\"}}student:\n  name: {{template \"T1\" .name}}\n  gender: {{template \"T2\" .gender}}{{end}}\n{{template \"T3\" .student}}\n",
      "admins": {
        "tom",
        "jason",
        "alice"
      },
      "template_def_plain": "\n\n\nONE TWO\"\n",
      "template_def_consume": "\nshow example of how you can define reusable template\nand how you can pass in the parameters\n\n\n\n\nstudent:\n  name: ONE: Tom\n  gender: TWO: Male\n",
      "old": 54
    })
    
    kickass_bohr8: overall final exec vars:
    
    (*core.Cache)({
      "usage_of_with": "  student name: Tom\n  school name: Sydney Grammar\n  Male\n  ",
      "age": 34,
      "template_def_consume": "\nshow example of how you can define reusable template\nand how you can pass in the parameters\n\n\n\n\nstudent:\n  name: ONE: Tom\n  gender: TWO: Male\n",
      "nobody": <nil>,
      "managers": {
        "tom",
        "jason",
        "alice"
      },
      "usage_of_with_else": "  i am somebody  ",
      "ns": "prod",
      "student": {
        "address": {
          "school": "Sydney Grammar",
          "suburb": {
            "postcode": 2000,
            "cbd": true,
            "name": "sydney"
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
      "template_def_consume_dynamic_t2": "{{define \"T2\"}}TWO: {{.}}{{end}}",
      "template_def_consume_dynamic": "\n\n\n\nstudent:\n  name: ONE: Tom\n  gender: TWO: Male\n\n",
      "template_def_consume_dynamic_t1": "{{define \"T1\"}}ONE: {{.}}{{end}}\n",
      "template_def_plain": "\n\n\nONE TWO\"\n",
      "template_def_consume_dynamic_t3": "{{define \"T3\"}}student:\n  name: {{template \"T1\" .name}}\n  gender: {{template \"T2\" .gender}}{{end}}\n{{template \"T3\" .student}}\n",
      "pod_name": "web_app",
      "template_use_block": "\n\nstudent:\n  name: ONE: Tom\ngender: TWO: Male\n\n",
      "old": 54,
      "ha": true,
      "admins": {
        "tom",
        "jason",
        "alice"
      },
      "template_def_consume_dynamic_main": "{{.template_def_consume_dynamic_t1}}\n{{.template_def_consume_dynamic_t2}}\n{{.template_def_consume_dynamic_t3}}\n{{template \"T3\" .student}}\n"
    })
    
    cmd( 1):
    echo "value\n {{.usage_of_with}}"
    
     \_ echo "value\n   student name: Tom
      school name: Sydney Grammar
      Male
      "
    value\n   student name: Tom
      school name: Sydney Grammar
      Male
     .. ok
    cmd( 2):
    echo "{{.usage_of_template}}"
    
     \_ echo "<no value>"
    <no value>
     .. ok
    cmd( 3):
    echo "{{.template_def_consume}}"
    
     \_ echo "
    show example of how you can define reusable template
    and how you can pass in the parameters
    
    
    
    
    student:
      name: ONE: Tom
      gender: TWO: Male
    "
    show example of how you can define reusable template
    and how you can pass in the parameters
    
    
    
    
    student:
      name: ONE: Tom
      gender: TWO: Male
     .. ok
    cmd( 4):
    echo "{{.template_def_consume_dynamic_t1}}"
    
     \_ echo "{{define "T1"}}ONE: {{.}}{{end}}
    "
    {{define T1}}ONE: {{.}}{{end}}
     .. ok
    cmd( 5):
    echo "{{.template_def_consume_dynamic_t2}}"
    
     \_ echo "{{define "T2"}}TWO: {{.}}{{end}}"
    {{define T2}}TWO: {{.}}{{end}}
     .. ok
    cmd( 6):
    echo "{{.template_def_consume_dynamic_t3}}"
    
     \_ echo "{{define "T3"}}student:
      name: {{template "T1" .name}}
      gender: {{template "T2" .gender}}{{end}}
    {{template "T3" .student}}
    "
    {{define T3}}student:
      name: {{template T1 .name}}
      gender: {{template T2 .gender}}{{end}}
    {{template T3 .student}}
     .. ok
    cmd( 7):
    echo "{{.template_def_consume_dynamic}}"
    
     \_ echo "
    
    
    
    student:
      name: ONE: Tom
      gender: TWO: Male
    
    "
    student:
      name: ONE: Tom
      gender: TWO: Male
     .. ok
    cmd( 8):
    echo "{{.template_use_block}}"
    
     \_ echo "
    
    student:
      name: ONE: Tom
    gender: TWO: Male
    
    "
    student:
      name: ONE: Tom
    gender: TWO: Male
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
