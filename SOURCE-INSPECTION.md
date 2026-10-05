# Source inspection — `diggo-master.zip`

Inspected and unpacked before implementation on 2026-10-05. The archive is a static HTML template named `diggo-master` (not a Next.js app). It contains 134 files, approximately 11.0 MB uncompressed, under these top-level folders: `css/`, `fonts/`, `images/`, `js/`, plus `index.html`.

## Complete file inventory

- `index.html`
- `css/`: `.DS_Store`, `animate.min.css`, `bootstrap-grid.css`, `bootstrap-grid.css.map`, `bootstrap-grid.min.css`, `bootstrap-grid.min.css.map`, `bootstrap-reboot.css`, `bootstrap-reboot.css.map`, `bootstrap-reboot.min.css`, `bootstrap-reboot.min.css.map`, `bootstrap.css`, `bootstrap.css.map`, `bootstrap.min.css`, `bootstrap.min.css.map`, `default-skin.css`, `font-awesome.min.css`, `icomoon.css`, `jquery-ui.css`, `jquery.fancybox.min.css`, `jquery.mCustomScrollbar.min.css`, `meanmenu.css`, `nice-select.css`, `normalize.css`, `owl.carousel.min.css`, `responsive.css`, `slick.css`, `style.css`.
- `fonts/`: `FontAwesome.otf`, `IcoMoon-Free.ttf`, `fontawesome-webfont.{eot,svg,ttf,woff,woff2}`, and Poppins `{Black,BlackItalic,Bold,BoldItalic,ExtraBold,ExtraBoldItalic,ExtraLight,ExtraLightItalic,Italic,Light,LightItalic,Medium,MediumItalic,Regular,SemiBold,SemiBoldItalic,Thin,ThinItalic}.ttf`.
- `images/`: `.DS_Store`, `banner.png`, `banner1.png`, `body_bg.png`, `bottom.png`, `box_img.png`, `business_img.jpg`, `loading.gif`, `logo.png`, `menu_icon.png`, `midil.png`, `plan1.png`, `projects_img.png`, `test.png`.
- `js/`: `.DS_Store`, `bootstrap.bundle.{js,js.map,min.js,min.js.map}`, `bootstrap.{js,js.map,min.js,min.js.map}`, `custom.js`, `jquery-3.0.0.min.js`, `jquery.mCustomScrollbar.concat.min.js`, `jquery.min.js`, `jquery.validate.js`, `modernizer.js`, `plugin.js`, `popper.min.js`, `slider-setting.js`.
- `js/revolution/`: `.DS_Store`; `assets/{coloredbg.png,gridtile.png,gridtile_3x3.png,gridtile_3x3_white.png,gridtile_white.png,loader.gif}`; `css/{closedhand.html,layers.css,navigation.css,openhand.html,settings.css}`; `fonts/pe-icon-7-stroke/css/pe-icon-7-stroke.css`; `fonts/pe-icon-7-stroke/fonts/{Pe-icon-7-strokebb1d.eot,Pe-icon-7-strokebb1d.svg,Pe-icon-7-strokebb1d.ttf,Pe-icon-7-strokebb1d.woff,Pe-icon-7-stroked41d.eot}`; `fonts/revicons/{revicons90c6.eot,revicons90c6.svg,revicons90c6.ttf,revicons90c6.woff}`; `js/.DS_Store`; `js/extensions/{revolution.extension.actions.min.js,revolution.extension.carousel.min.js,revolution.extension.kenburn.min.js,revolution.extension.layeranimation.min.js,revolution.extension.migration.min.js,revolution.extension.navigation.min.js,revolution.extension.parallax.min.js,revolution.extension.slideanims.min.js,revolution.extension.video.min.js}`; `js/{jquery.themepunch.revolution.min.js,jquery.themepunch.tools.min.js}`.

## Structure, routes, and components

There is one page and one route: `index.html` at `/` (static navigation links are `#`, with no real inner pages). No component files, React, TypeScript, API routes, MDX, server code, environment files, legal pages, 404 page, or 500 page are present. The page sections are: loader; header/navbar; hero/banner; business; projects; testimonial; contact form; footer. Naming is lowercase snake-free template naming with BEM-ish class names such as `banner_main`, `text-bg`, `business_box`, `projects_box`, `main_form`, `send_btn`.

## Design tokens and typography

No CSS custom properties or formal token system exists. Repeated source palette values are: `#0891f8` / `#008df3` bright blue, `#fdd430` yellow, `#38c8a8` green-teal, `#252525` dark charcoal, `#23262d`, `#272f43`, `#111111`, `#000000`, `#ffffff`, `#f9f9f9`, `#e6e1e1`, `#666666`, `#767676`, `#3e3e3e`, `#212121`, `#1f1f1f`. Backgrounds use image assets `body_bg.png`, `banner.png`, `test.png`, and `bottom.png`.

The stylesheet comments reference `Rajdhani`, `Poppins`, `Lato`, `Baloo Chettan`, and `Righteous`; only Poppins font files are bundled. Poppins includes regular, light, extra-light, medium, semibold, bold, extra-bold, black, thin, italic, and italic variants. `index.html` does not import bundled Poppins via `@font-face` or a webfont link; CSS relies on fallback/system availability. Source body copy is commonly 16–17px, hero heading 48px with 65px line-height, nav 16px uppercase, and source buttons 17px. No explicit CSS variable imports exist.

## Interactions and timing

`custom.js` hides the loader with `fadeToggle()` after exactly 1500ms. The loader is a fixed white full-screen layer (`z-index:9999999`) centering `images/loading.gif`, displayed at width 280px. The source does not include a wordmark/cursor/progress line. It initializes MeanMenu, Bootstrap tooltip, sticky header plugin, Owl carousels, validation, and other legacy plugin behavior. `slider-setting.js` configures a Revolution slider with a 5000ms delay, but that slider markup is not in `index.html`. No cookie consent, CAPTCHA, analytics, Meta Pixel, Three.js, WhatsApp, reCAPTCHA, Calendly, or API integration exists.

## Images and icons

The source uses only its local PNG/JPG/GIF art; there are no Pexels/Unsplash assets or image credits. Icons are Font Awesome 4 CSS and IcoMoon; the HTML uses Font Awesome social classes (`fa-facebook`, `fa-twitter`, `fa-linkedin`). It does not use Lucide. No icon-only component system exists.

## Forms and legal/error content

The only form is a non-wired contact form with Name, Phone Number, Email, Message, and Send. No server endpoint, validation processing, or CAPTCHA is implemented. There is no cookie banner or policy link, privacy policy, terms page, cookie policy, careers application, newsletter signup, booking form, enquiry form, or API environment variable. The original footer copy is `Free Multipurpose Responsive Landing Page 2019` and `Copyright 2019 All Right Reserved By Free html Templates` with Facebook/Twitter/LinkedIn placeholder links.

## Faithful reproduction decision

The implementation should preserve the source visual language: blue/yellow/teal palette, Poppins as the bundled font family, blue gradient/banner feel, white rounded CTA styling, loader duration of 1500ms, and the broad landing-page section rhythm. The requested Pulse Digital feature set is substantially larger than the supplied static source, so requested pages, legal/error states, forms, responsive behavior, Lucide icons, local CSS tokens, and accessible interactions are additions rather than elements found in the archive. The unpacked inspection is kept in `.source-inspection/` for reference; it is scratch/reference material and is not a production route.
