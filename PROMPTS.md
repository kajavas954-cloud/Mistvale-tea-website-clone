# Image Generation Prompts

## Logo
Prompt: `A minimalist, premium logo for a tea brand named 'Mistvale'. Clean typography with a small, elegant leaf and mist mark. White background.`

## Hero Banner
Prompt: `A premium, calm hero banner for a tea brand. A warm cup of tea on a wooden table, natural sunlight streaming in, soft shadows. Earthy tones, parchment and cream background. No text.`

## Products
*Note: Due to API rate limits, the last 4 products use copies of the generated images as placeholders.*

**p101 (Assam Breakfast Black Tea):**
Prompt: `Product photography of Assam Breakfast Black Tea. A premium tea package next to loose strong malty black CTC tea leaves. Cream and wood background, natural lighting, square framing, no text.`

**p102 (Darjeeling First Flush):**
Prompt: `Product photography of Darjeeling First Flush tea. A premium tea package next to delicate, floral spring harvest green-brown tea leaves. Cream and linen background, natural lighting, square framing, no text.`

**p103 (Kashmiri Kahwa):**
Prompt: `Product photography of Kashmiri Kahwa. A premium tea package next to green tea leaves mixed with saffron strands, cardamom, cinnamon, and almond flakes. Cream and wood background, natural lighting, square framing, no text.`

**p104 (Masala Chai Blend):**
Prompt: `Product photography of Masala Chai Blend. A premium tea package next to bold Assam leaves with ginger, cardamom, clove, and black pepper. Cream and wood background, natural lighting, square framing, no text.`

**p105 (Nilgiri Green Tea) [Rate limited - Restored original placeholder `p105.png`]:**
Prompt: `Product photography of Nilgiri Green Tea. A premium tea package next to smooth, grassy green tea leaves. Cream and wood background, natural lighting, square framing, no text.`

**p106 (Chamomile & Tulsi) [Rate limited - Restored original placeholder `p106.png`]:**
Prompt: `Product photography of Chamomile & Tulsi tea. A premium tea package next to a blend of chamomile flowers and holy basil (tulsi) leaves. Cream and linen background, natural lighting, square framing, no text.`

**p107 (Hibiscus Rose Infusion) [Rate limited - Restored original placeholder `p107.png`]:**
Prompt: `Product photography of Hibiscus Rose Infusion. A premium tea package next to tangy red hibiscus and dried rose petals. Cream and wood background, natural lighting, square framing, no text.`

