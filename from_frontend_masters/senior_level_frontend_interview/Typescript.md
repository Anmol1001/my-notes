**What is never in typescript?**
	 never in typescript is empty union. It cannot have anything.
**How do you convert empty union to some union?**
	You can convert type T to array [T].
**How do you loop through array in typescript?**
	You can use extends keywords with [infer First,...Tail]. And you can use recursion loop.
**Why doesn't the type check `T extends never` work directly for detecting the never type in TypeScript?**
	The never type in TypeScript is an empty union, which means `T extends never` doesn't produce any value - it just returns never itself rather than reaching the true or false statement. This makes it impossible to directly detect the never type using a simple extends check.
**How can you check if an object type is empty (has no keys) in TypeScript?**
	Use the condition `keyof T extends never`. If an object has no keys, `keyof T` produces an empty union, which extends never, causing the check to return true for empty objects.
**In the following code, what does the `infer` keyword accomplish?**
`T extends [infer First, ...infer Tail]`
	The `infer` keyword allows you to extract and reference types from a structure. In this case, it extracts the type of the first element as `First` and the remaining elements as `Tail`, enabling you to recursively process array/tuple types element by element.