# Ever Gauzy Java SDK

Official Java SDK for the [Ever Gauzy](https://gauzy.co) API, auto-generated using [Microsoft Kiota](https://learn.microsoft.com/en-us/openapi/kiota/).

## Installation

### Maven

```xml
<dependency>
    <groupId>co.ever.gauzy</groupId>
    <artifactId>ever-gauzy-sdk</artifactId>
    <version>0.1.0</version>
</dependency>
```

### Gradle

```groovy
implementation 'co.ever.gauzy:ever-gauzy-sdk:0.1.0'
```

## Quick Start

```java
import co.ever.gauzy.sdk.EverGauzyApiClient;
import com.microsoft.kiota.http.OkHttpRequestAdapter;
import com.microsoft.kiota.authentication.AnonymousAuthenticationProvider;

// Create the API client
var authProvider = new AnonymousAuthenticationProvider();
var adapter = new OkHttpRequestAdapter(authProvider);
adapter.setBaseUrl("https://api.gauzy.co");
var client = new EverGauzyApiClient(adapter);

// Example: List employees
var employees = client.api().employee().get();
```

## Authentication

The Gauzy API supports multiple authentication methods:

- **Bearer Token (JWT)**: For user-authenticated requests
- **API Key**: Via `X-API-Key` header
- **OAuth2**: Authorization code flow

## API Documentation

- **Swagger UI**: https://api.gauzy.co/swg
- **Scalar Docs**: https://api.gauzy.co/docs
- **OpenAPI Spec**: https://api.gauzy.co/swg-json

## Development

```bash
git clone https://github.com/ever-co/ever-gauzy-sdk-java.git
cd ever-gauzy-sdk-java
mvn compile
mvn test
```

## SDK Generation

This SDK is auto-generated from the Ever Gauzy OpenAPI specification using Microsoft Kiota.
To regenerate, trigger the "Generate SDK" GitHub Action workflow.

## License

This SDK is licensed under the [MIT](LICENSE) license.

## Links

- [Ever Gauzy](https://gauzy.co)
- [API Documentation](https://docs.gauzy.co)
- [GitHub](https://github.com/ever-co/ever-gauzy)
