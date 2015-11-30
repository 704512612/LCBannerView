# LCBannerView

[**中文介绍**](https://github.com/LeoiOS/LCBannerView/blob/master/README-zh_CN.md)

🔥A very popular and highly customized banner view! And, infinite loop!

![LCBannerView](https://github.com/LeoiOS/LCBannerView/blob/master/LCBannerViewDemo.gif)
````
心有猛虎，细嗅蔷薇。
````



## Introduction

This is a display of advertising or information.

If you feel good, please give me a star, thank you! ⭐️

You can using the images from **local** or **internet**.



## Installation

LCBannerView is available on [CocoaPods](https://cocoapods.org/). Just add the following to your project Podfile:
````ruby
pod "LCBannerView"  # Podfile
````



## Non-CocoaPods Installation

Just drag the LCBannerView folder into your project.



## Usage

* Use by including the following import:
````objc
#import "LCBannerView"
````
* Demo code:
````objc
// 1. from internet
[scrollView addSubview:({
    
    LCBannerView *bannerView = [LCBannerView bannerViewWithFrame:CGRectMake(0, 300.0f, [UIScreen mainScreen].bounds.size.width, 200.0f)
                                                        delegate:self
                                                       imageURLs:URLs
                                                placeholderImage:nil
                                                   timerInterval:2.0f
                                   currentPageIndicatorTintColor:[UIColor redColor]
                                          pageIndicatorTintColor:[UIColor whiteColor]];
    bannerView;
})];

// 2. from local
// please find out the code from the demo
````

* Delegate (`@optional`):
````objc
- (void)bannerView:(LCBannerView *)bannerView didClickedImageIndex:(NSInteger)index;
````
* For example:
````objc
- (void)bannerView:(LCBannerView *)bannerView didClickedImageIndex:(NSInteger)index {
      
      NSLog(@"you clicked image in %@ at index: %ld", bannerView, (long)index);
}

// logs
2015-11-30 17:36:20.611 LCBannerViewDemo[6075:456257] you clicked image in <LCBannerView: 0x7fc98b751ff0; frame = (0 300; 375 200); layer = <CALayer: 0x7fc98b7521b0>> at index: 1
2015-11-30 17:36:21.292 LCBannerViewDemo[6075:456257] you clicked image in <LCBannerView: 0x7fc98b433190; frame = (0 20; 375 200); layer = <CALayer: 0x7fc98b42ce20>> at index: 1
2015-11-30 17:36:21.801 LCBannerViewDemo[6075:456257] you clicked image in <LCBannerView: 0x7fc98b751ff0; frame = (0 300; 375 200); layer = <CALayer: 0x7fc98b7521b0>> at index: 2
2015-11-30 17:36:22.380 LCBannerViewDemo[6075:456257] you clicked image in <LCBannerView: 0x7fc98b433190; frame = (0 20; 375 200); layer = <CALayer: 0x7fc98b42ce20>> at index: 3
````



## Thanks
* [SDWebImage](https://github.com/rs/SDWebImage)



## Support
* If you have any questions, please commit a issure! Thx!
* Email: leoios@sina.com
* Blog: http://www.leodong.com



### License
[MIT License](http://opensource.org/licenses/MIT)
