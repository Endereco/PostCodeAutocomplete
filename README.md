# PostCodeAutocomplete

Assists input for post code in the checkout or registration form. When the user enters the first characters of a post code, a dropdown with zip code variants appears.
Its possible to click on one of the varaints or to navigate with keyboard arrows and press enter to select one. The selected variant is copied to the input field.

It makes the entry of postal code faster and allows the user to double check the post code.

## Installation

In order to pull the latest version:

### npm (preferred)

```
npm i @endereco/postcodeautocomplete
```

### github

```
git clone https://github.com/Endereco/PostCodeAutocomplete.git
```

Then include PostCodeAutocomplete.js in `<header>` or before config.

## Configuration

In order to use postcode autocomplete you must specify the fields that make the postcode, city name and country and some colors.

Here is an example configuration:

```

new PostCodeAutocomplete({
    'inputSelector': 'input[name="register[billing][zipcode]"]',
    'secondaryInputSelectors': {
        'cityName': 'input[name="register[billing][city]"]',
        'country': 'select[name="register[billing][country]"]'
    },
    'endpoint': 'https://example-domain.com/endpoint',
    'apiKey': '041c3c302746cf37722560a7a285690738a7db4e55b7aaf26a545ffabd318a83',
    'colors' : {
        'primaryColor' => '#fff',
        'primaryColorHover' => '#fff',
        'primaryColorText' => '#fff',
        'secondaryColor' => '#fff',
        'secondaryColorHover' => '#fff',
        'secondaryColorText' => '#fff',
        'warningColor' => '#fff',
        'warningColorHover' => '#fff',
        'warningColorText' => '#fff',
        'successColor' => '#fff',
        'successColorHover' => '#fff',
        'successColorText' => '#fff'
    }
});
```

## Dependencies

PostCodeAutocomplete relies on StatusIndicator to mark fields green on correct input.

PostCodeAutocomplete also relies on Accounting to generate the tid and track transactions.
