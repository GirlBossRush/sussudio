## API Report File for "@sussudio/base/common/lazy"

> Do not edit this file. It is a report generated by [API Extractor](https://api-extractor.com/).

```ts

// @public
export interface Lazy<T> {
    	// (undocumented)
    getValue(): T;
    	// (undocumented)
    hasValue(): boolean;
    	// (undocumented)
    map<R>(f: (x: T) => R): Lazy<R>;
}

// @public (undocumented)
export class Lazy<T> {
    	constructor(executor: () => T);
    	get rawValue(): T | undefined;
    	}

// (No @packageDocumentation comment for this package)

```
