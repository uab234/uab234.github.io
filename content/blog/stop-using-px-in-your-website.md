---
title: "Stop Using .px for font-size, embrace .rem for accessibility web design"
#description: "Why you should stop using px in your website project"
layout: "blog"
url: "/blog/stop-using-px-in-your-website-font-size"
weight: 1
# aliases: ["/first"]
# tags: ["first"]
author: "Umar"
#author: ["Me", "You"] # multiple authors
showToc: false
TocOpen: false
draft: false
hidemeta: false
comments: false
canonicalURL: "https://uab234.github.io/to/page"
ShowCodeCopyButtons: true
ShowShareButtons: true
disableHLJS: true # to disable highlightjs
disableShare: false
disableHLJS: false
hideSummary: false
searchHidden: false
ShowReadingTime: true
ShowBreadCrumbs: true
ShowPostNavLinks: true
ShowWordCount: true
ShowRssButtonInSectionTermList: false
UseHugoToc: true
ShareButtons: ["linkedin", "twitter"] # To customize which share buttons to be enabled on page

cover:
    imageUrl: "/blog/coming-soon.jpg" # image path/url
    #alt: "eid celebration moon flyer" # alt text
    #caption: "Write a photo caption" # display caption under cover
    relative: false # when using page bundles set this to true
    hidden: false # only hide on current single page

#editPost:
    #URL: "https://uab234.github.io"
    #Text: "Suggest Changes" # edit text
    #appendFilePath: true # to append file path to Edit link
---
In the evolving world of web design, flexibility and scalability are key. As we design for a multitude of devices and screen sizes, it's essential to adopt practices that ensure our designs are both accessible and responsive. One crucial practice is the shift from using pixels (px) to root ems (rem) for defining font sizes in CSS. In this post, we'll explore why using rem units can significantly enhance your web design projects and how to make the transition smoothly.

## Understanding px, em, and rem

- **Pixels (px)**: Traditionally, web designers have used pixels to define font sizes. Pixels are a fixed unit of measurement, which makes them predictable and easy to understand. However, their rigidity is also their biggest drawback. As screen sizes and resolutions vary, pixel-based designs can struggle to maintain consistency across different devices.

- **Ems (em)**: An em is a relative unit of measurement based on the font size of its closest parent element. For example, if the font size of a parent element is 16px, then 1em equals 16px. While em units offer more flexibility than pixels, they can lead to complex calculations and inheritance issues, as each em is relative to its parent element.

- **Root ems (rem)**: The rem unit, introduced in CSS3, stands for "root em." Unlike em, rem units are relative to the root element (<html>) font size, which is typically set to 16px by default in most browsers. This creates a consistent and scalable unit of measurement that simplifies responsive design.

## Why Choose .rem over .px

1. ### Scalability and Accessibility

- **User Preferences**: Modern browsers allow users to set their preferred font size. By using rem units, your design respects these preferences, ensuring better accessibility for users with visual impairments.

- **Zoom and Resize**: Designs based on rem units scale more naturally when users zoom in or resize their browser windows, maintaining readability and usability.

2. ### Consistency

- **Design Uniformity:** rem units provide a consistent scaling factor across the entire website, making it easier to maintain uniformity in your design. Adjusting the root font size adjusts all rem-based measurements proportionally.

- **Simplified Calculations**: Since rem units are relative to the root font size, there's no need to consider the cascading effects of nested elements, as with em units.

### Transitioning from px to rem

1. **Set a Base Font Size**: Begin by defining a base font size for your root element (<html>). The default is usually 16px, but you can adjust this based on your design needs. For example:

```CSS
html {
    font-size: 16px;
}
```

2. **Convert px to rem**: To convert pixel values to rem, divide the pixel value by the root font size. For instance, 16px becomes 1rem, 24px becomes 1.5rem, and so on. Here’s a quick conversion example:

```CSS
/* Old px-based values */
h1 {
    font-size: 32px;
}
p {
    font-size: 16px;
}

/* New rem-based values */
h1 {
    font-size: 2rem; /* 32px / 16px = 2rem */
}
p {
    font-size: 1rem; /* 16px / 16px = 1rem */
}
```

3. **Testing and Refining**: Thoroughly test your website across different device browsers to ensure the rem units are functioning as expected.

### Common Pitfalls and How to Avoid Them

1. **Ignoring Browser Defaults**: Remember that browser defaults can vary. Always set a base font size in your CSS to ensure consistency across different environments.

2. **Complexity in Mixed Units**: Avoid mixing px, em, and rem units in your font-size, as this can lead to confusion and inconsistency. Stick to rem unit to maintain uniformity.

3. **Over-reliance on Default Sizes**: While it's convenient to rely on default sizes, customize your root font size to match your design specifications. This ensures your design looks good on all devices.

*I find this youtube video by Coder Coder useful, I recommend watching it.*

{{< youtube xCSw6bPXZks >}}

### Conclusion

Embracing ***rem*** units over ***px*** is a step towards creating more accessible, and scalable websites. By making this transition, you ensure that your websites are better equipped to handle the diverse range of user preferences in today's digital landscape.

*Happy designing!*
