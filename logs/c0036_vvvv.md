---
title: "c0036_vvvv"
date: 2020-07-20T02:01:35+77:00
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
              ModuleName -> self
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
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    module: [self] instance id: [dev]
    merged[ dev ] runtime vars:
    {
      "fieldnames": {
        "name-with-dash": "this_is_a_field_with_dash: you will have to use index func to access the field\nnote: direct access this field will trigger template rendering error\n"
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
      },
      "managers": {
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
    
    dvar> out_of_normal_field_name:
    "this_is_a_field_with_dash: you will have to use index func to access the field\nnote: direct access this field will trigger template rendering error\n"
    
    dvar> var_slice:
    "[jason]"
    
    dvar> var_equal:
    "false"
    
    dvar> var_not_equal:
    "true"
    
    dvar> var_not_equal_another_way:
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
      "fieldnames": {
        "name-with-dash": "this_is_a_field_with_dash: you will have to use index func to access the field\nnote: direct access this field will trigger template rendering error\n"
      },
      "var_with_ifelse": "prod-web_app-HA",
      "var_with_print": "prodweb_app",
      "var_not_equal": "true",
      "managers": {
        "tom",
        "jason",
        "alice"
      },
      "ha": true,
      "var_with_and": "web_app",
      "admins": {
        "tom",
        "jason",
        "alice"
      },
      "var_with_if": "prod-web_app-HA",
      "var_with_range_item_simpler": " tom  jason  alice ",
      "ns": "prod",
      "age": 34,
      "var_with_not": "prod-web_app",
      "var_slice": "[jason]",
      "var_with_range": " x  x  x ",
      "var_greater_and_equal": "hello",
      "pod_name": "web_app",
      "old": 54,
      "var_not_equal_another_way": "true",
      "var_equal": "false",
      "out_of_normal_field_name": "this_is_a_field_with_dash: you will have to use index func to access the field\nnote: direct access this field will trigger template rendering error\n",
      "var_length": "12",
      "var_with_ifelse_multilines": "  prod-web_app-HA ",
      "var_with_range_item": " tom  jason  alice ",
      "var_test_log_auto_print_object": "prodweb_app",
      "var_commented": " prod-web_app",
      "var_space_trimmed": "prod-web_app",
      "var_commented_trimmed": "prod-web_app",
      "var_with_not_object": "prod-web_app",
      "var_slice_index": "jason",
      "var_space_not_trimmed": "prod       -            web_app",
      "var_with_or": "prod",
      "var_test_log_auto_print": "prodweb_app",
      "var_greater": "false",
      "template_def": "\n\n\nONE TWO\"\n",
      "instance_full_name": "prod-web_app"
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "var_with_print": "prodweb_app",
      "var_with_range_item_simpler": " tom  jason  alice ",
      "var_commented_trimmed": "prod-web_app",
      "var_with_not_object": "prod-web_app",
      "var_with_range_item": " tom  jason  alice ",
      "var_test_log_auto_print": "prodweb_app",
      "var_with_ifelse": "prod-web_app-HA",
      "managers": {
        "tom",
        "jason",
        "alice"
      },
      "var_length": "12",
      "var_test_log_auto_print_object": "prodweb_app",
      "pod_name": "web_app",
      "template_def": "\n\n\nONE TWO\"\n",
      "instance_full_name": "prod-web_app",
      "admins": {
        "tom",
        "jason",
        "alice"
      },
      "var_slice": "[jason]",
      "var_greater_and_equal": "hello",
      "var_with_or": "prod",
      "var_not_equal": "true",
      "var_with_and": "web_app",
      "var_with_if": "prod-web_app-HA",
      "var_greater": "false",
      "var_with_not": "prod-web_app",
      "old": 54,
      "var_space_not_trimmed": "prod       -            web_app",
      "age": 34,
      "var_with_range": " x  x  x ",
      "var_with_ifelse_multilines": "  prod-web_app-HA ",
      "var_commented": " prod-web_app",
      "var_space_trimmed": "prod-web_app",
      "var_slice_index": "jason",
      "ha": true,
      "ns": "prod",
      "var_not_equal_another_way": "true",
      "out_of_normal_field_name": "this_is_a_field_with_dash: you will have to use index func to access the field\nnote: direct access this field will trigger template rendering error\n",
      "fieldnames": {
        "name-with-dash": "this_is_a_field_with_dash: you will have to use index func to access the field\nnote: direct access this field will trigger template rendering error\n"
      },
      "var_equal": "false"
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "out_of_normal_field_name": "this_is_a_field_with_dash: you will have to use index func to access the field\nnote: direct access this field will trigger template rendering error\n",
      "var_commented": " prod-web_app",
      "var_space_trimmed": "prod-web_app",
      "var_slice_index": "jason",
      "ha": true,
      "ns": "prod",
      "var_not_equal_another_way": "true",
      "fieldnames": {
        "name-with-dash": "this_is_a_field_with_dash: you will have to use index func to access the field\nnote: direct access this field will trigger template rendering error\n"
      },
      "var_equal": "false",
      "var_with_print": "prodweb_app",
      "var_with_range_item_simpler": " tom  jason  alice ",
      "var_test_log_auto_print_object": "prodweb_app",
      "var_commented_trimmed": "prod-web_app",
      "var_with_not_object": "prod-web_app",
      "var_with_range_item": " tom  jason  alice ",
      "var_test_log_auto_print": "prodweb_app",
      "var_with_ifelse": "prod-web_app-HA",
      "managers": {
        "tom",
        "jason",
        "alice"
      },
      "var_length": "12",
      "var_greater_and_equal": "hello",
      "pod_name": "web_app",
      "template_def": "\n\n\nONE TWO\"\n",
      "instance_full_name": "prod-web_app",
      "admins": {
        "tom",
        "jason",
        "alice"
      },
      "var_slice": "[jason]",
      "var_with_or": "prod",
      "var_not_equal": "true",
      "var_with_and": "web_app",
      "var_with_if": "prod-web_app-HA",
      "var_greater": "false",
      "var_with_not": "prod-web_app",
      "old": 54,
      "var_space_not_trimmed": "prod       -            web_app",
      "age": 34,
      "var_with_range": " x  x  x ",
      "var_with_ifelse_multilines": "  prod-web_app-HA "
    })
    
    cmd( 1):
    echo "{{.instance_full_name}}"
    
    cmd=>:
    echo "prod-web_app"<=
    prod-web_app
     .. ok
    cmd( 2):
    echo "{{.var_space_not_trimmed}}"
    
    cmd=>:
    echo "prod       -            web_app"<=
    prod       -            web_app
     .. ok
    cmd( 3):
    echo "{{.var_space_trimmed}}"
    
    cmd=>:
    echo "prod-web_app"<=
    prod-web_app
     .. ok
    cmd( 4):
    echo "{{.var_commented}}"
    
    cmd=>:
    echo " prod-web_app"<=
    prod-web_app
     .. ok
    cmd( 5):
    echo "{{.var_commented_trimmed}}"
    
    cmd=>:
    echo "prod-web_app"<=
    prod-web_app
     .. ok
    cmd( 6):
    echo "{{.var_with_if}}"
    
    cmd=>:
    echo "prod-web_app-HA"<=
    prod-web_app-HA
     .. ok
    cmd( 7):
    echo "{{.var_with_ifelse}}"
    
    cmd=>:
    echo "prod-web_app-HA"<=
    prod-web_app-HA
     .. ok
    cmd( 8):
    echo "{{.var_with_ifelse_multilines}}"
    
    cmd=>:
    echo "  prod-web_app-HA "<=
    prod-web_app-HA
     .. ok
    cmd( 9):
    echo "{{.var_with_not}}"
    
    cmd=>:
    echo "prod-web_app"<=
    prod-web_app
     .. ok
    cmd(10):
    echo "{{.var_with_not_object}}"
    
    cmd=>:
    echo "prod-web_app"<=
    prod-web_app
     .. ok
    cmd(11):
    echo "{{.var_length}}"
    
    cmd=>:
    echo "12"<=
    12
     .. ok
    cmd(12):
    echo "{{.var_with_or}}"
    
    cmd=>:
    echo "prod"<=
    prod
     .. ok
    cmd(13):
    echo "{{.var_with_print}}"
    
    cmd=>:
    echo "prodweb_app"<=
    prodweb_app
     .. ok
    cmd(14):
    echo "check the value of other dvar using vvvv flag print out"
    
    cmd=>:
    echo "check the value of other dvar using vvvv flag print out"<=
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
