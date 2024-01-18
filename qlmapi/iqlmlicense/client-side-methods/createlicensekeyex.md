# CreateLicenseKeyEx

### Description

Creates a computer-bound license key.

```c#
string CreateLicenseKeyEx (ELicenseType licenseType, string machineID)
```

```c++
 _bstr_t CreateLicenseKeyEx (ELicenseType LicenseType, BSTR MachineID)
```

### Arguments

| Name        |                            Data Type                            | Description                                                                                                                                                                                                                                                                                                                                      |
| ----------- | :-------------------------------------------------------------: | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| licenseType | [ELicenseType](https://soraco.readme.io/reference/elicensetype) | Specify the type of license to generate.                                                                                                                                                                                                                                                                                                         |
| machineID   |                              string                             | A unique identifier for the machine. If you specify a ComputerName as the LicenseType, this argument must be the Computer Name. If you specify User Defined as the LicenseType, this argument can be anything you want. When validating the license key in your code, you will need to provide the same value to the ValidateLicenseEx function. |

### Return

| Type   | Description                  |
| ------ | ---------------------------- |
| string | a computer-bound license key |

## Remarks

Prior to calling this function, you must call DefineProduct and set the PrivateKey property. Note that including the PrivateKey in your code is not recommended. Creation of license keys should never be done from within the application but rather from a server that the user does not have access to.
