# Exemple de code pour l'integration de FeexPay dans un projet Laravel


## 1. Installation du package avec composer

```php
composer require feexpay/feexpay-php
```

## 2. Ajout du code exemple pour le bouton

```php
<div id='button_payee'></div>
@php
    $price = 50;
    $id= "shop's id";
    $token= "token key api";
    $callback_url= 'https://www.google.com';
    $error_callback_url= 'https://www.google.com';
    $mode='LIVE';
    $feexpayclass = new Feexpay\FeexpayPhp\FeexpayClass($id, $token, $callback_url, $mode, $error_callback_url);
    $result = $feexpayclass->init($price, "button_payee", false, "", "votre description", "votre callback_info")
@endphp
```
Vous ajoutez ce code dans votre fichier .blade.php (ex: welcome.blade.php) en y mettant votre shop'id et le token key de votre compte.
Ce code vous permet de faire apparaitre directement le bouton de paiement dans votre interface.

