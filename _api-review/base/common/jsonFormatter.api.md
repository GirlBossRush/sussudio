## API Report File for "@sussudio/base/common/jsonFormatter"

> Do not edit this file. It is a report generated by [API Extractor](https://api-extractor.com/).

```ts

// @public
export interface Edit {
    	content: string;
    	length: number;
    	offset: number;
}

// @public (undocumented)
export function format(documentText: string, range: Range_2 | undefined, options: FormattingOptions): Edit[];

// @public (undocumented)
export interface FormattingOptions {
    	eol?: string;
    	insertSpaces?: boolean;
    	tabSize?: number;
}

// @public (undocumented)
export function getEOL(options: FormattingOptions, text: string): string;

// @public (undocumented)
export function isEOL(text: string, offset: number): boolean;

// @public
interface Range_2 {
    	length: number;
    	offset: number;
}
export { Range_2 as Range }

// @public
export function toFormattedString(obj: any, options: FormattingOptions): string;

// (No @packageDocumentation comment for this package)

```
