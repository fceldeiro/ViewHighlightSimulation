# ViewHighlightSimulation

```
#pragma mark - selection effects
// HIghlight simulations
- (void)simulateHighlightForView:(UIView *)view {
	[UIView animateWithDuration:0.25 delay:0 options:UIViewAnimationOptionCurveEaseInOut animations: ^{
	    view.layer.backgroundColor = [UIColor colorWithWhite:0.90 alpha:1.0].CGColor;
	} completion: ^(BOOL finished) {
	}];
}

- (void)simulateDeHighlightForView:(UIView *)view {
	[UIView animateWithDuration:0.25 delay:0 options:UIViewAnimationOptionCurveEaseInOut animations: ^{
	    view.layer.backgroundColor = [UIColor colorWithWhite:1.0 alpha:0.0].CGColor;
	} completion: ^(BOOL finished) {
	}];
}

// Simulating highlights
- (IBAction)touchDragExit:(UIView *)sender {
	[self simulateDeHighlightForView:sender];
}

- (IBAction)touchUpOutside:(UIView *)sender {
	[self simulateDeHighlightForView:sender];
}

- (IBAction)touchCancel:(UIView *)sender {
	[self simulateDeHighlightForView:sender];
}

- (IBAction)touchUpInside:(UIView *)sender {
	[self simulateDeHighlightForView:sender];
}

// Simulating highlights
- (IBAction)touchDown:(UIView *)sender {
	[self simulateHighlightForView:sender];
}

- (IBAction)touchDragEnter:(UIView *)sender {
	[self simulateHighlightForView:sender];
}

```
