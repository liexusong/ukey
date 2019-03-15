Atom
====
Based on the Twitter Snowflake algorithm

### PHP unique ID generator

functions list:
* 1) string <b>atom_next_id</b>(void);<br />
&nbsp;&nbsp;&nbsp;Get the next unique ID.<br />
* 2) array <b>atom_explain</b>(string ID);<br />
&nbsp;&nbsp;&nbsp;Change unique ID to array includes: timestamp, datacenter id and worker id.<br />

### example:
```php
<?php
$id = atom_next_id();
echo $id;

$info = atom_explain($id);
echo date('Y-m-d H:i:s', $info['timestamp']);
?>
```

### install:
```
$  cd ./atom
$  phpize
$  ./configure
$  make
$  sudo make install
```

### php.ini configure entries:
```
[atom]
atom.datacenter = integer
atom.worker = integer
atom.twepoch = uint64
```
