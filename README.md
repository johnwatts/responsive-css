# Powerpoint presentation

<a href="https://github.com/johnwatts/responsive-css/blob/master/Responsive%20Design.pptx?raw=true">Download</a>

# Exercises

## 1. Start with a trivial site. Responsive but dull.

Create a basic web page with just a title and a bit of content. Resize the browser window and note that the content adjusts to fit within the width of the viewport. Open developer tools and simulate a mobile device. The content is displayed reasonably well across all the different viewport sizes.

<a href="https://github.com/johnwatts/responsive-css/archive/1.zip">Download Source</a>

## 2. Add bootstrap the easy way (from a CDN) and include the default template.

Add boostrap as described under Bootstrap CDN http://getbootstrap.com/getting-started/#download-cdn. Move all the content in the `<body>` into a `<div class="container-fluid">`. Note that not much changes. The style is a little different and just like before the arrangement of the content responds to the viewport width. Add the <meta> tags from the Basic Template at http://getbootstrap.com/getting-started/#template. These ensure the document is not in IE backwards-compatibility mode and it will use the same default zoom level for both portrait and landscape on a mobile device.

<a href="https://github.com/johnwatts/responsive-css/archive/2.zip">Download Source</a>

## 3. Add some content using the grid system. Use appropriate column widths at the different breakpoints.

Read http://getbootstrap.com/css/#grid-intro and skim a few examples. Then add some content in a few separate container `<div>`s and assign some of the `.col-*-*` classes to them. Resize the window and see how the content layout adjusts.

<a href="https://github.com/johnwatts/responsive-css/archive/3.zip">Download Source</a>

## 4. Add a responsive table, which will scroll horizontally on small viewports.

Add a table with a few rows and columns. Note how the table is poorly styled. Note that when you resize the window to be very narrow the table wraps across many lines trying to fit within the width. Add the .table class as shown at http://getbootstrap.com/css/#tables-example. The styling is much better. Now nest the table inside a `<div class="table-responsive">` as shown at http://getbootstrap.com/css/#tables-responsive. Note that when you resize the window to be very narrow the table scrolls horizontally.

<a href="https://github.com/johnwatts/responsive-css/archive/4.zip">Download Source</a>

## 5. Add a navbar.

Add a navbar to the top of the page, as shown in http://getbootstrap.com/components/#navbar. The explanation and example are a bit wordy. A minimal collapsible navbar is:

    <nav class="navbar navbar-default">
        <div class="container-fluid">
            <div class="navbar-header">
                <button type="button" class="navbar-toggle collapsed" data-toggle="collapse" data-target="#navbar-collapsible" aria-expanded="false">
                    <span class="icon-bar"></span>
                    <span class="icon-bar"></span>
                    <span class="icon-bar"></span>
                </button>
                <a class="navbar-brand" href="#">Brand</a>
            </div>
            <div class="collapse navbar-collapse" id="navbar-collapsible">
                <ul class="nav navbar-nav">
                    <li>
                        <a href="#site">A Link</a>
                    </li>
                    <!-- Add more links! -->
                </ul>
            </div>
        </div>
    </nav>

<a href="https://github.com/johnwatts/responsive-css/archive/5.zip">Download Source</a>

## 6. Add a responsive banner image.

Add a very wide image to the top of the page. Give it the class `.img-responsive`. Note that it takes up the full width of the viewport until doing so would require sizing it over 100% of its original size. See http://getbootstrap.com/css/#images.

<a href="https://github.com/johnwatts/responsive-css/archive/6.zip">Download Source</a>

## 7. Add a responsive embed of a YouTube video

Follow the example at http://getbootstrap.com/components/#responsive-embed. Note that the embedded element always takes up the full size of its container while maintaining the same ratio of width to height.

<a href="https://github.com/johnwatts/responsive-css/archive/7.zip">Download Source</a>

## 8. Position some images left, right and center

Try positioning some images to the left, right and center of the parent element. Read http://getbootstrap.com/css/#helper-classes-floats and http://getbootstrap.com/css/#helper-classes-center. For details. You'll need http://getbootstrap.com/css/#helper-classes-clearfix after floating elements left or right in order to position the following elements below the floated ones. Resize the window and note how the elements shift when there isn't enough space for them.

<a href="https://github.com/johnwatts/responsive-css/archive/8.zip">Download Source</a>

## 9. Add a modal dialog

Add a modal dialog. The simplest example to start from is at http://getbootstrap.com/javascript/#modals-sizes. Resize the window and see how the modal resizes, eventually taking up the full width of the screen. Note the limitations for modals on mobile devices at http://getbootstrap.com/getting-started/#support-fixed-position-keyboards.

<a href="https://github.com/johnwatts/responsive-css/archive/9.zip">Download Source</a>

## 10. Add a tabbed content section

Move some content into separate tabs of a single section. See http://getbootstrap.com/javascript/#markup for an example.

<a href="https://github.com/johnwatts/responsive-css/archive/10.zip">Download Source</a>

## 11. Add a carousel

Follow the example at http://getbootstrap.com/javascript/#carousel.

<a href="https://github.com/johnwatts/responsive-css/archive/11.zip">Download Source</a>

## 12. Make navbar fixed to top of screen.

The basic navbar is attached to the top of the page and scrolls with it. Instead, make the navbar fixed to the top of the screen so it is always visible as shown at http://getbootstrap.com/components/#navbar-fixed-top. You will likely want to work around some undesirable side effects:

1. Add padding-top to the body so that the top of the page won't be covered by the navbar.
2. Reserve space over the elements you are navigating to so the navbar won't cover them after navigating. http://stackoverflow.com/questions/10732690/offsetting-an-html-anchor-to-adjust-for-fixed-header.
3. Make the nav menu close after an item is selected. http://stackoverflow.com/questions/21203111/bootstrap-3-collapsed-menu-doesnt-close-on-click.

<a href="https://github.com/johnwatts/responsive-css/archive/12.zip">Download Source</a>

## 13. Add a high DPI image to be shown only on retina displays.

Use the technique from http://getbootstrap.com/css/#less-mixins-retina-images to show a higher-DPI image when on a retina display. To do this, you must switch from an `<img>` to a `<div>` with a known class or ID and then use CSS background-image to choose the appropriate image URL. There are two ways to write the CSS:

1. Compile bootstrap from the less files as shown at the top of the "Using Less" section.
2. Extract all the CSS from the sample shown and replace the token like "@{file-2x}" with the actual filenames.

If you apply this to a responsive image, you will have to add some additional CSS to keep it responsive. Try setting the CSS:

    height: 100px;
    background-size: cover;

And then using media queries to set an appropriate height at each breakpoint.

<a href="https://github.com/johnwatts/responsive-css/archive/13.zip">Download Source</a>