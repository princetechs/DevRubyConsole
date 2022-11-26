# irb.wasm

IRB on browser powered by WebAssembly.
You can try irb.wasm on your browser. It works on CRuby ported to WebAssembly.

Demo: https://irb-wasm.vercel.app/

<div align="center">
<img src=./docs/demo.png width="400px">
</div>

## Development

```console
$ rake static/irb.wasm   # You can omit the argument as default task makes static/irb.wasm
$ npm install
$ rake parcel
```

### Clean build

If you need to re-build Ruby itself (when you made a change to Ruby), clean `rubies` and `build` directories by `rake deep_clean`, then re-execute `rake static/irb.wasm`

If you just made a change to `fake-gems`, you only need to remove `static/irb.wasm` by `rake clean` and re-execute `rake static/irb.wasm` to avoid rebuilding everything.
