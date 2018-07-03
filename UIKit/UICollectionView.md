# UIKit | UICollectionView

## UICollectionView extends UIScrollView

An object that manages an ordered collection of data items and presents them using customizable layouts.

```typescript
/** 
 * Initializes and returns a newly allocated collection view object with the specified layout.
 */
constructor(collectionViewLayout: UICollectionViewLayout)

/** 
 * The layout used to organize the collected view’s items.
 */
readonly collectionViewLayout: UICollectionViewLayout

/** 
 * A Boolean value that indicates whether users can select items in the collection view.
 */
allowsSelection: boolean

/** 
 * A Boolean value that determines whether users can select more than one item in the collection view.
 */
allowsMultipleSelection: boolean

/** 
 * Registers an object initializer returning a cell with the collection view under a specified identifier.
 */
register(initializer: (context: any) => UICollectionViewCell, reuseIdentifier: string)

/** 
 * Returns a reusable collection-view cell object for the specified reuse identifier and adds it to the table.
 */
dequeueReusableCell(reuseIdentifier: string, indexPath: UIIndexPath): UICollectionViewCell

/** 
 * Reloads the rows and sections of the table view.
 */
reloadData(): void

/** 
 * Selects the item at the specified index path and optionally scrolls it into view.
 */
selectItem(indexPath: UIIndexPath, animated: boolean): void

/** 
 * Deselects the item at the specified index.
 */
deselectItem(indexPath: UIIndexPath, animated: boolean): void

/** 
 * Tells your data source object for the number of sections in the collection view.
 */
on('numberOfSections', () => number): void

/** 
 * Tells your data source object for the number of items in the specified section.
 */
on('numberOfItems', (inSection: number) => number): void

/** 
 * Tells your data source object for the cell that corresponds to the specified item in the collection view.
 */
on('cellForItem', (indexPath: UIIndexPath) => UICollectionViewCell): void

/** 
 * Tells the delegate that the item at the specified index path was selected.
 */
on('didSelectItem', (indexPath: UIIndexPath, cell: UICollectionViewCell) => void): void

/** 
 * Tells the delegate that the item at the specified path was deselected.
 */
on('didDeselectItem', (indexPath: UIIndexPath, cell: UICollectionViewCell) => void): void
```

## UICollectionViewCell extends UIView

A single data item when that item is within the collection view’s visible bounds.

```typescript

/** 
 * An UICollectionViewCell must be created with context which should be call by UICollectionView.register method's callback.
 */
constructor(context: any)

/** 
 * The main view to which you add your cell’s custom content.
 */
readonly contentView: UIView

/** 
 * A string used to identify a cell that is reusable.
 */
readonly reuseIdentifier: string | undefined

/** 
 * Calls after cell select state change.
 */
on('selected', (sender: UITableViewCell, selected: boolean) => void): void

/** 
 * Calls after cell highlight state change.
 */
on('highlighted', (sender: UITableViewCell, highlighted: boolean) => void): void
```

## UICollectionViewLayout

An abstract base class for generating layout information for a collection view.

```typescript

/** 
 * The collection view object currently using this layout object.
 */
readonly collectionView: UICollectionView | undefined

/** 
 * Invalidates the current layout and triggers a layout update.
 */
invalidateLayout(): void
```

## UICollectionViewFlowLayout extends UICollectionViewLayout

A concrete layout object that organizes items into a grid with optional header and footer views for each section.

```typescript
/** 
 * The minimum spacing to use between lines of items in the grid.
 */
minimumLineSpacing: number

/** 
 * The minimum spacing to use between items in the same row.
 */
minimumInteritemSpacing: number

/** 
 * The default size to use for cells.
 */
itemSize: Size

/** 
 * The default sizes to use for section headers.
 */
headerReferenceSize: Size

/** 
 * The default sizes to use for section footers.
 */
footerReferenceSize: Size

/** 
 * The margins used to lay out content in a section
 */
sectionInset: EdgeInsets

/** 
 * The scroll direction of the grid.
 */
scrollDirection: UICollectionViewScrollDirection = .vertical

/** 
 * Tells the delegate for the size of the specified item’s cell.
 */
on('sizeForItem', (indexPath: UIIndexPath) => Size): void

/** 
 * Tells the delegate for the margins to apply to content in the specified section.
 */
on('insetForSection', (inSection: number) => EdgeInsets): void

/** 
 * Tells the delegate for the spacing between successive rows or columns of a section.
 */
on('minimumLineSpacing', (inSection: number) => number): void

/** 
 * Tells the delegate for the spacing between successive items in the rows or columns of a section.
 */
on('minimumInteritemSpacing', (inSection: number) => number): void

/** 
 * Tells the delegate for the size of the header view in the specified section.
 */
on('referenceSizeForHeader', (inSection: number) => Size): void

/** 
 * Tells the delegate for the size of the footer view in the specified section.
 */
on('referenceSizeForFooter', (inSection: number) => Size): void
```

## UICollectionViewScrollDirection

```typescript
enum UICollectionViewScrollDirection {
  vertical,
  horizontal,
}
```

## Relate

* [Apple Document](https://developer.apple.com/documentation/uikit/uicollectionview?language=objc)
* [UIIndexPath](UIIndexPath.md)