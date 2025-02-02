## API Report File for "@sussudio/base/browser/ui/tree/compressedObjectTreeModel"

> Do not edit this file. It is a report generated by [API Extractor](https://api-extractor.com/).

```ts

// @public (undocumented)
export function compress<T>(element: ICompressedTreeElement<T>): ITreeElement<ICompressedTreeNode<T>>;

// @public (undocumented)
export type CompressedNodeUnwrapper<T> = (node: ICompressedTreeNode<T>) => T;

// @public (undocumented)
export class CompressedObjectTreeModel<T extends NonNullable<any>, TFilterData extends NonNullable<any> = void>
	implements ITreeModel<ICompressedTreeNode<T> | null, TFilterData, T | null>
    {
    	constructor(
    		user: string,
    		list: IList<ITreeNode<ICompressedTreeNode<T>, TFilterData>>,
    		options?: ICompressedObjectTreeModelOptions<T, TFilterData>,
    	);
    	// (undocumented)
    expandTo(location: T | null): void;
    	// (undocumented)
    getCompressedNode(element: T | null): ICompressedTreeNode<T> | null;
    	// (undocumented)
    getFirstElementChild(location: T | null): ICompressedTreeNode<T> | null | undefined;
    	// (undocumented)
    getLastElementAncestor(location?: T | null | undefined): ICompressedTreeNode<T> | null | undefined;
    	// (undocumented)
    getListIndex(location: T | null): number;
    	// (undocumented)
    getListRenderCount(location: T | null): number;
    	// (undocumented)
    getNode(location?: T | null | undefined): ITreeNode<ICompressedTreeNode<T> | null, TFilterData>;
    	// (undocumented)
    getNodeLocation(node: ITreeNode<ICompressedTreeNode<T>, TFilterData>): T | null;
    	// (undocumented)
    getParentNodeLocation(location: T | null): T | null;
    	// (undocumented)
    has(element: T | null): boolean;
    	// (undocumented)
    isCollapsed(location: T | null): boolean;
    	// (undocumented)
    isCollapsible(location: T | null): boolean;
    	// (undocumented)
    isCompressionEnabled(): boolean;
    	// (undocumented)
    get onDidChangeCollapseState(): Event_2<ICollapseStateChangeEvent<ICompressedTreeNode<T>, TFilterData>>;
    	// (undocumented)
    get onDidChangeRenderNodeCount(): Event_2<ITreeNode<ICompressedTreeNode<T>, TFilterData>>;
    	// (undocumented)
    get onDidSplice(): Event_2<ITreeModelSpliceEvent<ICompressedTreeNode<T> | null, TFilterData>>;
    	// (undocumented)
    refilter(): void;
    	// (undocumented)
    rerender(location: T | null): void;
    	// (undocumented)
    resort(location?: T | null, recursive?: boolean): void;
    	// (undocumented)
    readonly rootRef: null;
    	// (undocumented)
    setChildren(
    		element: T | null,
    		children: Iterable<ICompressedTreeElement<T>> | undefined,
    		options: IObjectTreeModelSetChildrenOptions<T, TFilterData>,
    	): void;
    	// (undocumented)
    setCollapsed(location: T | null, collapsed?: boolean | undefined, recursive?: boolean | undefined): boolean;
    	// (undocumented)
    setCollapsible(location: T | null, collapsible?: boolean): boolean;
    	// (undocumented)
    setCompressionEnabled(enabled: boolean): void;
    	// (undocumented)
    get size(): number;
    	// (undocumented)
    updateElementHeight(element: T, height: number): void;
    	}

// @public (undocumented)
export class CompressibleObjectTreeModel<
	T extends NonNullable<any>,
	TFilterData extends NonNullable<any> = void,
> implements IObjectTreeModel<T, TFilterData>
    {
    	constructor(
    		user: string,
    		list: IList<ITreeNode<T, TFilterData>>,
    		options?: ICompressibleObjectTreeModelOptions<T, TFilterData>,
    	);
    	// (undocumented)
    expandTo(location: T | null): void;
    	// (undocumented)
    getCompressedTreeNode(location?: T | null): ITreeNode<ICompressedTreeNode<T> | null, TFilterData>;
    	// (undocumented)
    getFirstElementChild(location: T | null): T | null | undefined;
    	// (undocumented)
    getLastElementAncestor(location?: T | null | undefined): T | null | undefined;
    	// (undocumented)
    getListIndex(location: T | null): number;
    	// (undocumented)
    getListRenderCount(location: T | null): number;
    	// (undocumented)
    getNode(location?: T | null | undefined): ITreeNode<T | null, any>;
    	// (undocumented)
    getNodeLocation(node: ITreeNode<T | null, any>): T | null;
    	// (undocumented)
    getParentNodeLocation(location: T | null): T | null;
    	// (undocumented)
    has(location: T | null): boolean;
    	// (undocumented)
    isCollapsed(location: T | null): boolean;
    	// (undocumented)
    isCollapsible(location: T | null): boolean;
    	// (undocumented)
    isCompressionEnabled(): boolean;
    	// (undocumented)
    get onDidChangeCollapseState(): Event_2<ICollapseStateChangeEvent<T | null, TFilterData>>;
    	// (undocumented)
    get onDidChangeRenderNodeCount(): Event_2<ITreeNode<T | null, TFilterData>>;
    	// (undocumented)
    get onDidSplice(): Event_2<ITreeModelSpliceEvent<T | null, TFilterData>>;
    	// (undocumented)
    refilter(): void;
    	// (undocumented)
    rerender(location: T | null): void;
    	// (undocumented)
    resort(element?: T | null, recursive?: boolean): void;
    	// (undocumented)
    readonly rootRef: null;
    	// (undocumented)
    setChildren(
    		element: T | null,
    		children?: Iterable<ICompressedTreeElement<T>>,
    		options?: IObjectTreeModelSetChildrenOptions<T, TFilterData>,
    	): void;
    	// (undocumented)
    setCollapsed(location: T | null, collapsed?: boolean | undefined, recursive?: boolean | undefined): boolean;
    	// (undocumented)
    setCollapsible(location: T | null, collapsed?: boolean): boolean;
    	// (undocumented)
    setCompressionEnabled(enabled: boolean): void;
    	// (undocumented)
    updateElementHeight(element: T, height: number): void;
}

// @public (undocumented)
export function decompress<T>(element: ITreeElement<ICompressedTreeNode<T>>): ICompressedTreeElement<T>;

// @public (undocumented)
export const DefaultElementMapper: ElementMapper<any>;

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
export type ElementMapper<T> = (elements: T[]) => T;

// @public
interface Event_2<T> {
    	// (undocumented)
    (listener: (e: T) => any, thisArgs?: any, disposables?: IDisposable[] | DisposableStore): IDisposable;
}

// @public (undocumented)
namespace Event_2 {
    	const // (undocumented)
    None: Event_2<any>;
    	function accumulate<T>(event: Event_2<T>, delay?: number, disposable?: DisposableStore): Event_2<T[]>;
    	function any<T>(...events: Event_2<T>[]): Event_2<T>;
    	// (undocumented)
    function any(...events: Event_2<any>[]): Event_2<void>;
    	function buffer<T>(event: Event_2<T>, flushAfterTimeout?: boolean, _buffer?: T[]): Event_2<T>;
    	// (undocumented)
    function chain<T>(event: Event_2<T>): IChainableEvent<T>;
    	function debounce<T>(
    		event: Event_2<T>,
    		merge: (last: T | undefined, event: T) => T,
    		delay?: number,
    		leading?: boolean,
    		leakWarningThreshold?: number,
    		disposable?: DisposableStore,
    	): Event_2<T>;
    	function debounce<I, O>(
    		event: Event_2<I>,
    		merge: (last: O | undefined, event: I) => O,
    		delay?: number,
    		leading?: boolean,
    		leakWarningThreshold?: number,
    		disposable?: DisposableStore,
    	): Event_2<O>;
    	function defer(event: Event_2<unknown>, disposable?: DisposableStore): Event_2<void>;
    	// (undocumented)
    interface DOMEventEmitter {
        		// (undocumented)
        addEventListener(event: string | symbol, listener: Function): void;
        		// (undocumented)
        removeEventListener(event: string | symbol, listener: Function): void;
        	}
    	function filter<T, U>(event: Event_2<T | U>, filter: (e: T | U) => e is T, disposable?: DisposableStore): Event_2<T>;
    	// (undocumented)
    function filter<T>(event: Event_2<T>, filter: (e: T) => boolean, disposable?: DisposableStore): Event_2<T>;
    	// (undocumented)
    function filter<T, R>(event: Event_2<T | R>, filter: (e: T | R) => e is R, disposable?: DisposableStore): Event_2<R>;
    	function forEach<I>(event: Event_2<I>, each: (i: I) => void, disposable?: DisposableStore): Event_2<I>;
    	// (undocumented)
    function fromDOMEventEmitter<T>(emitter: DOMEventEmitter, eventName: string, map?: (...args: any[]) => T): Event_2<T>;
    	// (undocumented)
    function fromNodeEventEmitter<T>(emitter: NodeEventEmitter, eventName: string, map?: (...args: any[]) => T): Event_2<T>;
    	// (undocumented)
    function fromObservable<T>(obs: IObservable<T, any>, store?: DisposableStore): Event_2<T>;
    	// (undocumented)
    interface IChainableEvent<T> extends IDisposable {
        		// (undocumented)
        debounce(
        			merge: (last: T | undefined, event: T) => T,
        			delay?: number,
        			leading?: boolean,
        			leakWarningThreshold?: number,
        		): IChainableEvent<T>;
        		// (undocumented)
        debounce<R>(
        			merge: (last: R | undefined, event: T) => R,
        			delay?: number,
        			leading?: boolean,
        			leakWarningThreshold?: number,
        		): IChainableEvent<R>;
        		// (undocumented)
        event: Event_2<T>;
        		// (undocumented)
        filter(fn: (e: T) => boolean): IChainableEvent<T>;
        		// (undocumented)
        filter<R>(fn: (e: T | R) => e is R): IChainableEvent<R>;
        		// (undocumented)
        forEach(fn: (i: T) => void): IChainableEvent<T>;
        		// (undocumented)
        latch(): IChainableEvent<T>;
        		// (undocumented)
        map<O>(fn: (i: T) => O): IChainableEvent<O>;
        		// (undocumented)
        on(listener: (e: T) => any, thisArgs?: any, disposables?: IDisposable[] | DisposableStore): IDisposable;
        		// (undocumented)
        once(listener: (e: T) => any, thisArgs?: any, disposables?: IDisposable[]): IDisposable;
        		// (undocumented)
        reduce<R>(merge: (last: R | undefined, event: T) => R, initial?: R): IChainableEvent<R>;
        	}
    	function latch<T>(event: Event_2<T>, equals?: (a: T, b: T) => boolean, disposable?: DisposableStore): Event_2<T>;
    	function map<I, O>(event: Event_2<I>, map: (i: I) => O, disposable?: DisposableStore): Event_2<O>;
    	// (undocumented)
    interface NodeEventEmitter {
        		// (undocumented)
        on(event: string | symbol, listener: Function): unknown;
        		// (undocumented)
        removeListener(event: string | symbol, listener: Function): unknown;
        	}
    	function once<T>(event: Event_2<T>): Event_2<T>;
    	function reduce<I, O>(
    		event: Event_2<I>,
    		merge: (last: O | undefined, event: I) => O,
    		initial?: O,
    		disposable?: DisposableStore,
    	): Event_2<O>;
    	// (undocumented)
    function runAndSubscribe<T>(event: Event_2<T>, handler: (e: T | undefined) => any): IDisposable;
    	// (undocumented)
    function runAndSubscribeWithStore<T>(
    		event: Event_2<T>,
    		handler: (e: T | undefined, disposableStore: DisposableStore) => any,
    	): IDisposable;
    	function signal<T>(event: Event_2<T>): Event_2<void>;
    	function split<T, U>(
    		event: Event_2<T | U>,
    		isT: (e: T | U) => e is T,
    		disposable?: DisposableStore,
    	): [Event_2<T>, Event_2<U>];
    	// (undocumented)
    function toPromise<T>(event: Event_2<T>): Promise<T>;
}

// @public (undocumented)
interface ICollapseStateChangeEvent<T, TFilterData> {
    	// (undocumented)
    deep: boolean;
    	// (undocumented)
    node: ITreeNode<T, TFilterData>;
}

// @public (undocumented)
interface ICompressedObjectTreeModelOptions<T, TFilterData>
	extends IObjectTreeModelOptions<ICompressedTreeNode<T>, TFilterData> {
    	// (undocumented)
    readonly compressionEnabled?: boolean;
}

// @public (undocumented)
export interface ICompressedTreeElement<T> extends ITreeElement<T> {
    	// (undocumented)
    readonly children?: Iterable<ICompressedTreeElement<T>>;
    	// (undocumented)
    readonly incompressible?: boolean;
}

// @public (undocumented)
export interface ICompressedTreeNode<T> {
    	// (undocumented)
    readonly elements: T[];
    	// (undocumented)
    readonly incompressible: boolean;
}

// @public (undocumented)
export interface ICompressibleObjectTreeModelOptions<T, TFilterData> extends IObjectTreeModelOptions<T, TFilterData> {
    	// (undocumented)
    readonly compressionEnabled?: boolean;
    	// (undocumented)
    readonly elementMapper?: ElementMapper<T>;
}

// @public
interface IDisposable {
    	// (undocumented)
    dispose(): void;
}

// @public (undocumented)
interface IIdentityProvider<T> {
    	// (undocumented)
    getId(element: T): {
        		toString(): string;
        	};
}

// @public (undocumented)
interface IIndexTreeModelOptions<T, TFilterData> {
    	// (undocumented)
    readonly autoExpandSingleChildren?: boolean;
    	// (undocumented)
    readonly collapseByDefault?: boolean;
    	// (undocumented)
    readonly filter?: ITreeFilter<T, TFilterData>;
}

// @public (undocumented)
interface IIndexTreeModelSpliceOptions<T, TFilterData> {
    	readonly diffDepth?: number;
    	readonly diffIdentityProvider?: IIdentityProvider<T>;
    	onDidCreateNode?: (node: ITreeNode<T, TFilterData>) => void;
    	onDidDeleteNode?: (node: ITreeNode<T, TFilterData>) => void;
}

// @public (undocumented)
interface IList<T> extends ISpliceable<T> {
    	// (undocumented)
    updateElementHeight(index: number, height: number | undefined): void;
}

// @public (undocumented)
interface IObjectTreeModel<T extends NonNullable<any>, TFilterData extends NonNullable<any> = void>
	extends ITreeModel<T | null, TFilterData, T | null> {
    	// (undocumented)
    resort(element?: T | null, recursive?: boolean): void;
    	// (undocumented)
    setChildren(
    		element: T | null,
    		children: Iterable<ITreeElement<T>> | undefined,
    		options?: IObjectTreeModelSetChildrenOptions<T, TFilterData>,
    	): void;
    	// (undocumented)
    updateElementHeight(element: T, height: number | undefined): void;
}

// @public (undocumented)
interface IObjectTreeModelOptions<T, TFilterData> extends IIndexTreeModelOptions<T, TFilterData> {
    	// (undocumented)
    readonly identityProvider?: IIdentityProvider<T>;
    	// (undocumented)
    readonly sorter?: ITreeSorter<T>;
}

// @public (undocumented)
interface IObjectTreeModelSetChildrenOptions<T, TFilterData>
	extends IIndexTreeModelSpliceOptions<T, TFilterData> {}

// @public (undocumented)
interface IObservable<T, _TChange = void> {
    	addObserver(observer: IObserver): void;
    	// (undocumented)
    readonly debugName: string;
    	get(): T;
    	// (undocumented)
    map<TNew>(fn: (value: T) => TNew): IObservable<TNew>;
    	read(reader: IReader): T;
    	// (undocumented)
    removeObserver(observer: IObserver): void;
    	// (undocumented)
    readonly TChange: _TChange;
}

// @public (undocumented)
interface IObserver {
    	beginUpdate<T>(observable: IObservable<T>): void;
    	endUpdate<T>(observable: IObservable<T>): void;
    	handleChange<T, TChange>(observable: IObservable<T, TChange>, change: TChange): void;
}

// @public (undocumented)
interface IReader {
    	subscribeTo<T>(observable: IObservable<T, any>): void;
}

// @public (undocumented)
interface ISpliceable<T> {
    	// (undocumented)
    splice(start: number, deleteCount: number, toInsert: readonly T[]): void;
}

// @public (undocumented)
interface ITreeElement<T> {
    	// (undocumented)
    readonly children?: Iterable<ITreeElement<T>>;
    	// (undocumented)
    readonly collapsed?: boolean;
    	// (undocumented)
    readonly collapsible?: boolean;
    	// (undocumented)
    readonly element: T;
}

// @public
interface ITreeFilter<T, TFilterData = void> {
    	filter(element: T, parentVisibility: TreeVisibility): TreeFilterResult<TFilterData>;
}

// @public
interface ITreeFilterDataResult<TFilterData> {
    	data: TFilterData;
    	visibility: boolean | TreeVisibility;
}

// @public (undocumented)
interface ITreeModel<T, TFilterData, TRef> {
    	// (undocumented)
    expandTo(location: TRef): void;
    	// (undocumented)
    getFirstElementChild(location: TRef): T | undefined;
    	// (undocumented)
    getLastElementAncestor(location?: TRef): T | undefined;
    	// (undocumented)
    getListIndex(location: TRef): number;
    	// (undocumented)
    getListRenderCount(location: TRef): number;
    	// (undocumented)
    getNode(location?: TRef): ITreeNode<T, any>;
    	// (undocumented)
    getNodeLocation(node: ITreeNode<T, any>): TRef;
    	// (undocumented)
    getParentNodeLocation(location: TRef): TRef | undefined;
    	// (undocumented)
    has(location: TRef): boolean;
    	// (undocumented)
    isCollapsed(location: TRef): boolean;
    	// (undocumented)
    isCollapsible(location: TRef): boolean;
    	// (undocumented)
    readonly onDidChangeCollapseState: Event_2<ICollapseStateChangeEvent<T, TFilterData>>;
    	// (undocumented)
    readonly onDidChangeRenderNodeCount: Event_2<ITreeNode<T, TFilterData>>;
    	// (undocumented)
    readonly onDidSplice: Event_2<ITreeModelSpliceEvent<T, TFilterData>>;
    	// (undocumented)
    refilter(): void;
    	// (undocumented)
    rerender(location: TRef): void;
    	// (undocumented)
    readonly rootRef: TRef;
    	// (undocumented)
    setCollapsed(location: TRef, collapsed?: boolean, recursive?: boolean): boolean;
    	// (undocumented)
    setCollapsible(location: TRef, collapsible?: boolean): boolean;
}

// @public (undocumented)
interface ITreeModelSpliceEvent<T, TFilterData> {
    	// (undocumented)
    deletedNodes: ITreeNode<T, TFilterData>[];
    	// (undocumented)
    insertedNodes: ITreeNode<T, TFilterData>[];
}

// @public (undocumented)
interface ITreeNode<T, TFilterData = void> {
    	// (undocumented)
    readonly children: ITreeNode<T, TFilterData>[];
    	// (undocumented)
    readonly collapsed: boolean;
    	// (undocumented)
    readonly collapsible: boolean;
    	// (undocumented)
    readonly depth: number;
    	// (undocumented)
    readonly element: T;
    	// (undocumented)
    readonly filterData: TFilterData | undefined;
    	// (undocumented)
    readonly visible: boolean;
    	// (undocumented)
    readonly visibleChildIndex: number;
    	// (undocumented)
    readonly visibleChildrenCount: number;
}

// @public (undocumented)
interface ITreeSorter<T> {
    	// (undocumented)
    compare(element: T, otherElement: T): number;
}

// @public
type TreeFilterResult<TFilterData> = boolean | TreeVisibility | ITreeFilterDataResult<TFilterData>;

// @public (undocumented)
const enum TreeVisibility {
    	Hidden = 0,
    	Recurse = 2,
    	Visible = 1,
}

// (No @packageDocumentation comment for this package)

```
