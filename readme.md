#Inspector

Inspector - A PHP library that fetches the social accounts, website, name, photos, employment history and other details possible for the user by his email.

##Installation
You can install the library using the following ways:

##Using Composer
You can install this through <a href="http://getcomposer.org/">Composer</a>, a dependency manager for PHP. Just run the below command:

```
composer require zeeshanu/inspector
```

For further details you can find the package at <a href="https://packagist.org/packages/zeeshanu/inspector">Packagist</a>.

##Manual way
- Copy <code>src</code> to your codebase, perhaps to the vendor directory.
- Add the <code>Zeeshan\Inspector\Inspector</code> class to your autoloader or require the file directly.

##Getting Started
I'm going to use the following email address to demonstrate the usage of this php wrapper.

>ziishaned@gmail.com

```php
// Your FulContact API key https://portal.fullcontact.com/signup
$apiKey = "";

$inspector = new Inspector($apiKey);
$person = $inspector->getProfile("ziishaned@gmail.com");

$person->getPhotos();
$person->getContactInfo();
$person->getOrganizations();
$person->getDemographics();
$person->getSocialProfiles();
$person->getInterests();
$person->getEmail();
```

## Feedback
If you notice that there might be some improvements in code you can create a pull request or report an issue. You can also contact me at <a href="mailto:ziishaned@gmail.com">ziishaned@gmail.com</a>.

# Note
Please note that the library relies upon <a href="https://portal.fullcontact.com/signup">FullContact API</a> and you will need an API key to use this package.

## License
The MIT License (MIT). Please see [License File](LICENSE.md) for more information.
