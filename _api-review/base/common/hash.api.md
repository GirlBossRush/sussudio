## API Report File for "@sussudio/base/common/hash"

> Do not edit this file. It is a report generated by [API Extractor](https://api-extractor.com/).

```ts

// @public (undocumented)
export function doHash(obj: any, hashVal: number): number;

// @public
export function hash(obj: any): number;

// @public (undocumented)
export class Hasher {
    	// (undocumented)
    hash(obj: any): number;
    	// (undocumented)
    get value(): number;
    	}

// @public (undocumented)
export function numberHash(val: number, initialHashVal: number): number;

// @public (undocumented)
export function stringHash(s: string, hashVal: number): number;

// @public
export class StringSHA1 {
    	constructor();
    	// (undocumented)
    digest(): string;
    	// (undocumented)
    update(str: string): void;
    	}

// @public (undocumented)
export function toHexString(buffer: ArrayBuffer): string;

// @public (undocumented)
export function toHexString(value: number, bitsize?: number): string;

// (No @packageDocumentation comment for this package)

```
