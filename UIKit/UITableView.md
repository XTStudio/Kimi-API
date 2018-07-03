# UIKit | UITableView extends UIScrollView

A view that presents data using rows arranged in a single column.

```typescript
/**
 * Returns an accessory view that is displayed above the table.
 */
tableHeaderView: UIView | undefined

/**
 * Returns an accessory view that is displayed below the table.
 */
tableFooterView: UIView | undefined

/**
 * The color of separator rows in the table view.
 */
separatorColor: UIColor | undefined

/**
 * Specifies the default inset of cell separators.
 */
separatorInset: EdgeInsets

/**
 * A Boolean value that determines whether users can select a row.
 */
allowsSelection: boolean

/**
 * A Boolean value that determines whether users can select more than one row outside of editing mode.
 */
allowsMultipleSelection: boolean

/**
 * Registers an object initializer returning a cell with the table view under a specified identifier.
 */
register(initializer: (context: any) => UITableViewCell, reuseIdentifier: string)

/**
 * Returns a reusable table-view cell object for the specified reuse identifier and adds it to the table.
 */
dequeueReusableCell(reuseIdentifier: string, indexPath: UIIndexPath): UITableViewCell

/**
 * Reloads the rows and sections of the table view.
 */
reloadData(): void

/**
 * Selects a row in the table view identified by index path, optionally scrolling the row to a location in the table view.
 */
selectRow(indexPath: UIIndexPath, animated: boolean): void

/**
 * Deselects a given row identified by index path, with an option to animate the deselection.
 */
deselectRow(indexPath: UIIndexPath, animated: boolean): void

/**
 * Tells the data source to return the number of sections in the table view.
 */
on('numberOfSections', () => number): void

/**
 * Tells the data source to return the number of rows in a given section of a table view.
 */
on('numberOfRows', (inSection: number) => number): void

/**
 * Tells the delegate for the height to use for a row in a specified location.
 */
on('heightForRow', (indexPath: UIIndexPath) => number): void

/**
 * Tells the data source for a cell to insert in a particular location of the table view.
 */
on('cellForRow', (indexPath: UIIndexPath) => UITableViewCell): void

/**
 * Tells the delegate for a view object to display in the header of the specified section of the table view.
 */
on('viewForHeader', (inSection: number) => UIView | undefined): void

/**
 * Tells the delegate for the height to use for the header of a particular section.
 */
on('heightForHeader', (inSection: number) => number): void

/**
 * Tells the delegate for a view object to display in the footer of the specified section of the table view.
 */
on('viewForFooter', (inSection: number) => UIView | undefined): void

/**
 * Tells the delegate for the height to use for the footer of a particular section.
 */
on('heightForFooter', (inSection: number) => number): void

/**
 * Tells the delegate that the specified row is now selected.
 */
on('didSelectRow', (indexPath: UIIndexPath, cell: UITableViewCell) => void): void

/**
 * Tells the delegate that the specified row is now deselected.
 */
on('didDeselectRow', (indexPath: UIIndexPath, cell: UITableViewCell) => void): void
```

# UIKit | UITableViewCell extends UIView

A cell in a table view.

```typescript

/**
 * An UITableViewCell must be created with context which should be call by UITableView.register method's callback.
 */
constructor(context: any)

/**
 * Returns the content view of the cell object.
 */
readonly contentView: UIView

/**
 * A string used to identify a cell that is reusable.
 */
readonly reuseIdentifier: string | undefined

/**
 * A boolean value indicator that cell should show highlight background style.
 */
hasSelectionStyle: boolean = true

/**
 * Calls after cell select state change.
 */
on('selected', (sender: UITableViewCell, selected: boolean, animated: boolean) => void): void

/**
 * Calls after cell highlight state change.
 */
on('highlighted', (sender: UITableViewCell, highlighted: boolean, animated: boolean) => void): void
```

## Relate

* [Apple Document](https://developer.apple.com/documentation/uikit/uitableview?language=objc)
* [UIColor](UIColor.md)
* [EdgeInsets](Interfaces.md)
* [UIIndexPath](UIIndexPath.md)