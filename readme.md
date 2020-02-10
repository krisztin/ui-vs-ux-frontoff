# Frontloops Challenge

[Frontloops](https://frontloops.io) is a front-end challenge site by Dimitry Belyaev, a Sr. FE Dev at Booking.com. As part of the challenge you get an image/video file of the final design then off you code.

I've decided to hone my FE skills a bit whilst also **practicing some UX Design by also tweaking the designs** if and when needed.

## Markup challenges
To improve HTML and CSS skills.

### Day 1 - Plan Picker

The original design:

![original design - plan picker](1-plan_picker/design/l1s1.png)

My design:

![my design - plan picker](1-plan_picker/design/l1s1m.png)

🤖 [The code](1-plan_picker/)

🧐 <a href="https://krisztin.github.io/ui-vs-ux-frontoff/1-plan_picker/" target="_blank" rel="noopener noreferrer">See it in action</a>

#### UX redesign

- changed uppercase text to normal for readability
- added an h1 to explain the selection
- slightly larger text (suggested base font-size was 14px 🔬 which is waaaay too tiny)
- more contrasting font colour for the description


### Day 2 - Payment method picker

The original design:

![original design - payment method picker](2-payment_method/design/l1s2.png)

My design:

![my design - payment method picker](2-payment_method/design/l1s2m.png)

🤖 [The code](2-payment_method/)

🧐 <a href="https://krisztin.github.io/ui-vs-ux-frontoff/2-payment_method/" target="_blank" rel="noopener noreferrer">See it in action</a>

#### UX redesign

- unchecked inputs' labels are still black; design suggested grey but that could potentially confuse users thinking the option is disabled
- made the container narrower so the checkmark is closer to the label instead of miles away on the right
- design called for all text to be uppercase which is hell on readability
- checked label gets physically larger to give better feedback on it being selected

### Day 3 - Order thank you page

The original design:

![original design - thank you page](3-order_thanks/design/l1s3.png)

My design:

![my design - thank you page](3-order_thanks/design/l1s3m.png)

🤖 [The code](3-order_thanks/)

🧐 <a href="https://krisztin.github.io/ui-vs-ux-frontoff/3-order_thanks/" target="_blank" rel="noopener noreferrer">See it in action</a>

#### UX redesign

Information enrichment:

- **'my account' label** for the account icon, because icon+label is superior to icon or label only.
- **Thank you heading text** for the skimmers as a quick feedback that all is well.
- **Headers for the order summary** 'table' (i.e. Product name, Quantitiy).
- Quantity column... 🙄
- **Individual price** displayed under the product's name.
- A **CTA to get in touch**, just in case something went wrong or the user has a question about the order.

Wanted to add:
- Thumbnail image of the product

Layout/accessibility:
- **Moved the background image bicycle** so it doesn't overlap with the order details. It's positioned that it also never interferes with the `contact` section.
- **Didn't use a table** for the summary due to accessibility concerns (not just the lack of a consistent way to be read by screen readers but how unpredictable tables are when it comes to sizing on smaller screens).
- Each order item also has an **accessibility text paragraph that collates all the information** in the table/line into one single, uninterrupted paragraph.

```html

<!-- This garble below is hidden for screen readers to avoid confusion -->
<div class="row" aria-hidden="true">
  <p class="col-6">
    <span class="product-name">Castelli Arenberg Gel Gloves</span>
    <span class="product-price">£39</span>
  </p>
  <p class="align--centre col-2">1</p>
  <p class="align--right col-2">£39</p>
</div>

<!-- Instead, screen readers will read this line -->
<p class="a11ytxt">1, Castelli Arenberg Gel Gloves, £39</p>

```

