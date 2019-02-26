# PHP _mt_rand()_ Function

>PHP 7.2 was leveraged to make the random values via a [Laravel 5.7](https://laravel.com) app framework running in a localhost [MAMP PRO 5.1.1](https://www.mamp.info/en/mamp-pro/) environment. Generated values were initially recorded to a [MySQL v5.7.23](https://www.mysql.com) database, then exported to CSV.

[PHP mt_rand() Docs](http://php.net/manual/en/function.mt-rand.php)

Per documentation: _"Generate a random value via the [Mersenne Twister](http://www.math.sci.hiroshima-u.ac.jp/~m-mat/MT/emt.html) Random Number Generator"_

```php
// Sample Laravel controller code to generate MT_RAND()
// batch1 values for fake earthquake entities

// Seed the algorithm. Apparently this is not needed
// in PHP 7.2 but I ran it anyway :)
mt_srand();

// loop
for ($i=0;$i<333857;++$i){
  // create a model
  $record = new Fakie;
  // make the values
  $record->fill([
    'batch' => 'b1',
    'month' => mt_rand(1,12),
    'marker' => mt_rand(1,16),
    'hour' => mt_rand(0, 23)
  ]);
  // save the model to the database
  $record->save();
}
```

## CSV Schema

The data is recorded in CSV files and organized in the following column schema (with headers):

| **1** _(row)_     | bat _(batch ID)_ | of12 _(choices)_ | of16 _(choices)_ | of24 _(choices)_ |
| ----------------- | :--------------: | :--------------: | :--------------: | :--------------: |
| **2**             |       'b1'       |    int 1 to 12   |    int 1 to 16   |    int 0 to 23   |
| **3**             |       'b1'       |    int 1 to 12   |    int 1 to 16   |    int 0 to 23   |
| **4**             |       'b1'       |    int 1 to 12   |    int 1 to 16   |    int 0 to 23   |
| more rows...      |        ...       |        ...       |        ...       |        ...       |
| **333358**        |       'b2'       |    int 1 to 12   |    int 1 to 16   |    int 0 to 23   |
| **333359**        |       'b2'       |    int 1 to 12   |    int 1 to 16   |    int 0 to 23   |
| even more rows... |        ...       |        ...       |        ...       |        ...       |
| **416103**        |       'b6'       |    int 1 to 12   |    int 1 to 16   |    int 0 to 23  
