# Magento Captcha for Magento 1.6.x

This implementation ripped from Magento 1.9.

Additional code placed under `local` code pool.

`captcha.xml` has additional instructions to change templates of necessary blocks to avoid modification of original templates at store frontend.

Unfortunatly it is not the case with admin login page. Magento 1.6 creates 'login' block and 'forgor password' block programatically in controller. That is why there no other way than overwrite original templates for those blocks:

```
app/design/adminhtml/default/default/template/forgotpassword.phtml
app/design/adminhtml/default/default/template/login.phtml
```


#Install

```bash
cd <magento_root>
composer config repositories.tangar76/magento1-zend-captcha vcs git@github.com:tangar76/magento1-zend-captcha.git
composer require tangar76/magento1-zend-captcha
```
