# Standard Web

## [Layers for composition](https://www.youtube.com/watch?v=II6Szc2UPxw)
- only transform and opacity for animations
- Promote moving elements with will-change or translateZ
- Avoid overusing
- [details](https://developers.google.com/web/fundamentals/performance/rendering/stick-to-compositor-only-properties-and-manage-layer-count)

## [Fit to page](https://www.youtube.com/watch?v=299RZ0d1LQY)
- Set min-height: 100vh and position relative to body tag
- Set a backgrounf color on HTML for overscroll

## [Icons Fonts](https://www.youtube.com/watch?v=GnYoJY2zvvc) 
- use title
- look same everywhere

## [Align content Vertically](https://www.youtube.com/watch?v=5IP43MTfj0E)
- flexBox

## [form validation](https://www.youtube.com/watch?v=MppB5jaKyZ4)
- required
- pattern
- `this.form.checkValidy`
```css
input:invalid + div:hint {
background : red
}
``` 
- type

## [Theming](https://www.youtube.com/watch?v=5fEMTxpA6BA)
- Web app Manifest
- meta theme-color
- high res icon for mobile

## [Handle Back and Forwards](https://www.youtube.com/watch?v=KSfhW1hTOvw)
- `history.pushState(state, null, '/urltoSave')` 
- `window.onpopstate = () => console.log('new location')` 

## [Images](https://www.youtube.com/watch?v=Bd6Lkduupbc)
- jpeg
- png ( pngcruch -ow image.png)
- load image when displayed 
  ```js
  function scrollHandler = function(event){
    if (document.body.scrollTop > 1000){
        myImage.src = 'image-to-load.jpeg';
        document.removeEventListener('scroll', scrollHandler);
    }
    document.addEventListener('scroll', scrollHandler)
  ```