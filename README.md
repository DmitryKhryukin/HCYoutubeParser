##HCYoutubeParser

HCYoutubeParser is a class which lets you get the iOS compatible video url from YouTube so you don't need to use a `UIWebView` or open the YouTube Application.


It's really simple to get going
	
	// Gets an dictionary with each available youtube url
    NSDictionary *videos = [HCYoutubeParser h264videosWithYoutubeURL:[NSURL URLWithString:@"http://www.youtube.com/watch?v=8To-6VIJZRE"]];
	
	// Presents a MoviePlayerController with the youtube quality medium
	MPMoviePlayerViewController *mp = [[[MPMoviePlayerViewController alloc] initWithContentURL:[NSURL URLWithString:[videos objectForKey:@"medium"]]] autorelease];
	[self presentModalViewController:mp animated:YES];
	