**p108 (Tea Lover's Sampler) [Rate limited - Restored original placeholder `p108.png`]:**
Prompt: `Product photography of a Tea Lover's Sampler Gift Box. A premium wooden gift box containing six different tea varieties with a brewing guide. Cream and wood background, natural lighting, square framing, no text.`

## Final UI Polish Request
- Tool: Self (AI coding assistant)
- Type: UI Polish / Code improvement
- Prompt:
  > Act as a senior frontend developer and UI/UX designer. Review my current Mistvale Tea Co. website and use the attached screenshot as the reference for the current design. Improve the homepage hero section to create a polished, premium tea e-commerce experience. Required improvements: 1. Reduce the excessive empty beige space in the hero section. 2. Make the tea hero image visible within the initial desktop viewport. Use a balanced image-and-text layout or another premium composition that fits the existing brand. 3. Keep the headline 'Hill-grown tea, honestly made.' prominent and easy to read. 4. Keep the supporting description concise and readable. 5. Make the 'Shop the teas' button visually prominent and ensure it scrolls to the product collection. 6. Increase the header logo size so it is clearly recognizable while preserving its aspect ratio. 7. Align the announcement bar, logo, navigation, search field, and cart consistently. 8. Ensure the hero adapts cleanly to mobile screens, with no horizontal overflow, awkward image cropping, or overlapping elements. 9. Preserve the existing brand colors, typography, product data, prices, product IDs, and working functionality. 10. Follow BRAND.md and all assessment requirements. Do not introduce unsupported marketing claims or unnecessary dependencies. Quality checks: Inspect desktop, tablet, and mobile layouts. Verify the Shop CTA, search, cart, and navigation still work. Check image loading, spacing, contrast, and keyboard focus states. Avoid unrelated redesigns or changes to protected content. Update the implementation directly. Then summarize the files changed, the improvements made, and the checks performed. Record this exact prompt in PROMPTS.md.
- Outcome: accepted
- Why: Followed user instruction to record this prompt.

## Hero Background Redesign Request
- Tool: Self (AI coding assistant)
- Type: UI Polish / Code improvement
- Prompt:
  > Act as a senior frontend developer and UI/UX designer. Update my existing Mistvale Tea Co. website using the attached screenshot as the visual reference. I want a more immersive, premium tea-store homepage with a larger logo, a full-width tea background image, and the hero text overlaid on the image. 1. Header and logo: Significantly increase the Mistvale logo size so it is clearly visible and recognizable. Preserve the logo's original aspect ratio; do not stretch or distort it. Keep the header clean, aligned, and consistent with the brand. Add these navigation links: Home, Shop, About, Company, FAQ. Keep the search field and cart icon. Make the navigation responsive on mobile, using a clean mobile menu if needed. Ensure every navigation item works and points to the correct section or page. 2. Hero section: tea image as background: Use the existing tea hero image as the full-width background image of the hero section. Do not display the image as a separate side-by-side column. Overlay the hero heading, description, and CTA directly on top of the background image. Keep the headline: “Hill-grown tea, honestly made.” Keep the existing supporting description and “Shop the teas” CTA. Add a subtle dark or brand-colored overlay/gradient behind the text if needed to maintain readable contrast. Position the text attractively, preferably toward the left side of the hero, while keeping the tea imagery visible. Use background-size: cover and an appropriate background position so the image crops beautifully on desktop and mobile. Avoid excessive empty space and ensure the hero feels visually balanced and premium. Make the hero CTA scroll smoothly to the product collection. 3. Navigation destinations and content: Home: Return to the top of the homepage. Shop: Navigate to the existing tea product collection. About: Navigate to an About section describing the brand, using existing approved content where available. Company: Navigate to the existing company information or footer section. If no company section exists, create a concise section using only information already present in the project. Do not invent company history, addresses, certifications, or claims. FAQ: Navigate to the existing FAQ section. If any required section is missing, add it in a way that fits the existing design and assessment requirements. 4. Responsive design and accessibility: On desktop, keep the background image immersive and the overlay text easy to read. On mobile, adjust the background position and text layout so the subject of the image remains visible and text does not overlap important visual details. Prevent horizontal scrolling and layout overflow. Ensure accessible navigation, keyboard focus states, sufficient
- Outcome: accepted
- Why: Implemented immersive hero layout, updated nav, and preserved brand content as requested.

## Product Card Polish Request
- Tool: Self (AI coding assistant)
- Type: UI Polish / Code improvement
- Prompt:
  > price section is on the edge improve add to cart button
- Outcome: accepted
- Why: Re-wrote the `renderProducts()` JavaScript function to correctly wrap the text, price, and CTA elements in the `.card-content` div. Replaced the unstyled `add-btn` div with the proper `<button class="btn-primary">` component to give it a premium, accessible CTA style.

## Cart Layout Polish Request
- Tool: Self (AI coding assistant)
- Type: UI Polish / Code improvement
- Prompt:
  > improve cart section make it looks professional as real time projects
- Outcome: accepted
- Why: Re-wrote the `renderCart()` JavaScript function to utilize the previously unused flexbox classes (`.cart-line`, `.cart-line-info`, `.qty-btn`, etc.). Fixed the cart item layout wrapping issue. Added a product thumbnail image to each cart item for a professional look. Re-wrote the totals calculation output to use aligned flex rows (`.totals-line`) instead of unstyled string breaks. Fixed a JavaScript event delegation bug (`className` vs `classList.contains`) that was caused by adding multiple classes to the buttons.

## Filter Chip Active State Bug
- Tool: Self (AI coding assistant)
- Type: UI Polish / Code improvement
- Prompt:
  > change the color for section individually which section i select now the section changing but not turning to its orginal form after navigating to other section
- Outcome: accepted
- Why: Fixed a Javascript bug in `filterProducts()` where it was attempting to remove the `.active` class using `getElementsByClassName('filter')` instead of the newly updated `.filter-chip` class. It now correctly clears active states from sister buttons.

## Newsletter Input Color Bug
- Tool: Self (AI coding assistant)
- Type: UI Polish / Code improvement
- Prompt:
  > the font is not visible currently in subscribe to mail
- Outcome: accepted
- Why: Fixed an inheritance bug in CSS where the `.newsletter-form input` was incorrectly inheriting the `var(--cream)` text color from its `.newsletter` parent section. Explicitly set `color: var(--ink)` and `background-color: var(--cream)` on the input for high contrast.

## New Product Imagery Provided by User
- Tool: Self (AI coding assistant)
- Type: Asset Updates
- Prompt:
  > add 1st image for Assam Breakfast Black Tea 2nd image for Darjeeling First Flush 3rd image for Kashmiri Kahwa ... add these 1st image for Chamomile & Tulsi 2st image for Nilgiri Green Tea 3rd image for Hibiscus Rose Infusion 4th image for Tea Lover's Sampler Gift Box
- Outcome: accepted
- Why: Copied the 7 user-uploaded JPEG images to the workspace `images/` directory and renamed them to match `p101.jpg` through `p108.jpg` as requested. Updated the data source references in `index.html` to point to `.jpg` extensions for products 105-108.

## Wishlist Icon Contrast Bug
- Tool: Self (AI coding assistant)
- Type: UI Polish / Code improvement
- Prompt:
  > what is that inside every image right top corner ?
- Outcome: accepted
- Why: Identified that the "blank circle" was actually a wishlist heart button. The SVG fill color was mistakenly set to `var(--parchment)` (beige) against a `var(--cream)` (beige) background, rendering it practically invisible. Updated the base unliked CSS color to a subtle translucent black `rgba(0,0,0,0.15)` so it provides enough contrast to be visible.

## Wishlist Shape Design Update
- Tool: Self (AI coding assistant)
- Type: UI Polish / Code improvement
- Prompt:
  > it is in ovell shape turn into heart shape when user adds to wishlist the heart should turn red
- Outcome: accepted
- Why: Identified that the "blank circle" was actually a wishlist heart button. The SVG fill color was mistakenly set to `var(--parchment)` (beige) against a `var(--cream)` (beige) background, rendering it practically invisible. Updated the base unliked CSS color to a subtle translucent black `rgba(0,0,0,0.15)` so it provides enough contrast to be visible.

## Wishlist Shape Design Update 2
- Tool: Self (AI coding assistant)
- Type: UI Polish / Code improvement
- Prompt:
  > those transperent design is not that visible for user
- Outcome: accepted
- Why: Converted the wishlist button to an industry-standard e-commerce design. Restored the solid `var(--cream)` circular background with a clear drop-shadow for high visibility over any photo. Redesigned the heart SVG to use a thick dark outline (`stroke: currentColor`, `fill: none`) by default so it's instantly recognizable as a heart button, and fills with solid red (`var(--error)`) when clicked.
