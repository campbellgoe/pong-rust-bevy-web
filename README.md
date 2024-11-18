# steps to run the rust+bevy+wasm web projects

`cargo install -f wasm-bindgen-cli` - to install wasm bindgen cli

`rustup target add wasm32-unknown-unknown` - in the project directory to add web support

`cargo build --release --target wasm32-unknown-unknown` - to build for the web

`wasm-bindgen --out-dir ./out/ --target web ./target/wasm32-unknown-unknown/release/pong.wasm` - to generate wasm bindings for the web (make sure pong.wasm is set to your project name specified in Cargo.toml)

Now you can copy `./out` to `./web/out` and then run the project locally with `npx serve web`

Open localhost on the specified port and see the Rust+Bevy wasm web project locally