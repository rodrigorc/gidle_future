# gidle_future

A future executor for the glib main loop idle time.

[![Latest version](https://img.shields.io/crates/v/gidle_future.svg)](https://crates.io/crates/gidle_future)
[![Documentation](https://docs.rs/gidle_future/badge.svg)](https://docs.rs/gidle_future)

It is compatible with most of the async frameworks out there, but you won't need complex synchronization primitives,
because all you the code you write is run in the main thread.

For details, see the [documentation](https://docs.rs/gidle_future).

## Getting Started

It is recommended to go to [crates.io](https://crates.io/crates/pomelo) for
the newest released version, as well as links to the newest builds of the docs.

Add the following dependency to your Cargo manifest, together with the `glib` and `future` crates you need.

```toml
[dependencies]
gidle_future = "*"
```

Then any time you want to spawn an idle future:

```rust
gidle_future::spawn(async move { /* async code */ });
```

Or use any other style of async code.
