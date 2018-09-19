# institution
* [TENANT_ID](#tenant_id) [1] **
* [TENANT_NAME](#tenant_name) [0..1]
* [UDD_VERSION](#udd_version) [1]
* [MODULE_VLE_MAP_MODE](#module_vle_map_mode) [0..1]
* [PROVIDED_AT](assessment_instance.md#provided_at) [0..1]

\** indicates that the property is the primary key for this entity.

API endpoint name: **institution**

## Description of institution entity
An institution is the overall provider of one or more courses.  Example: University of Gloucestershire.

## TENANT_ID
### Description
This field records the unique identifier for the University College concerned - using the UK Provider Reference Number (UKRPN) which is the unique identifier allocated to institutions by the UK Register of Learning Providers (UKRLP).

### Purpose
To identify the organisation.

### Derivation
UK Register of Learning Providers (UKRLP).

### References

### Format
String (8)

### Notes
Further information (on UKPRN) available at www.ukrlp.co.uk


## TENANT_NAME
### Description
Institution's official legal name. This should match the name indicated in the UKRLP database, as used for TENANT_ID.

### Purpose
To identify the organisation.

### Derivation
Institution

### References

### Format
String (255)

### Notes
Omitting this property could impair the functionality of analytics applications such as student apps or dashboards.

## UDD_VERSION
### Description
Version number of this UDD specification.

### Purpose
Enables the UDD to be self-declaring of its version.

### Derivation
UDD specification in use by the institution

### References

### Format
String (8)

### Notes
Value will be the current version number of the UDD preceded by "v".  Example: if the data uses UDD v1.4.0, value will "v1.4.0".

## MODULE_VLE_MAP_MODE
### Description
This property enables an institution to specify the type of relationship between the module_instance in the Student Record System and module information in the VLE, identified by MOD_INSTANCE_ID and VLE_MOD_ID respectively. By default, MOD_INSTANCE_ID plus VLE_MOD_ID form a unique constraint in module_VLE_map, which supports a many-to-many relationship between them.

If absent or "0", then MOD_INSTANCE_ID plus VLE_MOD_ID form a unique constraint in module_VLE_map.

If "1", then MOD_INSTANCE_ID values in module_VLE_map must be unique.

### Purpose
To enable the constraints on the module_VLE_map entity to be varied between institutions.

### Derivation
Jisc

### Valid Values
0 or 1

### Format
Int

### Notes
If MODULE_VLE_MAP_MODE is absent, a default value of 0 for this property will be assumed. This property value can be supplied explicitly, if desired.
Also see the [module_VLE_map](module_vle_map.md) entity.
