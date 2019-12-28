# omise_flutter

A package for integrating Omise API

## Getting Started

### Create a token

```
create(String name, String number, String expirationMonth,
      String expirationYear, String securityCode,
      {String city,
      String country,
      String postalCode,
      String state,
      String street1,
      String street2,
      String phoneNumber})
```

** Usage **

```
OmiseFlutter omise = OmiseFlutter(YOUR_PUBLIC_KEY);
final response = await omise.token.create("John Doe", "4242424242424242", "12", "2020", "123");
```

### Create a source

```
create(int amount, String currency, String type,
      {String barcode,
      String email,
      int installmentTerm,
      String name,
      String storeId,
      String storeName,
      String terminalId,
      String phoneNumber,
      bool zeroInterestInstallments})
```

** Usage **

```
OmiseFlutter omise = OmiseFlutter(YOUR_PUBLIC_KEY);
final response = await omise.source.create(10000, "thb", "internet_banking_bay");
```

### Retrieve a capability

```
retrieve()
```

** Usage **

```
OmiseFlutter omise = OmiseFlutter(YOUR_PUBLIC_KEY);
final response = await omise.capability.retrieve();
```