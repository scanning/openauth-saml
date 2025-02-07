# @scanning/openauth-saml

SAML (browser-post) provider for OpenAuth.

## Features

- Easy integration with OpenAuth
- Type-safe implementation using TypeScript

## Installation

```bash
npm install @scanning/openauth-saml
```

## Usage

```typescript
import { authorizer } from "@openauthjs/openauth"
import { SamlAdapter } from "@openauthjs/openauth/adapter/saml"

export default authorizer({
  providers: {
    saml: SamlAdapter({
      idpCert: 'MIIDpjCCAo6gAwIBAgIGAZPxVe/7MA0GCSqGSIb3DQEBCwUAMIGTMQswCQYDVQQGEwJVUzETMBEGA1UECAwKQ2FsaWZvcm5pYTEWMBQGA1UEBwwNU2FuIEZyYW5jaXNjbzENMAsGA1UECgwET2t0YTEUMBIGA1UECwwLU1NPUHJvdmlkZXIxFDASBgNVBAMMC2Rldi03NjgzMzc5MRwwGgYJKoZIhvcNAQkBFg1pbmZvQG9rdGEuY29tMB4XDTI0MTIyMzAyMjUwMVoXDTM0MTIyMzAyMjYwMVowgZMxCzAJBgNVBAYTAlVTMRMwEQYDVQQIDApDYWxpZm9ybmlhMRYwFAYDVQQHDA1TYW4gRnJhbmNpc2NvMQ0wCwYDVQQKDARPa3RhMRQwEgYDVQQLDAtTU09Qcm92aWRlcjEUMBIGA1UEAwwLZGV2LTc2ODMzNzkxHDAaBgkqhkiG9w0BCQEWDWluZm9Ab2t0YS5jb20wggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQCkeCKYAi+Fhjw/8XXfPrLmFQGkAG43AD5L57ODvdQozYai1hCTxIc/m+9TiuaeS+Ujq9DuSqfdg5JypZ+tmk4btFyj8NwHUV1gUgnY/yHIzGxGwuMGlb5PlVASN4pCvOSsEApjolGOnHV0OyKmGJPB8HlIarEYC9oKh2TByq8O+fJbaTs0ifWlg1xTE8emPhE/QQKzSZKccwaZC5eo/0R+tt7J5r4qCjki1wtPRYDQPh7mNoJ+EjBtnPEAJiHvA5Jn1K0EuHf07OC3in91j0boPzh1vlgXI3//P/BVDkTUuyindFh/gdkhVEDXISI9yqqGrWJ8kSHOUdoEYBvbFTORAgMBAAEwDQYJKoZIhvcNAQELBQADggEBAGPVYctYWJTM7tkvjdDo9S2KAOMcEG4O+elz2IuXXnkjQiLLQx98HUm6PT35EEr/3rNpMviHRjC2s5V4P3I9/LKg3VyNVli8KoFjFX5166PqL2cJpfo8vwe3WYwY9skWqvrYvaPUiQrio6g+TsVpsUkIj3wwAJHGFgQnTykHSMi4lWgWNIIrWGfd9fivqFhbc7F41wt/zr+hB32Nl1EYNb51dlQhVLB4lVm4JQXkzJ7VJeJkk46E72noiU6tyIN0HKVoEvERm+nmZOLbjvRuR7GprE4/JiDJI76rgUjOTPFz77ZvfiONw0gwHlmDalgusm+DTXoqqsNSQIMYR2WMeXs=',
      idpIssuer: 'http://www.okta.com/exkm2znudk4iKZc3u5d7',
      idpSignonUrl: 'https://dev-7683379.okta.com/app/dev-7683379_openauthjs_1/exkm2znudk4iKZc3u5d7/sso/saml'
    }) 
  },
})
```

## Configuration Options

| Option                   | Type           | Description                                               |
| ------------------------ | -------------- | --------------------------------------------------------- |
| `idpCert`                | `string`       | X.509 certificate (in string format)                      |
| `idpIssuer`              | `string`       | Identity Provider issuer URL                              |
| `idpSignonUrl`           | `string`       | Identity Provider sign-on URL                             |

## License

MIT