# UITableView-with-UITextView-and-UILabel-Resize
Simple example of how to layout a UITableView automatically.

Works as of iOS 8.3

Bare minimum setup for having a UITableView containing UILabel and UITextView that automatically resize to fit content.

Key items

In TableViewController you must set some value for estimated row height and then set the rowHeight of the table view to automatically dimension:
```
    - (void)viewDidLoad {
        [super viewDidLoad];
        self.tableView.estimatedRowHeight = self.tableView.rowHeight;
        self.tableView.rowHeight = UITableViewAutomaticDimension;
    }
```
UITextView must have scrolling disabled!

UILabel must have lines set to zero and some sort of appropriate wrapping option.
