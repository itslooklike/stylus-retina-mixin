# stylus-retina-mixin
stylus retina mixin

Example:

params: `url`, `file format`, `width`, `height`, `retina scale`

input

    .class
      mixin-retina-bg('src/alert', jpg, 300, 500, 3)
 
output

    .class {
      background-image: url("src/alert.jpg");
      background-size: 300 500;
      background-repeat: no-repeat;
    }
    @media (min-resolution: 144dpi), (min-resolution: 1.5dppx) {
      .class {
        background-image: url("src/alert@2x.jpg");
      }
    }
    @media (min-resolution: 240dpi), (min-resolution: 2.5dppx) {
      .class {
        background-image: url("src/alert@3x.jpg");
      }
    }

best with autoprefixer
