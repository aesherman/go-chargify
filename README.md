# Chargify SDK

This library is a small wrapper around a subset of the Chargify API.

## Installation

Using your favorite dependency manager, make sure to add `github.com/getwagz/go-chargify`. For example, with dep,

`dep ensure -add github.com/getwagz/go-chargify`

## Usage

Usage is fairly straight-forward. See Configuration for more information about setting up and configuring the SDK.

## Environment Variables

* `CHARGIFY_ENV` set to production to actually make calls
* `CHARGIFY_API_KEY` Your secret API key
* `CHARGIFY_SUBDOMAIN` The subdomain for your account at Chargify

## Testing

Testing requires an actual account (nothing is mocked, but that could be a good addition!). Make sure your subdomain, api key, etc are properly set.

*IMPORTANT* If you run all of the tests, there isn't currently a way to delete the following entities. As such, you will need to handle that in the GUI until
a solution is provided in the official REST API:

* Product Family

## Other Libraries

We use the following additional tools in this library, and thank the maintainers and contributors of those libraries:

* [testify](https://github.com/stretchr/testify) - Makes our unit tests more readable and management

## Bugs

There is currently a bug in the Cyfe docs (as of 20180702). The docs mention that if onduplicate is set to replace, it would replace the data instead of accumulating. The behavior we are seeing is that passing anything for the field triggers the replacement, even if we send in a blank string.

## Implemented Endpoints

### Customers

* [Create Customer](https://reference.chargify.com/v1/customers/create-a-customer)
* [Delete Customer](https://reference.chargify.com/v1/customers/delete-the-customer)
* [Get Customers](https://reference.chargify.com/v1/customers/list-customers-for-a-site)
* [Search for Customers](https://reference.chargify.com/v1/customers/search-for-customer)

### Payment Profiles

* [Create Payment Profile](https://reference.chargify.com/v1/payment-profiles/create-a-payment-profile)
* [Delete Payment Profile](https://reference.chargify.com/v1/payment-profiles/delete-payment-profile)

### Product Families

* [Create Product Family](https://reference.chargify.com/v1/product-families/create-a-product)
* [Get Product Family](https://reference.chargify.com/v1/product-families/list-product-family-via-chargify-id)

### Products

* [Create a Product](https://reference.chargify.com/v1/products/create-a-product-1)
* [Archive a Product](https://reference.chargify.com/v1/products/archive-a-product)
* [Update a Product](https://reference.chargify.com/v1/products/update-a-product)
* [Get a Product By ID](https://reference.chargify.com/v1/products/read-the-product-via-chargify-id)
* [Get a Product By Handle](https://reference.chargify.com/v1/products/read-the-product-via-api-handle)
* [Get a Product In Family](https://reference.chargify.com/v1/products/list-products)

### Subscriptions

* [Create Subscription](https://reference.chargify.com/v1/subscriptions/create-subscription)
* [Cancel Subscription - Immediately](https://reference.chargify.com/v1/subscriptions-cancellations/cancel-subscription)
* [Cancel Subscription - Delayed](https://reference.chargify.com/v1/subscriptions-cancellations/cancel-subscription-delayed-method-1)
* [Remove Delayed Cancellation](https://reference.chargify.com/v1/subscriptions-cancellations/cancel-subscription-remove-delayed-method)

## Hiring

Are you on the New Hampshire Seacoast and love Go, Typescript, Swift, or Java? Send an email to engineering@wagz.com and let's find out if we're a good match!

## Contributing

Pull Requests are welcome! See our `CONTRIBUTING.md` file for more information.