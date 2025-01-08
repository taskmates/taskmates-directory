Breakpoints:

- Desktop: 992px and above
- Tablet: 768px to 991px
- Mobile Landscape: 480px to 767px
- Mobile Portrait: 479px and below

Style changes cascade both up and down (bidirectional cascade). They cascade up starting from 992px (desktop) and down from desktop to mobile. This means that styles applied on desktop, 1280px, 1440px, and 1920px cascade up to larger devices and styles you set on the desktop breakpoint cascade down and apply to the tablet and both mobile device sizes. All styles set on tablet will be carried over to the mobile breakpoints. You can override any styles inherited from a higher breakpoint.

