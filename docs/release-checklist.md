# Release checklist

This is a preparation checklist, not proof of release.

- Verify exact starter, start prompt, revision date and full question-bank identity.
- Verify rights for every included file against LICENSE.md and release metadata. The authored guide and the seven named supporting texts use the approved CC BY 4.0 grant; code, repository configuration, branding, third-party assets and personal materials remain excluded.
- Check full repository history, secrets, private data and applicable platform protections on the exact intended publication scope.
- Complete relevant assistant startup, recovery, continuation and safety-effect checks; document capability limits.
- Obtain separate approval for the exact upload, repository visibility and immutable source ref.
- Verify anonymous source bytes and real assistant retrieval after approved exposure.
- Keep website deployment, production feedback, Google measurement, privacy, accessibility and performance gates separate.
- Begin localization only after the complete English journey is accepted.

Preserve previous source identities. Do not rewrite history, repoint published tags or delete old files as a shortcut.

## Guide metadata and publication status

`release.json` schema version 2 describes the immutable guide edition: its version,
revision date, filenames, integrity hashes and licenses. Its revision date is the
date assigned to the guide text, not a timestamp of a website deployment.

The `release_url` and `publication_status_url` fields point to the corresponding
GitHub Release and its public API record. GitHub supplies the actual `published_at`
timestamp and `draft` status. A tag alone is not a published GitHub Release.

Mutable fields such as `published_at`, `public_source_verified`,
`website_deployed` and `supported_hosts_verified` are not stored in the immutable
guide metadata. A publication record describes the checks actually completed and
their edition; it does not prove permanent website availability or universal
assistant compatibility.

For 0.19.1, assistant observations and performance measurements are retained from
0.19 and identified as such. The correction changes date/version metadata and
references; it does not introduce new method rules or question revisions.

Before closing a release, verify the agreed edition date across the guide,
metadata and website. After source and site acceptance, publish a GitHub Release
for the exact existing tag, select the intended latest version and confirm that
the entry appears in the Releases list. Creating a tag does not close this step.
