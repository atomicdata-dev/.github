![Atomic Data](https://raw.githubusercontent.com/ontola/atomic-data-docs/master/src/assets/atomic_data_logo_stroke.svg)

**Atomic Data is a modular specification for sharing, modifying and modeling graph data. It combines the ease of use of JSON, the connectivity of RDF (linked data) and the reliability of type-safety.**

Atomic Data uses links to connect pieces of data, and therefore makes it easier to connect datasets to each other - even when these datasets exist on separate machines.

Atomic Data has been designed with [the following goals in mind](motivation.md):

- Give people more control over their data
- Make linked data easier to use
- Make it easier for developers to build highly interoperable apps
- Make standardization easier and cheaper

Atomic Data is [Linked Data](https://ontola.io/what-is-linked-data/), as it is a [strict subset of RDF](interoperability/rdf.md).
It is type-safe (you know if something is a `string`, `number`, `date`, `URL`, etc.) and extensible through [Atomic Schema](schema/intro.md), which means that you can re-use or define your own Classes, Properties and Datatypes.

The default serialization format for Atomic Data is [JSON-AD](core/json-ad.md), which is simply JSON where each key is a URL of an Atomic Property.
These Properties are responsible for setting the `datatype` (to ensure type-safety) and setting `shortnames` (which help to keep names short, for example in JSON serialization) and `descriptions` (which provide semantic explanations of what a property should be used for).

Atomic Data has specifications for [authentication](https://docs.atomicdata.dev/authentication.html), [authorization](https://docs.atomicdata.dev/hierarchy.html), [querying / filtering / pagination](https://docs.atomicdata.dev/hierarchy.html), [event sourcing and versioning](https://docs.atomicdata.dev/commits/intro.html), [file management](https://docs.atomicdata.dev/files.html), [websockets](https://docs.atomicdata.dev/websockets.html), [API endpoints](https://docs.atomicdata.dev/endpoints.html) and more.

[Read more on docs.atomicdata.dev](https://docs.atomicdata.dev).

## Tools & libraries

- Host your own [atomic-server](https://github.com/joepio/atomic) (powers [atomicdata.dev](https://atomicdata.dev), run with `docker run -p 80:80 -p 443:443 -v atomic-storage:/atomic-storage joepmeneer/atomic-server`)
- Browser app [atomic-data-browser](https://github.com/joepio/atomic-data-browser) ([demo on atomicdata.dev](https://atomicdata.dev))
- Build a react app using [typescript & react libraries](https://github.com/joepio/atomic-data-ts). Start with the [react template on codesandbox](https://codesandbox.io/s/atomic-data-react-template-4y9qu?file=/src/MyResource.tsx)
- Discover the command line tool: [atomic-cli](https://github.com/joepio/atomic) (`cargo install atomic-cli`)
- Use the Rust library: [atomic-lib](https://github.com/joepio/atomic)
- Check out the [RayCast] [plugin](https://github.com/atomicdata-dev/atomic-raycast)

## Get involved

Make sure to [join our Discord](https://discord.gg/a72Rv2P) if you'd like to discuss Atomic Data with others.

## Status

Keep in mind that none of the Atomic Data project has reached a v1, which means that breaking changes can happen.
