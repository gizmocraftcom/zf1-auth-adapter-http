# Changelog

## 2.0.0

Fork of `diablomedia/zendframework1-auth-adapter-http`, published as `gizmocraft/zendframework1-auth-adapter-http`.

### Breaking changes

- Requires PHP `>=8.5`. Tested on PHP 8.5 and 8.6.
- Package renamed from `diablomedia/zendframework1-auth-adapter-http` to `gizmocraft/zendframework1-auth-adapter-http`. It now requires `gizmocraft/zendframework1-auth` `^2.0.0` and `gizmocraft/zendframework1-controller` `^2.0.0`.

### Other changes

- `Zend_Auth_Adapter_Http::__construct()` casts the `realm` and `digest_domains` config values to string before `ctype_print()`, because `ctype_print()` with a non-string argument is deprecated since PHP 8.1. No signature change.
- Dev dependencies upgraded (PHPUnit 13, PHPStan 2.3, php-cs-fixer 3.95, GrumPHP 2.27). Dropped `composer-require-checker`, which has no release for PHP 8.6.
- Tests migrated to PHPUnit 13 (attributes, `createStub()` instead of `getMockBuilder()` with `expects($this->any())`).
- CI runs PHP 8.5 and 8.6.
