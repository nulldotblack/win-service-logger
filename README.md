# win-service-logger

A logger which writes log messages to the Windows Event Viewer

## Example

```rust
extern crate win_service_logger;
#[macro_use] extern crate log;

fn main() {
    win_service_logger::init();
    trace!("Hello from Rust!");

    warn!("This will be a warning in Event Viewer!");
    error!("Bad");
}
