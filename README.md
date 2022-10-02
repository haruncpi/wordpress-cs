# WPCS Setup Guideline

### 1. Install composer packages
```    
composer global require squizlabs/php_codesniffer
```
```
composer global require wp-coding-standards/wpcs
```
    
**Installation Test**: Run the below command for checking `phpcs` is installed correctly.

``` 
phpcs -i
```

**Problem Fix:** command not found: `phpcs`

To fix this problem, add the `phpcs` path to your PATH variable.

`phpcs` and `phpcbf` installed path.  
```
/Users/your_username/.composer/vendor/bin/phpcs
```
```
/Users/your_username/.composer/vendor/bin/phpcbf  
```
**[Note]** change  `your_username`  
### 2. Set WordPress as default coding standard
[Note] change `your_username`
    
```
phpcs --config-set installed_paths /Users/your_username/.composer/vendor/wp-coding-standards/wpcs
```

**Default Standard**
Set default CS

```
phpcs --config-set default_standard WordPress
```

**Installation Test**  
    
```
phpcs --config-show
```

### 3. To check a php file, run
    
```
phpcs abc.php
```

### 4. Run `phpcbf` for automatic fix, run

```
phpcbf abc.php
```

[Read about PHP CS for WordPress](https://developer.wordpress.org/coding-standards/wordpress-coding-standards/php/)
