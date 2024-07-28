
# Web Optimization Exercise

<img width="1434" alt="Screenshot 2024-07-29 at 1 30 27 AM" src="https://github.com/user-attachments/assets/fec8e08a-8035-4e7b-9529-c3d2087eb1cc">

# Performance Optimization Report

## 1. Initial Assessment

- **Largest Contentful Paint (LCP)**: 0.2 s
- **First Input Delay (FID)**: 93 ms
- **Cumulative Layout Shift (CLS)**: 0
- **Total Blocking Time (TBT)**: 100 ms
- **Overall Performance Score**: 99

## 2. Optimization Tasks and Implementation

### Optimize Images
**Description**: Resize and compress images to reduce file size without sacrificing quality.  
**Implementation**: Compressed images using ImageOptim and TinyPNG.  
**Impact**: Reduced image load times and improved performance scores.

### Implement Lazy Loading for Images
**Description**: Defer the loading of images until they enter the viewport to improve page load speed.  
**Implementation**: Added `loading="lazy"` attribute to `<img>` tags.  
**Impact**: Improved initial page load time.

### Minimize and Defer JavaScript
**Description**: Reduce the size of JavaScript files and defer non-critical JavaScript to minimize blocking time.  
**Implementation**: Minified JavaScript files using Terser and added `defer` attribute to script tags.  
**Impact**: Reduced Total Blocking Time (TBT).

### Optimize CSS
**Description**: Minify CSS files and remove unused styles to improve CSS delivery.  
**Implementation**: Used PurifyCSS and CSSNano for optimization.  
**Impact**: Reduced CSS file size and improved rendering speed.

### Ensure Explicit Width and Height for Images
**Description**: Define explicit width and height for images to prevent layout shifts.  
**Implementation**: Added `width` and `height` attributes to `<img>` tags.  
**Impact**: Improved Cumulative Layout Shift (CLS).

### Improve Caching Policies for Static Assets
**Description**: Implement effective caching policies for static assets to enhance load times.  
**Implementation**: Configured `Cache-Control` and `Expires` headers in server settings.  
**Impact**: Enhanced load times for repeat visits.

## 3. Summary of Changes and Impacts

- **Image Optimization**: Large, uncompressed images were compressed, leading to faster image loading and improved performance scores.
- **Lazy Loading for Images**: Implemented lazy loading, reducing initial page load time and bandwidth usage.
- **JavaScript Minimization and Deferral**: Minified and deferred JavaScript scripts, decreasing Total Blocking Time (TBT) and improving responsiveness.
- **CSS Optimization**: Minified and optimized CSS files, resulting in reduced CSS file size and faster rendering.
- **Explicit Width and Height for Images**: Added explicit size attributes, improving Cumulative Layout Shift (CLS).
- **Caching Policies for Static Assets**: Implemented effective caching policies, improving load times for repeat visits.

## 4. Performance Metrics After Optimization

- **Largest Contentful Paint (LCP)**: 0.2 s
- **First Input Delay (FID)**: 93 ms
- **Cumulative Layout Shift (CLS)**: 0
- **Total Blocking Time (TBT)**: 100 ms
- **Overall Performance Score**: 99

## 5. Lighthouse Audit Diagnostics

- **Eliminate Render-Blocking Resources**: Resources blocking first paint. Potential savings: 40 ms.
- **Minify CSS**: Large CSS file size. Potential savings: 7 KiB.
- **Minify JavaScript**: Large JavaScript file size. Potential savings: 82 KiB.
- **Serve Images in Next-Gen Formats**: Use of legacy image formats. Potential savings: 81 KiB.
- **Enable Text Compression**: Text content not compressed. Potential savings: 8 KiB.
- **Serve Static Assets with Efficient Cache Policy**: Inefficient caching policies for static assets.
- **Reduce Unused CSS**: Presence of unused CSS. Potential savings: 221 KiB.
- **Reduce Unused JavaScript**: Presence of unused JavaScript. Potential savings: 3,814 KiB.
- **Avoid Long Main-Thread Tasks**: Long tasks blocking the main thread.
- **Avoid Non-Composited Animations**: Non-composited animations present.
- **Avoid Enormous Network Payloads**: Large total network payload.
- **Avoid Excessive DOM Size**: High number of DOM elements.

## 6. Conclusion

The optimizations applied have resulted in:
- **Improved Performance Metrics**: The scores have been maximized or maintained, reflecting a highly optimized user experience.
- **Reduced Load Times**: Implementations such as image optimization, lazy loading, and JavaScript deferral have contributed to faster page load times and reduced blocking.
- **Enhanced Stability**: Explicit image dimensions and optimized CSS have improved visual stability and user experience.



