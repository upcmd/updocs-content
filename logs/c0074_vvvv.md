---
title: "c0074_vvvv"
date: 2020-06-27T03:09:24+66:00
draft: false
weight: 10743

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0074
                 Verbose -> vvvv
              ModuleName -> berserk_mclean3
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0074
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [berserk_mclean3] instance id: [dev]
    merged[ dev ] runtime vars:
    {
    }
    
    -------runtime global final merged with dvars-------
    
    {
      "usecase": "doc_meta: |\n  folder: query-object\n  title: parse yml to object\n  head: |\n    Showcase you can load a yml file and parse the content to object\n\n  sections:\n    - title: How to use\n      content: |\n        Simply use dvar ref to load the content and also flag it to be converted to_object\n\n        The print cmd shows how to use the object and reference in golang template to iterate through the elements\n\n    - title: Relavant\n      content: to_object cmd\n      refs:\n        - title: to_object cmd\n          link: ../../cmd-func/c0095\n\n    - title: Demo\n      log: yes\n\ndocs:\n  goal:\n    - to test that I can parse this file to an object and use it in templating\n    - use the format like this to automate the docs generation\n\n  usecase:\n    - used to generate auto document for up project\n\n  usage:\n    - use docs as root element to document a functest or a test case\n    - two layers structure\n\ndvars:\n  - name: usecase\n    ref: c0074.yml\n    flags: [to_object,]\n\ntasks:\n  -\n    name: task\n    desc:\n    task:\n      -\n        func: cmd\n        do:\n          -\n            name: print\n            cmd: \"<no value>\"\n\n          -\n            name: print\n            cmd: \"<no value>\"\n\n          -\n            name: print\n            cmd: |-\n              \n\n          -\n            name: print\n            cmd: |-\n              \n",
      "usecase_object": {
        "dvars": {
          {
            "name": "usecase",
            "ref": "c0074.yml",
            "flags": {
              "to_object"
            }
          }
        },
        "tasks": {
          {
            "task": {
              {
                "func": "cmd",
                "do": {
                  {
                    "name": "print",
                    "cmd": "<no value>"
                  },
                  {
                    "name": "print",
                    "cmd": "<no value>"
                  },
                  {
                    "name": "print",
                    "cmd": ""
                  },
                  {
                    "cmd": "",
                    "name": "print"
                  }
                }
              }
            },
            "name": "task",
            "desc": <nil>
          }
        },
        "doc_meta": "folder: query-object\ntitle: parse yml to object\nhead: |\n  Showcase you can load a yml file and parse the content to object\n\nsections:\n  - title: How to use\n    content: |\n      Simply use dvar ref to load the content and also flag it to be converted to_object\n\n      The print cmd shows how to use the object and reference in golang template to iterate through the elements\n\n  - title: Relavant\n    content: to_object cmd\n    refs:\n      - title: to_object cmd\n        link: ../../cmd-func/c0095\n\n  - title: Demo\n    log: yes\n",
        "docs": {
          "goal": {
            "to test that I can parse this file to an object and use it in templating",
            "use the format like this to automate the docs generation"
          },
          "usecase": {
            "used to generate auto document for up project"
          },
          "usage": {
            "use docs as root element to document a functest or a test case",
            "two layers structure"
          }
        }
      }
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
          "cmd": "{{.usecase_object}}"
        },
        {
          "name": "print",
          "cmd": "{{.usecase_object.docs}}"
        },
        {
          "name": "print",
          "cmd": "{{range $case :=.usecase_object.docs}}\n{{$case}}\n{{end}}"
        },
        {
          "name": "print",
          "cmd": "{{range $head,$items :=.usecase_object.docs}}\n{{$head}}:\n  {{range $idx,$item :=$items}}\n    * {{$idx|add1}}: {{$item}}\n  {{end}}\n{{end}}"
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
      "usecase_object": {
        "dvars": {
          {
            "flags": {
              "to_object"
            },
            "name": "usecase",
            "ref": "c0074.yml"
          }
        },
        "tasks": {
          {
            "desc": <nil>,
            "task": {
              {
                "func": "cmd",
                "do": {
                  {
                    "name": "print",
                    "cmd": "<no value>"
                  },
                  {
                    "name": "print",
                    "cmd": "<no value>"
                  },
                  {
                    "name": "print",
                    "cmd": ""
                  },
                  {
                    "name": "print",
                    "cmd": ""
                  }
                }
              }
            },
            "name": "task"
          }
        },
        "doc_meta": "folder: query-object\ntitle: parse yml to object\nhead: |\n  Showcase you can load a yml file and parse the content to object\n\nsections:\n  - title: How to use\n    content: |\n      Simply use dvar ref to load the content and also flag it to be converted to_object\n\n      The print cmd shows how to use the object and reference in golang template to iterate through the elements\n\n  - title: Relavant\n    content: to_object cmd\n    refs:\n      - title: to_object cmd\n        link: ../../cmd-func/c0095\n\n  - title: Demo\n    log: yes\n",
        "docs": {
          "usecase": {
            "used to generate auto document for up project"
          },
          "usage": {
            "use docs as root element to document a functest or a test case",
            "two layers structure"
          },
          "goal": {
            "to test that I can parse this file to an object and use it in templating",
            "use the format like this to automate the docs generation"
          }
        }
      },
      "usecase": "doc_meta: |\n  folder: query-object\n  title: parse yml to object\n  head: |\n    Showcase you can load a yml file and parse the content to object\n\n  sections:\n    - title: How to use\n      content: |\n        Simply use dvar ref to load the content and also flag it to be converted to_object\n\n        The print cmd shows how to use the object and reference in golang template to iterate through the elements\n\n    - title: Relavant\n      content: to_object cmd\n      refs:\n        - title: to_object cmd\n          link: ../../cmd-func/c0095\n\n    - title: Demo\n      log: yes\n\ndocs:\n  goal:\n    - to test that I can parse this file to an object and use it in templating\n    - use the format like this to automate the docs generation\n\n  usecase:\n    - used to generate auto document for up project\n\n  usage:\n    - use docs as root element to document a functest or a test case\n    - two layers structure\n\ndvars:\n  - name: usecase\n    ref: c0074.yml\n    flags: [to_object,]\n\ntasks:\n  -\n    name: task\n    desc:\n    task:\n      -\n        func: cmd\n        do:\n          -\n            name: print\n            cmd: \"<no value>\"\n\n          -\n            name: print\n            cmd: \"<no value>\"\n\n          -\n            name: print\n            cmd: |-\n              \n\n          -\n            name: print\n            cmd: |-\n              \n"
    })
    
    berserk_mclean3: overall final exec vars:
    
    (*core.Cache)({
      "usecase": "doc_meta: |\n  folder: query-object\n  title: parse yml to object\n  head: |\n    Showcase you can load a yml file and parse the content to object\n\n  sections:\n    - title: How to use\n      content: |\n        Simply use dvar ref to load the content and also flag it to be converted to_object\n\n        The print cmd shows how to use the object and reference in golang template to iterate through the elements\n\n    - title: Relavant\n      content: to_object cmd\n      refs:\n        - title: to_object cmd\n          link: ../../cmd-func/c0095\n\n    - title: Demo\n      log: yes\n\ndocs:\n  goal:\n    - to test that I can parse this file to an object and use it in templating\n    - use the format like this to automate the docs generation\n\n  usecase:\n    - used to generate auto document for up project\n\n  usage:\n    - use docs as root element to document a functest or a test case\n    - two layers structure\n\ndvars:\n  - name: usecase\n    ref: c0074.yml\n    flags: [to_object,]\n\ntasks:\n  -\n    name: task\n    desc:\n    task:\n      -\n        func: cmd\n        do:\n          -\n            name: print\n            cmd: \"<no value>\"\n\n          -\n            name: print\n            cmd: \"<no value>\"\n\n          -\n            name: print\n            cmd: |-\n              \n\n          -\n            name: print\n            cmd: |-\n              \n",
      "usecase_object": {
        "dvars": {
          {
            "flags": {
              "to_object"
            },
            "name": "usecase",
            "ref": "c0074.yml"
          }
        },
        "tasks": {
          {
            "name": "task",
            "desc": <nil>,
            "task": {
              {
                "func": "cmd",
                "do": {
                  {
                    "cmd": "<no value>",
                    "name": "print"
                  },
                  {
                    "name": "print",
                    "cmd": "<no value>"
                  },
                  {
                    "name": "print",
                    "cmd": ""
                  },
                  {
                    "name": "print",
                    "cmd": ""
                  }
                }
              }
            }
          }
        },
        "doc_meta": "folder: query-object\ntitle: parse yml to object\nhead: |\n  Showcase you can load a yml file and parse the content to object\n\nsections:\n  - title: How to use\n    content: |\n      Simply use dvar ref to load the content and also flag it to be converted to_object\n\n      The print cmd shows how to use the object and reference in golang template to iterate through the elements\n\n  - title: Relavant\n    content: to_object cmd\n    refs:\n      - title: to_object cmd\n        link: ../../cmd-func/c0095\n\n  - title: Demo\n    log: yes\n",
        "docs": {
          "goal": {
            "to test that I can parse this file to an object and use it in templating",
            "use the format like this to automate the docs generation"
          },
          "usecase": {
            "used to generate auto document for up project"
          },
          "usage": {
            "use docs as root element to document a functest or a test case",
            "two layers structure"
          }
        }
      }
    })
    
    ~SubStep1: [print:  ]
    map[doc_meta:folder: query-object
    title: parse yml to object
    head: |
      Showcase you can load a yml file and parse the content to object
    
    sections:
      - title: How to use
        content: |
          Simply use dvar ref to load the content and also flag it to be converted to_object
    
          The print cmd shows how to use the object and reference in golang template to iterate through the elements
    
      - title: Relavant
        content: to_object cmd
        refs:
          - title: to_object cmd
            link: ../../cmd-func/c0095
    
      - title: Demo
        log: yes
     docs:map[goal:[to test that I can parse this file to an object and use it in templating use the format like this to automate the docs generation] usage:[use docs as root element to document a functest or a test case two layers structure] usecase:[used to generate auto document for up project]] dvars:[map[flags:[to_object] name:usecase ref:c0074.yml]] tasks:[map[desc:<nil> name:task task:[map[do:[map[cmd:<no value> name:print] map[cmd:<no value> name:print] map[cmd: name:print] map[cmd: name:print]] func:cmd]]]]]
    ~SubStep2: [print:  ]
    map[goal:[to test that I can parse this file to an object and use it in templating use the format like this to automate the docs generation] usage:[use docs as root element to document a functest or a test case two layers structure] usecase:[used to generate auto document for up project]]
    ~SubStep3: [print:  ]
    
    [to test that I can parse this file to an object and use it in templating use the format like this to automate the docs generation]
    
    [use docs as root element to document a functest or a test case two layers structure]
    
    [used to generate auto document for up project]
    
    ~SubStep4: [print:  ]
    
    goal:
      
        * 1: to test that I can parse this file to an object and use it in templating
      
        * 2: use the format like this to automate the docs generation
      
    
    usage:
      
        * 1: use docs as root element to document a functest or a test case
      
        * 2: two layers structure
      
    
    usecase:
      
        * 1: used to generate auto document for up project
      
    
    
```

##### Logs with different verbose level
* [c0074 log - verbose level v](../../logs/c0074_v)
* [c0074 log - verbose level vv](../../logs/c0074_vv)
* [c0074 log - verbose level vvv](../../logs/c0074_vvv)
* [c0074 log - verbose level vvvv](../../logs/c0074_vvvv)
* [c0074 log - verbose level vvvvv](../../logs/c0074_vvvvv)

##### References
* [Related Chapter](../../query-object/c0074)
