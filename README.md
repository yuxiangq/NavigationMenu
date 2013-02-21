Navigation Menu for iOS
=============
*Version 1.0*

Navigation Menu is an Objective-C component that adds possibility to show menu from navigation bar.

Examples
---------
	- (void)viewDidLoad
	{
    	[super viewDidLoad];
    	// check if we have a navigationItem
		if (self.navigationItem) {
        	CGRect frame = CGRectMake(0.0, 0.0, 200.0, self.navigationController.navigationBar.bounds.size.height);
        	SINavigationMenuView *menu = [[SINavigationMenuView alloc] initWithFrame:frame title:@"Menu"];
        	//Set in which view we will display a menu
        	[menu displayMenuInView:self.view];
        	//Create array of items
        	menu.items = @[@"News", @"Top Articles", @"Messages"];
        	menu.delegate = self;
        	self.navigationItem.titleView = menu;
    	}
    }
    
    //Delegate method
    - (void)didSelectItemAtIndex:(NSUInteger)index
	{
    	NSLog(@"did selected item at index %d", index);
	}
    
See the demo project for more examples.