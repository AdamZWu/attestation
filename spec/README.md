# in-toto Attestation Framework Spec

Latest version: [v1.0-draft]

An **in-toto attestation** is authenticated metadata about one or more
software artifacts[^1]. The intended consumers are automated policy engines,
such as [in-toto-verify] and [Binary Authorization].

It has four layers that are independent but designed to work together:

-   [Predicate]: Contains arbitrary metadata about a subject artifact, with a
    type-specific schema.
-   [Statement]: Binds the attestation to a particular subject and
    unambiguously identifies the types of the predicate.
-   [Envelope]: Handles authentication and serialization.
-   [Bundle]: Defines a method of grouping multiple attestations together.

The [validation model] provides pseudocode showing how these layers fit
together. See the [documentation] for more background and examples.

[^1]: This is compatible with the [SLSA Attestation Model].

[Binary Authorization]: https://cloud.google.com/binary-authorization
[Bundle]: v1.0-draft/bundle.md
[Envelope]: v1.0-draft/envelope.md
[Predicate]: v1.0-draft/predicate.md
[SLSA Attestation Model]: https://slsa.dev/attestation-model
[Statement]: v1.0-draft/statement.md
[documentation]: ../docs
[in-toto-verify]: https://github.com/in-toto/in-toto#verification
[v1.0-draft]: v1.0-draft/README.md
[validation model]: ../../docs/validation.md
