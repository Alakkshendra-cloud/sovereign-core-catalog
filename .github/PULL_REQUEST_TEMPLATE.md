## Description

<!-- What does this PR change and why? -->

## Type of change

- [ ] New component (software / hardware / service / AI model / company profile)
- [ ] Update to existing component
- [ ] Schema change (`schemas/`)
- [ ] Workflow / tooling change
- [ ] Documentation

## Checklist

### Metadata files
- [ ] All new/modified `metadata.yaml` and `profile.yaml` files conform to their schema
- [ ] `apiVersion` is `sovereign-catalog.io/v1alpha1`
- [ ] `kind` matches the correct type (`SoftwareListing`, `HardwareProfile`, `ServiceProfile`, `ModelListing`, `CompanyProfile`)
- [ ] `metadata.lifecycleStatus` is one of: `draft`, `review`, `approved`, `deprecated`, `retired`
- [ ] `metadata.storefrontVisibility` is one of: `public`, `unlisted`, `private`
- [ ] `metadata.availabilityState` is one of: `available_central_it`, `byop_ready`, `technical_assets_available`, `discoverable_only`

### Schema cross-references
- [ ] `metadata.category` uses a valid `softwareCategory` value (software listings only)
- [ ] `metadata.industries` entries use valid `industry` values
- [ ] `spec.jurisdiction.hq` / `ultimateParentCompanyHQ` in component `metadata.yaml` use a valid `componentsCountryEnum` value (`Global` is not allowed)
- [ ] `spec.jurisdiction.corporateHQ` / `ultimateParentCompanyHQ` in `profile.yaml` use a valid `companyProfileCountryEnum` value (`Global` is allowed)
- [ ] `spec.jurisdiction` may be omitted for software listings with no clear single owner (e.g. community-run open source); if present, `hq` is required
- [ ] Any `$ref` to `common-definitions.yaml` resolves to a defined `$defs` entry

### Security
- [ ] No secrets, credentials, or API keys included
- [ ] No hardcoded internal URLs or environment-specific values

## Affected components

<!-- List the files added or modified, e.g.:
- components/software/open-source/redis/v8.10.2/metadata.yaml
- companies/open-source/profile.yaml
-->

## Related issues

<!-- Closes # -->
