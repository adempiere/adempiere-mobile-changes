# ADempiere Mobile Changes

A project to make dictionary changes from ADempiere and reuse some entities inside mobile application


## Badges

Add badges from somewhere like: [shields.io](https://shields.io/)

[![GPLv3 License](https://img.shields.io/badge/License-GPL%20v3-yellow.svg)](https://opensource.org/licenses/)


## Requirements
- [JDK 11 or later](https://adoptium.net/)
- [Gradle 8.0.1 or later](https://gradle.org/install/)


### Packages Names
The main package name is `org.spin.mobile` by your implementation

```Java
org.spin.mobile.model.validator
org.spin.mobile.setup
org.spin.mobile.util
```

### Model Validators
Change the `org.spin.mobile.model.validator.Validator` by your implementation, example: `org.spin.mobile.model.validator.MyOwnFunctionality`

### Model Deploy class
Change the `org.spin.mobile.setup.Deploy` by your implementation, example: `org.spin.mobile.setup.MyOwnSetupForDeploy`

### Model Util class for core changes
Change the `org.spin.mobile.util.Changes` by your implementation, example: `org.spin.mobile.util.MyOwnChanges`

## Core Changes

The main core changes is some elements and columns added to identify mobile entities.

### Entity Type

- Code: `MOBILE`
- Name: `Spin Contribution (Mobile Support)`
- Model Package: `org.spin.mobile.model` 

### Elements

- DB Column Name: `MOBILE_IsMobile`
- Name: `Mobile Feature`
- Type: `Yes-No`

### Column Changes

- Table: `AD_Form` 
  - `MOBILE_IsMobile`
  - `MOBILE_Slug`
  - `MOBILE_ImageURL`
  
- Table: `AD_User`
  - `MOBILE_IsMobile`
- Table: `AD_Role`
  - `MOBILE_IsMobile`


## Binary Project

You can get all binaries from github [here](https://central.sonatype.com/artifact/io.github.adempiere/adempiere-mobile-changes/1.0.0).

All contruction is from github actions


## Some XML's:

All dictionary changes are writing from XML and all XML's hare `xml/migration`


## How to add this library?

Is very easy.

- Gradle

```Java
implementation 'io.github.adempiere:adempiere-mobile-changes:1.0.0'
```

- SBT

```
libraryDependencies += "io.github.adempiere" % "adempiere-mobile-changes" % "1.0.0"
```

- Apache Maven

```
<dependency>
    <groupId>io.github.adempiere</groupId>
    <artifactId>adempiere-mobile-changes</artifactId>
    <version>1.0.0</version>
</dependency>
```