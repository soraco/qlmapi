# GetStatus

### Description

Returns the last license validation status. See [ELicenseStatus ](https://soraco.readme.io/reference/elicensestatus)for possible values.

```c#
int GetStatus ()
```

### Return

| Data Type | Description |
| :-------: | ----------- |
|    int    | the status  |

### Remarks

You must always call this function after calling ValidateLicense or ValidateLicenseEx to get the result of the validation.
