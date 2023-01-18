# Wallet Usage

Configured Echo SDK alows users to receive Push Notifications on their devices about important events, like an auth request or a sign session request.

### Initial configurations

Make sure to configure Networking instance first:
- [Networking](../core/networking-configuration.md)

### Configure Client

1. get client id:

```swift
let clientId = try! Networking.interactor.getClientId()
```

2. call configuration method:

```swift
Echo.configure(clientId: clientId)
```

### Register device token

Communicate with Apple Push Notification service and receive unique device token. Register that token with following method:

```swift
try await Echo.instance.register(deviceToken: deviceToken)
```