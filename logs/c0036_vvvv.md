---
title: "c0036_vvvv"
date: 2020-07-01T15:34:25+77:00
draft: false
weight: 10363

---

### Log reference: <no value>

```
    loading [Config]:  ./tests/functests/upconfig.yml
    Main config:
                 Version -> 1.0.0
                  RefDir -> ./tests/functests
                 WorkDir -> cwd
              AbsWorkDir -> /up_project/up
                TaskFile -> c0036
                 Verbose -> vvvv
              ModuleName -> boring_shockley5
               ShellType -> /bin/sh
           MaxCallLayers -> 8
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0036
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    module: [boring_shockley5] instance id: [dev]
    merged[ dev ] runtime vars:
    {
      "managers": {
        "tom",
        "jason",
        "alice"
      },
      "ns": "prod",
      "pod_name": "web_app",
      "ha": true,
      "age": 34,
      "old": 54,
      "admins": {
        "tom",
        "jason",
        "alice"
      }
    }
    
    dvar> var_with_range:
    " x  x  x "
    
    dvar> var_with_range_item:
    " tom  jason  alice "
    
    dvar> var_with_range_item_simpler:
    " tom  jason  alice "
    
    dvar> var_test_log_auto_print:
    "prodweb_app"
    
    dvar> var_test_log_auto_print_object:
    "prodweb_app"
    
    dvar> var_with_and:
    "web_app"
    
    dvar> var_slice_index:
    "jason"
    
    dvar> var_slice:
    "[jason]"
    
    dvar> var_equal:
    "false"
    
    dvar> var_not_equal:
    "true"
    
    dvar> var_greater:
    "false"
    
    dvar> var_greater_and_equal:
    "true"
    
    dvar> var_greater_and_equal:
    "hello"
    
    dvar> template_def:
    "\n\n\nONE TWO\"\n"
    
    -------runtime global final merged with dvars-------
    
    {
      "var_with_ifelse_multilines": "  prod-web_app-HA ",
      "var_length": "12",
      "var_space_trimmed": "prod-web_app",
      "pod_name": "web_app",
      "var_commented_trimmed": "prod-web_app",
      "var_with_not": "prod-web_app",
      "var_space_not_trimmed": "prod       -            web_app",
      "var_with_range_item": " tom  jason  alice ",
      "admins": {
        "tom",
        "jason",
        "alice"
      },
      "ns": "prod",
      "var_with_range": " x  x  x ",
      "var_slice_index": "jason",
      "age": 34,
      "var_slice": "[jason]",
      "var_with_ifelse": "prod-web_app-HA",
      "var_greater": "false",
      "var_commented": " prod-web_app",
      "ha": true,
      "var_with_print": "prodweb_app",
      "var_test_log_auto_print": "prodweb_app",
      "var_with_range_item_simpler": " tom  jason  alice ",
      "var_not_equal": "true",
      "var_greater_and_equal": "hello",
      "template_def": "\n\n\nONE TWO\"\n",
      "var_equal": "false",
      "var_with_and": "web_app",
      "old": 54,
      "managers": {
        "tom",
        "jason",
        "alice"
      },
      "instance_full_name": "prod-web_app",
      "var_with_or": "prod",
      "var_test_log_auto_print_object": "prodweb_app",
      "var_with_if": "prod-web_app-HA",
      "var_with_not_object": "prod-web_app"
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    {
      Name: "",
      Do: {
        "echo \"{{.instance_full_name}}\"",
        "echo \"{{.var_space_not_trimmed}}\"",
        "echo \"{{.var_space_trimmed}}\"",
        "echo \"{{.var_commented}}\"",
        "echo \"{{.var_commented_trimmed}}\"",
        "echo \"{{.var_with_if}}\"",
        "echo \"{{.var_with_ifelse}}\"",
        "echo \"{{.var_with_ifelse_multilines}}\"",
        "echo \"{{.var_with_not}}\"",
        "echo \"{{.var_with_not_object}}\"",
        "echo \"{{.var_length}}\"",
        "echo \"{{.var_with_or}}\"",
        "echo \"{{.var_with_print}}\"",
        "echo \"check the value of other dvar using vvvv flag print out\""
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
      "instance_full_name": "prod-web_app",
      "ns": "prod",
      "var_with_range": " x  x  x ",
      "var_space_trimmed": "prod-web_app",
      "var_with_ifelse_multilines": "  prod-web_app-HA ",
      "admins": {
        "tom",
        "jason",
        "alice"
      },
      "var_with_print": "prodweb_app",
      "var_with_and": "web_app",
      "var_commented_trimmed": "prod-web_app",
      "var_space_not_trimmed": "prod       -            web_app",
      "var_slice_index": "jason",
      "var_with_ifelse": "prod-web_app-HA",
      "age": 34,
      "var_test_log_auto_print": "prodweb_app",
      "template_def": "\n\n\nONE TWO\"\n",
      "var_greater_and_equal": "hello",
      "var_with_not_object": "prod-web_app",
      "pod_name": "web_app",
      "var_not_equal": "true",
      "old": 54,
      "var_with_range_item": " tom  jason  alice ",
      "var_with_range_item_simpler": " tom  jason  alice ",
      "var_with_or": "prod",
      "var_length": "12",
      "var_with_not": "prod-web_app",
      "ha": true,
      "var_equal": "false",
      "managers": {
        "tom",
        "jason",
        "alice"
      },
      "var_test_log_auto_print_object": "prodweb_app",
      "var_with_if": "prod-web_app-HA",
      "var_slice": "[jason]",
      "var_greater": "false",
      "var_commented": " prod-web_app"
    })
    
    boring_shockley5: overall final exec vars:
    
    (*core.Cache)({
      "var_with_or": "prod",
      "var_length": "12",
      "var_greater": "false",
      "instance_full_name": "prod-web_app",
      "ns": "prod",
      "var_with_ifelse_multilines": "  prod-web_app-HA ",
      "var_with_ifelse": "prod-web_app-HA",
      "var_greater_and_equal": "hello",
      "var_with_not_object": "prod-web_app",
      "var_not_equal": "true",
      "var_equal": "false",
      "template_def": "\n\n\nONE TWO\"\n",
      "old": 54,
      "var_test_log_auto_print_object": "prodweb_app",
      "var_with_if": "prod-web_app-HA",
      "var_commented_trimmed": "prod-web_app",
      "managers": {
        "tom",
        "jason",
        "alice"
      },
      "var_slice_index": "jason",
      "pod_name": "web_app",
      "var_with_range_item_simpler": " tom  jason  alice ",
      "var_commented": " prod-web_app",
      "var_space_trimmed": "prod-web_app",
      "admins": {
        "tom",
        "jason",
        "alice"
      },
      "var_with_print": "prodweb_app",
      "var_with_and": "web_app",
      "var_space_not_trimmed": "prod       -            web_app",
      "var_test_log_auto_print": "prodweb_app",
      "var_with_not": "prod-web_app",
      "var_with_range": " x  x  x ",
      "age": 34,
      "var_with_range_item": " tom  jason  alice ",
      "ha": true,
      "var_slice": "[jason]"
    })
    
    cmd( 1):
    echo "{{.instance_full_name}}"
    
     \_ echo "prod-web_app"
    prod-web_app
     .. ok
    cmd( 2):
    echo "{{.var_space_not_trimmed}}"
    
     \_ echo "prod       -            web_app"
    prod       -            web_app
     .. ok
    cmd( 3):
    echo "{{.var_space_trimmed}}"
    
     \_ echo "prod-web_app"
    prod-web_app
     .. ok
    cmd( 4):
    echo "{{.var_commented}}"
    
     \_ echo " prod-web_app"
    prod-web_app
     .. ok
    cmd( 5):
    echo "{{.var_commented_trimmed}}"
    
     \_ echo "prod-web_app"
    prod-web_app
     .. ok
    cmd( 6):
    echo "{{.var_with_if}}"
    
     \_ echo "prod-web_app-HA"
    prod-web_app-HA
     .. ok
    cmd( 7):
    echo "{{.var_with_ifelse}}"
    
     \_ echo "prod-web_app-HA"
    prod-web_app-HA
     .. ok
    cmd( 8):
    echo "{{.var_with_ifelse_multilines}}"
    
     \_ echo "  prod-web_app-HA "
    prod-web_app-HA
     .. ok
    cmd( 9):
    echo "{{.var_with_not}}"
    
     \_ echo "prod-web_app"
    prod-web_app
     .. ok
    cmd(10):
    echo "{{.var_with_not_object}}"
    
     \_ echo "prod-web_app"
    prod-web_app
     .. ok
    cmd(11):
    echo "{{.var_length}}"
    
     \_ echo "12"
    12
     .. ok
    cmd(12):
    echo "{{.var_with_or}}"
    
     \_ echo "prod"
    prod
     .. ok
    cmd(13):
    echo "{{.var_with_print}}"
    
     \_ echo "prodweb_app"
    prodweb_app
     .. ok
    cmd(14):
    echo "check the value of other dvar using vvvv flag print out"
    
     \_ echo "check the value of other dvar using vvvv flag print out"
    check the value of other dvar using vvvv flag print out
     .. ok
    . ok
    
```

##### Logs with different verbose level
* [c0036 log - verbose level v](../../logs/c0036_v)
* [c0036 log - verbose level vv](../../logs/c0036_vv)
* [c0036 log - verbose level vvv](../../logs/c0036_vvv)
* [c0036 log - verbose level vvvv](../../logs/c0036_vvvv)
* [c0036 log - verbose level vvvvv](../../logs/c0036_vvvvv)

##### References
* [Related Chapter](../../template/c0036)
