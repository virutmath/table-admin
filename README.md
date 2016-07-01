# table-admin

* Stand-alone TableAdmin for project
* Using Bootstrap style, `iCheck`, `select2` class
* Support pagination for table

**Usage**

```
$config = [
    'show' => [
        'id' => true
    ],
    'formatDate' => 'd/m/Y',
    'defaultOptionLabel' => '',
    'pageSize' => 30,
    'module'=>'',
    'idField'=>'id',
];
$categories = [
  1=>'Category 1',
  2=>'Category 2'
];
$listRecord = [
  [
    'id'=>1,
    'name'=>'Jame Doe',
    'category_id'=>1
    'active'=>1
  ],
  [
    'id'=>2,
    'name'=>'Joe Doe',
    'category_id'=>2
    'active'=>0
  ]
];

$table = new TableAdmin($listRecord,$config);
$table->column('id','ID record','text');
$table->columnDropdown('category_id','Category',$categories);
$table->column('active','Active','checkbox');
$table->column('id','Edit','edit');
$table->column('id','Delete','delete');
echo $table->render();
```
