## API Report File for "@sussudio/base/browser/ui/iconLabel/iconLabel"

> Do not edit this file. It is a report generated by [API Extractor](https://api-extractor.com/).

```ts

// @public (undocumented)
interface CancellationToken {
    	readonly isCancellationRequested: boolean;
    	readonly onCancellationRequested: (
    		listener: (e: any) => any,
    		thisArgs?: any,
    		disposables?: IDisposable[],
    	) => IDisposable;
}

// @public (undocumented)
namespace CancellationToken {
    	// (undocumented)
    function isCancellationToken(thing: unknown): thing is CancellationToken;
    	const // (undocumented)
    None: Readonly<CancellationToken>;
    	const // (undocumented)
    Cancelled: Readonly<CancellationToken>;
}

// @public
abstract class Disposable implements IDisposable {
    	constructor();
    	// (undocumented)
    dispose(): void;
    	static readonly None: Readonly<IDisposable>;
    	protected _register<T extends IDisposable>(o: T): T;
    	// (undocumented)
    protected readonly _store: DisposableStore;
}

// @public
class DisposableStore implements IDisposable {
    	constructor();
    	add<T extends IDisposable>(o: T): T;
    	clear(): void;
    	// (undocumented)
    static DISABLE_DISPOSED_WARNING: boolean;
    	dispose(): void;
    	// (undocumented)
    get isDisposed(): boolean;
    	}

// @public (undocumented)
const enum HoverPosition {
    	// (undocumented)
    ABOVE = 3,
    	// (undocumented)
    BELOW = 2,
    	// (undocumented)
    LEFT = 0,
    	// (undocumented)
    RIGHT = 1,
}

// @public (undocumented)
export class IconLabel extends Disposable {
    	constructor(container: HTMLElement, options?: IIconLabelCreationOptions);
    	// (undocumented)
    dispose(): void;
    	// (undocumented)
    get element(): HTMLElement;
    	// (undocumented)
    setLabel(label: string | string[], description?: string, options?: IIconLabelValueOptions): void;
    	}

// @public
interface IDisposable {
    	// (undocumented)
    dispose(): void;
}

// @public @deprecated
interface IHoverAction {
    	// (undocumented)
    commandId: string;
    	// (undocumented)
    iconClass?: string;
    	// (undocumented)
    label: string;
    	// (undocumented)
    run(target: HTMLElement): void;
}

// @public (undocumented)
interface IHoverDelegate {
    	// (undocumented)
    delay: number;
    	// (undocumented)
    onDidHideHover?: () => void;
    	// (undocumented)
    placement?: 'mouse' | 'element';
    	// (undocumented)
    showHover(options: IHoverDelegateOptions, focus?: boolean): IHoverWidget | undefined;
}

// @public (undocumented)
interface IHoverDelegateOptions extends IUpdatableHoverOptions {
    	// (undocumented)
    content: IMarkdownString | string | HTMLElement;
    	// (undocumented)
    hoverPosition?: HoverPosition;
    	// (undocumented)
    showPointer?: boolean;
    	// (undocumented)
    skipFadeInAnimation?: boolean;
    	// (undocumented)
    target: IHoverDelegateTarget | HTMLElement;
}

// @public (undocumented)
interface IHoverDelegateTarget extends IDisposable {
    	// (undocumented)
    readonly targetElements: readonly HTMLElement[];
    	// (undocumented)
    x?: number;
}

// @public (undocumented)
interface IHoverWidget extends IDisposable {
    	// (undocumented)
    readonly isDisposed: boolean;
}

// @public (undocumented)
export interface IIconLabelCreationOptions {
    	// (undocumented)
    readonly hoverDelegate?: IHoverDelegate;
    	// (undocumented)
    readonly supportDescriptionHighlights?: boolean;
    	// (undocumented)
    readonly supportHighlights?: boolean;
    	// (undocumented)
    readonly supportIcons?: boolean;
}

// @public (undocumented)
export interface IIconLabelValueOptions {
    	// (undocumented)
    descriptionMatches?: readonly IMatch[];
    	// (undocumented)
    descriptionTitle?: string;
    	// (undocumented)
    disabledCommand?: boolean;
    	// (undocumented)
    readonly domId?: string;
    	// (undocumented)
    extraClasses?: readonly string[];
    	// (undocumented)
    hideIcon?: boolean;
    	// (undocumented)
    italic?: boolean;
    	// (undocumented)
    labelEscapeNewLines?: boolean;
    	// (undocumented)
    matches?: readonly IMatch[];
    	// (undocumented)
    readonly separator?: string;
    	// (undocumented)
    strikethrough?: boolean;
    	// (undocumented)
    title?: string | ITooltipMarkdownString;
}

// @public (undocumented)
interface IMarkdownString {
    	// (undocumented)
    readonly baseUri?: UriComponents;
    	// (undocumented)
    readonly isTrusted?: boolean | MarkdownStringTrustedOptions;
    	// (undocumented)
    readonly supportHtml?: boolean;
    	// (undocumented)
    readonly supportThemeIcons?: boolean;
    	// (undocumented)
    uris?: {
        		[href: string]: UriComponents;
        	};
    	// (undocumented)
    readonly value: string;
}

// @public (undocumented)
interface IMatch {
    	// (undocumented)
    end: number;
    	// (undocumented)
    start: number;
}

// @public (undocumented)
interface ITooltipMarkdownString {
    	// (undocumented)
    markdown:
    		| IMarkdownString
    		| string
    		| undefined
    		| ((token: CancellationToken) => Promise<IMarkdownString | string | undefined>);
    	// (undocumented)
    markdownNotSupportedFallback: string | undefined;
}

// @public (undocumented)
interface IUpdatableHoverOptions {
    	// (undocumented)
    actions?: IHoverAction[];
    	// (undocumented)
    linkHandler?(url: string): void;
}

// @public (undocumented)
interface MarkdownStringTrustedOptions {
    	// (undocumented)
    readonly enabledCommands: readonly string[];
}

// @public (undocumented)
interface UriComponents {
    	// (undocumented)
    authority: string;
    	// (undocumented)
    fragment: string;
    	// (undocumented)
    path: string;
    	// (undocumented)
    query: string;
    	// (undocumented)
    scheme: string;
}

// (No @packageDocumentation comment for this package)

```
