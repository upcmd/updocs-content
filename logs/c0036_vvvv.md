---
title: "c0036_vvvv"
date: 2020-08-09T01:36:04+88:00
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
                 Timeout -> 3600000
     MaxModuelCallLayers -> 256
     :release version:  1.0.0
     :verbose level:  vvvv
    work dir: /up_project/up
    -exec task: task
    loading [Task]:  ./tests/functests/c0036
    module: [self], instance id: [dev], exec profile: []
    profile -  envVars:
    
    (*core.Cache)({
    })
    
    ---------group vars----------
    
    global: {
    }
    
    
    groups members:[]
    merged[ dev ] runtime vars:
    {
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
      },
      "fieldnames": {
        "name-with-dash": "this_is_a_field_with_dash: you will have to use index func to access the field\nnote: direct access this field will trigger template rendering error\n"
      },
      "ns": "prod",
      "pod_name": "web_app"
    }
    
    dvar> var_with_range:
    " x  x  x "
    
    -
     x  x  x 
    dvar> var_with_range_item:
    " tom  jason  alice "
    
    -
     tom  jason  alice 
    dvar> var_with_range_item_simpler:
    " tom  jason  alice "
    
    -
     tom  jason  alice 
    dvar> var_test_log_auto_print:
    "prodweb_app"
    
    -
    prodweb_app
    dvar[object]> var_test_log_auto_print_object:
    "prodweb_app"
    
    dvar> var_with_and:
    "web_app"
    
    -
    web_app
    dvar> var_slice_index:
    "jason"
    
    -
    jason
    dvar> out_of_normal_field_name:
    "this_is_a_field_with_dash: you will have to use index func to access the field\nnote: direct access this field will trigger template rendering error\n"
    
    -
    this_is_a_field_with_dash: you will have to use index func to access the field
    note: direct access this field will trigger template rendering error
    
    dvar> var_slice:
    "[jason]"
    
    -
    [jason]
    dvar> var_equal:
    "false"
    
    -
    false
    dvar> var_not_equal:
    "true"
    
    -
    true
    dvar> var_not_equal_another_way:
    "true"
    
    -
    true
    dvar> var_greater:
    "false"
    
    -
    false
    dvar> var_greater_and_equal:
    "true"
    
    -
    true
    dvar> var_greater_and_equal:
    "hello"
    
    -
    hello
    dvar> var_use_and_operator:
    "true"
    
    -
    true
    dvar> var_use_or_operator:
    "true"
    
    -
    true
    dvar> var_concat_values:
    "web_app: 34 years old"
    
    -
    web_app: 34 years old
    dvar> template_def:
    "\n\n\nONE TWO\"\n"
    
    -
    
    
    
    ONE TWO"
    
    -------runtime global final merged with dvars-------
    
    {
      "var_test_log_auto_print_object": "prodweb_app",
      "age": 34,
      "out_of_normal_field_name": "this_is_a_field_with_dash: you will have to use index func to access the field\nnote: direct access this field will trigger template rendering error\n",
      "template_def": "\n\n\nONE TWO\"\n",
      "var_with_and": "web_app",
      "var_use_and_operator": "true",
      "var_commented_trimmed": "prod-web_app",
      "var_with_ifelse": "prod-web_app-HA",
      "var_slice_index": "jason",
      "ha": true,
      "managers": {
        "tom",
        "jason",
        "alice"
      },
      "var_length": "12",
      "var_commented": " prod-web_app",
      "var_with_not": "prod-web_app",
      "var_greater_and_equal": "hello",
      "var_space_trimmed": "prod-web_app",
      "var_greater": "false",
      "var_not_equal": "true",
      "var_slice": "[jason]",
      "var_test_log_auto_print": "prodweb_app",
      "var_with_range_item_simpler": " tom  jason  alice ",
      "old": 54,
      "var_with_print": "prodweb_app",
      "var_equal": "false",
      "var_with_not_object": "prod-web_app",
      "var_with_ifelse_multilines": "  prod-web_app-HA ",
      "var_space_not_trimmed": "prod       -            web_app",
      "var_use_or_operator": "true",
      "var_concat_values": "web_app: 34 years old",
      "pod_name": "web_app",
      "fieldnames": {
        "name-with-dash": "this_is_a_field_with_dash: you will have to use index func to access the field\nnote: direct access this field will trigger template rendering error\n"
      },
      "admins": {
        "tom",
        "jason",
        "alice"
      },
      "var_with_range": " x  x  x ",
      "var_with_range_item": " tom  jason  alice ",
      "var_with_if": "prod-web_app-HA",
      "var_not_equal_another_way": "true",
      "instance_full_name": "prod-web_app",
      "ns": "prod",
      "var_with_or": "prod"
    }
    
      located task-> 1 [task]: 
    Task1: [task ==> task:  ]
    Executing task stack layer: 1
    
    -Step1:
    current exec runtime vars:
    (*core.Cache)({
      "managers": {
        "tom",
        "jason",
        "alice"
      },
      "var_greater": "false",
      "var_with_ifelse_multilines": "  prod-web_app-HA ",
      "var_equal": "false",
      "instance_full_name": "prod-web_app",
      "age": 34,
      "var_commented_trimmed": "prod-web_app",
      "out_of_normal_field_name": "this_is_a_field_with_dash: you will have to use index func to access the field\nnote: direct access this field will trigger template rendering error\n",
      "var_with_ifelse": "prod-web_app-HA",
      "template_def": "\n\n\nONE TWO\"\n",
      "var_with_range_item_simpler": " tom  jason  alice ",
      "var_with_print": "prodweb_app",
      "var_with_if": "prod-web_app-HA",
      "var_with_and": "web_app",
      "var_greater_and_equal": "hello",
      "pod_name": "web_app",
      "var_use_or_operator": "true",
      "var_with_range_item": " tom  jason  alice ",
      "var_commented": " prod-web_app",
      "old": 54,
      "var_space_not_trimmed": "prod       -            web_app",
      "var_with_or": "prod",
      "ha": true,
      "var_use_and_operator": "true",
      "var_test_log_auto_print": "prodweb_app",
      "fieldnames": {
        "name-with-dash": "this_is_a_field_with_dash: you will have to use index func to access the field\nnote: direct access this field will trigger template rendering error\n"
      },
      "var_concat_values": "web_app: 34 years old",
      "admins": {
        "tom",
        "jason",
        "alice"
      },
      "var_test_log_auto_print_object": "prodweb_app",
      "var_with_not": "prod-web_app",
      "var_space_trimmed": "prod-web_app",
      "var_not_equal": "true",
      "var_slice": "[jason]",
      "var_with_not_object": "prod-web_app",
      "ns": "prod",
      "var_not_equal_another_way": "true",
      "var_slice_index": "jason",
      "var_length": "12",
      "var_with_range": " x  x  x "
    })
    
    self: final context exec vars:
    
    (*core.Cache)({
      "pod_name": "web_app",
      "var_use_or_operator": "true",
      "var_with_range_item": " tom  jason  alice ",
      "var_commented": " prod-web_app",
      "old": 54,
      "var_space_not_trimmed": "prod       -            web_app",
      "var_with_or": "prod",
      "ha": true,
      "var_use_and_operator": "true",
      "var_test_log_auto_print": "prodweb_app",
      "fieldnames": {
        "name-with-dash": "this_is_a_field_with_dash: you will have to use index func to access the field\nnote: direct access this field will trigger template rendering error\n"
      },
      "var_concat_values": "web_app: 34 years old",
      "admins": {
        "tom",
        "jason",
        "alice"
      },
      "var_test_log_auto_print_object": "prodweb_app",
      "var_with_not": "prod-web_app",
      "var_space_trimmed": "prod-web_app",
      "var_not_equal": "true",
      "var_slice": "[jason]",
      "var_with_not_object": "prod-web_app",
      "ns": "prod",
      "var_not_equal_another_way": "true",
      "var_slice_index": "jason",
      "var_length": "12",
      "var_with_range": " x  x  x ",
      "managers": {
        "tom",
        "jason",
        "alice"
      },
      "var_greater": "false",
      "var_with_ifelse_multilines": "  prod-web_app-HA ",
      "var_equal": "false",
      "instance_full_name": "prod-web_app",
      "age": 34,
      "var_commented_trimmed": "prod-web_app",
      "out_of_normal_field_name": "this_is_a_field_with_dash: you will have to use index func to access the field\nnote: direct access this field will trigger template rendering error\n",
      "var_with_ifelse": "prod-web_app-HA",
      "template_def": "\n\n\nONE TWO\"\n",
      "var_with_range_item_simpler": " tom  jason  alice ",
      "var_with_print": "prodweb_app",
      "var_with_if": "prod-web_app-HA",
      "var_with_and": "web_app",
      "var_greater_and_equal": "hello"
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
