# GooglePlacesAutocomplete

[![Build Status](http://img.shields.io/travis/watsonbox/ios_google_places_autocomplete.svg?style=flat)](https://travis-ci.org/watsonbox/ios_google_places_autocomplete)

A simple [Google Places API](https://developers.google.com/places/documentation/autocomplete) autocompleting address entry view for iOS devices.

There are already a couple of solutions out there for this. GooglePlacesAutocomplete is different because it is 100% Swift, and aims to provide the simplest possible method of entering validated, autocompleted addresses. No attempt has been made to integrate MapKit since displaying Google Places on a non-Google map is against their terms of service.

<table width="100%">
  <tr>
    <td align="left"><img src="Screenshots/view.png"/></td>
    <td align="right"><img src="Screenshots/search.png"/></td>
  </td>
</table>

----------


## Requirements

- iOS 8.0+
- XCode 6.1


## Installation

Simply copy `GooglePlacesAutocomplete.swift` and `GooglePlacesAutocomplete.xib` to your project.

Framework / CocoaPod to follow.

Note: Don't forget to add the PoweredByGoogle image to your xcassets.


## Usage

```swift
let gpaViewController = GooglePlacesAutocomplete(
  apiKey: "[YOUR GOOGLE PLACES API KEY]",
  placeType: .Address
)

gpaViewController.placeDelegate = self // Conforms to GooglePlacesAutocompleteDelegate

presentViewController(gpaViewController, animated: true, completion: nil)
```

`GooglePlacesAutocompleteDelegate` supports two methods:

- `placeSelected(place: Place)`: Invoked when a new place is selected
- `placeViewClosed()`: Invoked when the view is closed

Here's a [complete example](https://github.com/watsonbox/ios_google_places_autocomplete/blob/master/GooglePlacesAutocomplete/ViewController.swift).


## Contributing

1. Fork it ( https://github.com/watsonbox/ios-google-places-autocomplete/fork )
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create a new Pull Request