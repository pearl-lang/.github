# [Pearl language](https://pearl-lang.github.io)

```
// Good luck 🫡.
require color::{red, green, blue, reset}

declare global_var = "Hello" // this is global variable.
ebpf declare ebpf_global_var = "Hello" // this can be reachable from all ebpf scopes.

#[ebpf(load, xdp)]
ebpf hello_xdp(ctx) {
	// not is alias of "!="
	if &ctx not 0 {
		printk("{0^}, Xdp.", ebpf_global_var)
	}
}

function main() -> int {
	declare var = "world"
	echo("Hello, {0}{1^}{2}!", red, global_var, reset)
	0
}
```

Let's get build something amazing together 👉 [Pearl Social](https://pearl-lang.github.io/social).
