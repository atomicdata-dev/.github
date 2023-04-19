[![Atomic Data](https://raw.githubusercontent.com/ontola/atomic-data-docs/master/src/assets/atomic_data_logo_stroke.svg)](https://atomicdata.dev)

**Atomic Data is a modular specification for sharing, modifying and modeling graph data. It combines the ease of use of JSON, the connectivity of RDF (linked data) and the reliability of type-safety.**

Atomic Data uses links to connect pieces of data, and therefore makes it easier to connect datasets to each other - even when these datasets exist on separate machines.

## The specification

Atomic Data has been designed with [the following goals in mind](https://docs.atomicdata.dev/motivation.html):

- Give people more control over their data
- Make linked data easier to use
- Make it easier for developers to build highly interoperable apps
- Make standardization easier and cheaper

Atomic Data is [Linked Data](https://ontola.io/blog/what-is-linked-data/), as it is a [strict subset of RDF](https://docs.atomicdata.dev/interoperability/rdf.html).
It is type-safe (you know if something is a `string`, `number`, `date`, `URL`, etc.) and extensible through [Atomic Schema](https://docs.atomicdata.dev/schema/intro.html), which means that you can re-use or define your own Classes, Properties and Datatypes.

The default serialization format for Atomic Data is [JSON-AD](https://docs.atomicdata.dev/core/json-ad.html), which is simply JSON where each key is a URL of an Atomic Property.
These Properties are responsible for setting the `datatype` (to ensure type-safety) and setting `shortnames` (which help to keep names short, for example in JSON serialization) and `descriptions` (which provide semantic explanations of what a property should be used for).

Atomic Data has specifications for [authentication](https://docs.atomicdata.dev/authentication.html), [authorization](https://docs.atomicdata.dev/hierarchy.html), [querying / filtering / pagination](https://docs.atomicdata.dev/hierarchy.html), [event sourcing and versioning](https://docs.atomicdata.dev/commits/intro.html), [file management](https://docs.atomicdata.dev/files.html), [websockets](https://docs.atomicdata.dev/websockets.html), [API endpoints](https://docs.atomicdata.dev/endpoints.html) and more.

[Read more on docs.atomicdata.dev](https://docs.atomicdata.dev).

## Tools & libraries

- [**AtomicServer**](https://github.com/atomicdata-dev/atomic-server): powerful database + all-in-one workspace (powers [atomicdata.dev](https://atomicdata.dev), run with `docker run -p 80:80 -p 443:443 -v atomic-storage:/atomic-storage joepmeneer/atomic-server`)
- **Browser GUI app** [atomic-data-browser](https://github.com/atomicdata-dev/atomic-data-browser) (bundled with atomic-server) features group chat, tables, documents and more. ([demo on atomicdata.dev](https://atomicdata.dev))
- **Typescript** library: [@tomic/lib](https://www.npmjs.com/package/@tomic/lib)
- **React** library: [@tomic/react](https://www.npmjs.com/package/@tomic/react). Start with the [react template on codesandbox](https://codesandbox.io/s/atomic-data-react-template-4y9qu?file=/src/MyResource.tsx)
- **Svelte** library: [@tomic/svelte](https://github.com/atomicdata-dev/atomic-svelte)
- **Command line tool**: [atomic-cli](https://github.com/joepio/atomic) (`cargo install atomic-cli`)
- **Rust** library: [atomic-lib](https://github.com/joepio/atomic)
- **RayCast** plugin: [atomic-raycast](https://github.com/atomicdata-dev/atomic-raycast) (quickly search in your atomic-server)

## Example projects

- [Atomic-Server as Headless CMS + SvelteKit](https://github.com/ontola/wonenatthepark/)
- [Atomic Data Model Builder](https://github.com/atomicdata-dev/atomic-data-model-builder) built with @tomic/svelte

## Get involved

Make sure to [join our Discord](https://discord.gg/a72Rv2P) if you'd like to discuss Atomic Data with others.

## Status

Keep in mind that none of the Atomic Data project has reached a v1, which means that breaking changes can happen.
Check out the [status + roadmap in the docs](https://docs.atomicdata.dev/roadmap.html#where-were-at).
Maintained and developed by [Ontola.io](https://ontola.io/)
