Responsive Flower Layout with Leaf Petals
Overview
This project features a visually engaging "flower" layout where each leaf represents a clickable petal, each linking to different resources. The desktop view showcases a creative circular arrangement of these leaves, with background images and overlay text. On mobile and tablet views, the design transitions to a more practical tab-based layout where each leaf becomes a horizontal, stackable tab.

The layout is built with HTML and CSS, using media queries to provide responsive design adjustments across devices.

File Structure
HTML

Each petal or "leaf" is an <a> tag containing an image, overlay text, and mobile-friendly tab content.
The structure ensures both desktop (flower) and mobile (tab) versions have the appropriate elements to display.
CSS

The styles ensure that the leaf petals are positioned and rotated to form a flower shape on desktop.
For mobile and tablet views, the CSS hides the leaf images and overlay text, instead showing the mobile-friendly tab content.
The responsive layout is controlled using media queries, targeting mobile (max-width: 767px) and tablet (max-width: 1024px) devices.
Features
Desktop View (Width: Above 1024px)
Flower Layout: Each link (<a>) is designed as a leaf/petal with an image (leaf-image) and overlay text (leaf-overlay-text). These are rotated and positioned to create a flower-like arrangement.
Hover Effects: The background images and overlay text are visible, adding a dynamic look to the leaf elements when hovered.
Leaf Center: An image in the center of the flower provides a cohesive look for the entire design.
Mobile & Tablet View (Width: Below 1024px)
Tab Layout: The leaf images and overlay text are hidden, and the mobile-friendly content (leaf-mobile) is displayed. Each tab contains:
An icon (leaf-icon)
A title (leaf-title)
The tabs are stacked vertically, making it easier to browse on smaller screens.
Responsive Design
Media Queries: Media queries control how the layout adapts to different screen sizes:
On screens wider than 1024px (desktop), the flower layout is displayed.
On screens between 768px and 1024px (tablet), the leaf images and overlay text are hidden, and the tab content is shown.
On screens smaller than 767px (mobile), the layout changes completely to a stacked tab structure.
Code Explanation
HTML
Each leaf is represented as follows:

html
Copy code
<a href="/link" id="leaf-1" class="leaf" title="Leaf Title">
    <div class="leaf-image" style="background-image:url('image-url');"></div>
    <span class="leaf-overlay-text">Overlay Text</span>
    <span class="leaf-mobile">
        <img class="leaf-icon" src="image-url" alt="Icon Description">
        <h4 class="leaf-title">Title</h4>
    </span>
</a>
leaf-image: The background image used in the desktop view to create the petal.
leaf-overlay-text: The text overlay positioned over the petal image.
leaf-mobile: Contains the icon and title to display in mobile view.
CSS
Flower Layout (Desktop)
css
Copy code
#leaf-1 .leaf-image {
    width: 40%;
    height: 40%;
    position: absolute;
    top: 30%;
    left: 25%;
    transform: rotate(-45deg); /* Rotates the image for alignment */
}
Each leaf has a different rotation to align it in a circular flower shape. The images and text overlays are positioned and rotated to fit within the petal structure.

Tab Layout (Mobile & Tablet)
css
Copy code
@media (max-width: 1024px) {
  .leaf-image,
  .leaf-overlay-text {
    display: none; /* Hide images and text on mobile and tablet */
  }

  .leaf-mobile {
    display: block; /* Show mobile-friendly tab content */
  }
}
For smaller screens, the leaf images and overlay text are hidden. Instead, the leaf-mobile content (icon and title) is displayed as a simple, user-friendly tab.

Customization
Adding New Leaves
To add a new leaf, simply replicate the structure of the existing <a> tags. Update the following:

Href: Update the link to point to the desired destination.
Background Image: Update the URL in the style attribute of leaf-image.
Overlay Text: Modify the content within leaf-overlay-text to suit the new link.
Mobile Icon: Update the leaf-icon image for mobile view.
Adjusting Layout
To change the size, position, or rotation of the petals in the flower, modify the values inside .leaf-image and .leaf-overlay-text (e.g., width, height, top, left, and transform).
To adjust the appearance of the mobile and tablet tabs, tweak the styles in the @media queries.
Known Issues
Images Overlapping on Smaller Screens: If images or text appear in mobile or tablet views when they shouldn’t, ensure the media queries hide the .leaf-image and .leaf-overlay-text properly.
Leaf Positioning: The positioning of the leaves is absolute, so adjusting one leaf might require adjusting others to maintain the flower shape.
Future Enhancements
Animations: Consider adding hover animations or transitions between views to enhance the user experience.
Interactive Tabs: For mobile views, make the tabs collapsible for a cleaner layout on smaller screens.
Credits
This project is part of the Urban Baby Beginnings initiative to provide user-friendly access to various maternal health resources.
