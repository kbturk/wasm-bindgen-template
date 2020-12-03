# Hello, World!

This is a simple template without wasm-pack that was forked from wasm-bidgen examples 
which bridging rust and javascript together.

[View the original documentation for this example from wasm-bidgen][dox] or [View 
the original compiled example here.][compiled]

[compiled]: https://rustwasm.github.io/wasm-bindgen/exbuild/hello_world/
[dox]: https://rustwasm.github.io/docs/wasm-bindgen/examples/hello-world.html

<h2>Instructions:</h2>
<ul>
<li>Initially, add wasm32-unknown-unknown to toolchain. This should only have to be done once:
    ```
    $rustup target add wasm32-unknown-unknown' 
    ```</li>

<li>Cargo build with wasm32-unknown-unknown: 
    ```
    $cargo build --target wasm32-unknown-unknown' 
    ```
</li>
<li>Check that you have this file: <path>\<program>\target\wasm32-unknown-unknown\debug\<program>.wasm </li>
<li>Run the following two commands to make the .wasm file able to be consumed by JS:
    ```
    $cargo install wasm-bindgen-cli
    $wasm-bindgen target\wasm32-unknown-unknown\debug\<program>.wasm --out-dir .
    ```
    This step is where the wasm-bindgen CLI tool postprocesses the input wasm file, 
    making it suitable to use.
</li>

<li> Finally, you can build the example locally with:

    ```
    $ npm run serve
    ```
    Or your other favorite bundler.
    </li>
</ul>
Now, you can visit http://localhost:8080 in a browser should run the example!
