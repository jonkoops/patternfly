---
id: Card
section: components
cssPrefix: pf-v5-c-card
---

import './Card.css'

## Examples
### Basic
```hbs
{{#> card card--id="card-basic-example"}}
  {{> card-title card-title-text--value="Title"}}
  {{#> card-body}}
    Body
  {{/card-body}}
  {{#> card-footer}}
    Footer
  {{/card-footer}}
{{/card}}
```

### With image and action
```hbs
{{#> card card--id="card-action-example-1"}}
  {{#> card-header}}
    {{#> card-header-main}}
      <img src="/assets/images/pf_logo.svg" width="300px" alt="Logo">
    {{/card-header-main}}
    {{#> card-actions}}
      {{> card--dropdown}}
      {{> card--check}}
    {{/card-actions}}
  {{/card-header}}
  {{> card-title card-title-text--value="Title" card-title-text--id=(concat card--id '-check-label')}}
  {{#> card-body}}
    Body
  {{/card-body}}
  {{#> card-footer}}
    Footer
  {{/card-footer}}
{{/card}}
```

### With title in head
```hbs
{{#> card card--id="card-action-example-2"}}
  {{#> card-header}}
    {{#> card-actions}}
      {{> card--dropdown}}
      {{> card--check}}
    {{/card-actions}}
    {{#> card-header-main}}
      {{> card-title card-title-text--value="This is a really really really really really really really really really really long title" card-title-text--id=(concat card--id '-check-label')}}
    {{/card-header-main}}
  {{/card-header}}
  {{#> card-body}}
    Body
  {{/card-body}}
  {{#> card-footer}}
    Footer
  {{/card-footer}}
{{/card}}
```

### With only actions in head (no title/footer)
```hbs
{{#> card card--id="card-action-example-3"}}
  {{#> card-header}}
    {{#> card-actions}}
      {{> card--dropdown}}
      {{> card--check}}
    {{/card-actions}}
  {{/card-header}}
  {{#> card-body card-body--attribute=(concat 'id="' card--id '-check-label"')}}
    This is the card body. There are only actions in the card head.
  {{/card-body}}
{{/card}}
```

### Actions with no offset
```hbs
{{#> card card--id="card-action-no-offset"}}
  {{#> card-header}}
    {{#> card-actions card-actions--modifier="pf-m-no-offset"}}
      {{#> button button--modifier="pf-m-primary"}}Action{{/button}}
    {{/card-actions}}
    {{#> card-header-main}}
      {{#> title title--modifier="pf-m-2xl" title--attribute=(concat 'id="' card--id '-check-label"')}}This is a card title{{/title}}
    {{/card-header-main}}
  {{/card-header}}
  {{#> card-body}}
    Body
  {{/card-body}}
  {{#> card-footer}}
    Footer
  {{/card-footer}}
{{/card}}
```

### With only image in head
```hbs
{{#> card card--id="card-image-head-example"}}
  {{#> card-header}}
    {{#> card-header-main}}
      <img src="/assets/images/pf_logo.svg" width="300px" alt="Logo">
    {{/card-header-main}}
  {{/card-header}}
  {{> card-title card-title-text--value="Title"}}
  {{#> card-body}}
    Body
  {{/card-body}}
  {{#> card-footer}}
    Footer
  {{/card-footer}}
{{/card}}
```

### With no footer
```hbs
{{#> card card--id="card-no-footer-example"}}
  {{> card-title card-title-text--value="Title"}}
  {{#> card-body}}
    This card has no footer
  {{/card-body}}
{{/card}}
```

### With no title
```hbs
{{#> card card--id="card-no-title-example"}}
  {{#> card-body}}
    This card has no title
  {{/card-body}}
  {{#> card-footer}}
    Footer
  {{/card-footer}}
{{/card}}
```

### With only a content section
```hbs
{{#> card card--id="card-body-example"}}
  {{#> card-body}}
    Body
  {{/card-body}}
{{/card}}
```

### With multiple body sections
```hbs
{{#> card card--id="card-multiple-body-example"}}
  {{> card-title card-title-text--value="Title"}}
  {{#> card-body}}
    Body
  {{/card-body}}
  {{#> card-body}}
    Body
  {{/card-body}}
  {{#> card-body}}
    Body
  {{/card-body}}
  {{#> card-footer}}
    Footer
  {{/card-footer}}
{{/card}}
```

### With only one body that fills
```hbs
{{#> card card--id="card-body-fill-example"}}
  {{> card-title card-title-text--value="Title"}}
  {{#> card-body card-body--modifier="pf-m-no-fill"}}
    Body pf-m-no-fill
  {{/card-body}}
  {{#> card-body card-body--modifier="pf-m-no-fill"}}
    Body pf-m-no-fill
  {{/card-body}}
  {{#> card-body}}
    Body
  {{/card-body}}
  {{#> card-footer}}
    Footer
  {{/card-footer}}
{{/card}}
```

### Compact
```hbs
{{#> card card--id="card-compact-example" card--modifier="pf-m-compact"}}
  {{> card-title card-title-text--value="Title"}}
  {{#> card-body}}
    Body
  {{/card-body}}
  {{#> card-footer}}
    Footer
  {{/card-footer}}
{{/card}}
```

### Large
```hbs
{{#> card card--id="card-display-lg-example" card--modifier="pf-m-display-lg"}}
  {{> card-title card-title-text--value="Title"}}
  {{#> card-body}}
    Body
  {{/card-body}}
  {{#> card-footer}}
    Footer
  {{/card-footer}}
{{/card}}
```

### Selectable
```hbs
{{#> gallery gallery--modifier="pf-m-gutter"}}
{{#> card card--id="card-selectable-example" card--modifier="pf-m-selectable" card--IsSelectable="true"}}
  {{#> card-header}}
    {{#> card-actions card-actions--modifier="pf-m-no-offset"}}
      {{#> card-selectable-actions}}
        {{> card--check}}
      {{/card-selectable-actions}}
    {{/card-actions}}
    {{#> card-header-main}}
      {{> card-title card-title-text--value="Title"}}
    {{/card-header-main}}
  {{/card-header}}
  {{#> card-body}}
    Body
  {{/card-body}}
  {{#> card-footer}}
    Footer
  {{/card-footer}}
{{/card}}

{{#> card card--id="card-selectable-example-disabled" card--modifier="pf-m-selectable pf-m-disabled" card--IsSelectable="true"}}
  {{#> card-header}}
    {{#> card-actions card-actions--modifier="pf-m-no-offset"}}
      {{#> card-selectable-actions}}
        {{> card--check check--IsDisabled=true}}
      {{/card-selectable-actions}}
    {{/card-actions}}
    {{#> card-header-main}}
      {{> card-title card-title-text--value="Disabled card" card-title--attribute=(concat 'id="' card--id '-title"')}}
    {{/card-header-main}}
  {{/card-header}}
  {{#> card-body}}
    Body
  {{/card-body}}
  {{#> card-footer}}
    Footer
  {{/card-footer}}
{{/card}}

{{#> card card--id="card-selectable-example-selected-disabled" card--modifier="pf-m-selectable pf-m-selected pf-m-disabled" card--IsSelectable="true"}}
  {{#> card-header}}
    {{#> card-actions card-actions--modifier="pf-m-no-offset"}}
      {{#> card-selectable-actions}}
        {{> card--check check-input--IsChecked=true check--IsDisabled=true}}
      {{/card-selectable-actions}}
    {{/card-actions}}
    {{#> card-header-main}}
      {{> card-title card-title-text--value="Selected but disabled card" card-title--attribute=(concat 'id="' card--id '-title"')}}
    {{/card-header-main}}
  {{/card-header}}
  {{#> card-body}}
    Body
  {{/card-body}}
  {{#> card-footer}}
    Footer
  {{/card-footer}}
{{/card}}

{{/gallery}}
```

### Single selectable
```hbs
{{#> gallery gallery--modifier="pf-m-gutter"}}

{{#> card card--id="card-single-selectable-example" card--modifier="pf-m-selectable" card--IsSelectable="true"}}
  {{#> card-header}}
    {{#> card-actions card-actions--modifier="pf-m-no-offset"}}
      {{#> card-selectable-actions}}
        {{> card--radio}}
      {{/card-selectable-actions}}
    {{/card-actions}}
    {{#> card-header-main}}
      {{> card-title card-title-text--value="Title" card-title--attribute=(concat 'id="' card--id '-title"')}}
    {{/card-header-main}}
  {{/card-header}}
  {{#> card-body}}
    Body
  {{/card-body}}
  {{#> card-footer}}
    Footer
  {{/card-footer}}
{{/card}}

{{#> card card--id="card-single-selectable-example-disabled" card--modifier="pf-m-selectable pf-m-disabled" card--IsSelectable="true"}}
  {{#> card-header}}
    {{#> card-actions card-actions--modifier="pf-m-no-offset"}}
      {{#> card-selectable-actions}}
        {{> card--radio card--radio--IsDisabled="disabled"}}
      {{/card-selectable-actions}}
    {{/card-actions}}
    {{#> card-header-main}}
      {{> card-title card-title-text--value="Disabled card" card-title--attribute=(concat 'id="' card--id '-title"')}}
    {{/card-header-main}}
  {{/card-header}}
  {{#> card-body}}
    Body
  {{/card-body}}
  {{#> card-footer}}
    Footer
  {{/card-footer}}
{{/card}}

{{#> card card--id="card-single-selectable-example-selected-disabled" card--modifier="pf-m-selectable pf-m-selected pf-m-disabled" card--IsSelectable="true"}}
  {{#> card-header}}
    {{#> card-actions card-actions--modifier="pf-m-no-offset"}}
      {{#> card-selectable-actions}}
        {{> card--radio card--radio--IsChecked="checked" card--radio--IsDisabled="disabled"}}
      {{/card-selectable-actions}}
    {{/card-actions}}
    {{#> card-header-main}}
      {{> card-title card-title-text--value="Selected but disabled card" card-title--attribute=(concat 'id="' card--id '-title"')}}
    {{/card-header-main}}
  {{/card-header}}
  {{#> card-body}}
    Body
  {{/card-body}}
  {{#> card-footer}}
    Footer
  {{/card-footer}}
{{/card}}

{{/gallery}}
```

### Clickable
```hbs
{{#> gallery gallery--modifier="pf-m-gutter"}}
{{#> card card--id="card-clickable-example" card--modifier="pf-m-clickable" card--IsClickable="true"}}
  {{#> card-header}}
    {{#> card-actions card-actions--modifier="pf-m-no-offset"}}
      {{#> card-selectable-actions}}
        {{> card--hidden-input}}
      {{/card-selectable-actions}}
    {{/card-actions}}
    {{#> card-header-main}}
      {{> card-title card-title-text--value="Title" card-title--attribute=(concat 'id="' card--id '-title"')}}
    {{/card-header-main}}
  {{/card-header}}
  {{#> card-body}}
    Body
  {{/card-body}}
  {{#> card-footer}}
    Footer
  {{/card-footer}}
{{/card}}

{{#> card card--id="card-clickable-example-disabled" card--modifier="pf-m-clickable pf-m-disabled" card--IsClickable="true"}}
  {{#> card-header}}
    {{#> card-actions card-actions--modifier="pf-m-no-offset"}}
      {{#> card-selectable-actions}}
        {{> card--hidden-input card--hidden-input--IsDisabled="disabled "}}
      {{/card-selectable-actions}}
    {{/card-actions}}
    {{#> card-header-main}}
      {{> card-title card-title-text--value="Disabled card" card-title--attribute=(concat 'id="' card--id '-title"')}}
    {{/card-header-main}}
  {{/card-header}}
  {{#> card-body}}
    Body
  {{/card-body}}
  {{#> card-footer}}
    Footer
  {{/card-footer}}
{{/card}}

{{#> card card--id="card-clickable-example-selected-disabled" card--modifier="pf-m-clickable pf-m-selected pf-m-disabled" card--IsClickable="true"}}
  {{#> card-header}}
    {{#> card-actions card-actions--modifier="pf-m-no-offset"}}
      {{#> card-selectable-actions}}
        {{> card--hidden-input card--hidden-input--IsDisabled="disabled "}}
      {{/card-selectable-actions}}
    {{/card-actions}}
    {{#> card-header-main}}
      {{> card-title card-title-text--value="Selected but disabled card" card-title--attribute=(concat 'id="' card--id '-title"')}}
    {{/card-header-main}}
  {{/card-header}}
  {{#> card-body}}
    Body
  {{/card-body}}
  {{#> card-footer}}
    Footer
  {{/card-footer}}
{{/card}}

{{/gallery}}
```

### Clickable and selectable
```hbs
{{#> gallery gallery--modifier="pf-m-gutter"}}

{{#> card card--id="card-clickable-selectable-example" card--modifier="pf-m-clickable pf-m-selectable" card--IsSelectable="true"}}
  {{#> card-header}}
    {{#> card-actions card-actions--modifier="pf-m-no-offset"}}
      {{#> card-selectable-actions}}
        {{> card--check}}
      {{/card-selectable-actions}}
    {{/card-actions}}
    {{#> card-header-main}}
      {{#> card-title card-title--attribute=(concat 'id="' card--id '-title"')}}
        {{#> button button--modifier="pf-m-link pf-m-inline"}}Title{{/button}}
      {{/card-title}}
    {{/card-header-main}}
  {{/card-header}}
  {{#> card-body}}
    Body
  {{/card-body}}
  {{#> card-footer}}
    Footer
  {{/card-footer}}
{{/card}}

{{#> card card--id="card-clickable-selectable-current-example" card--modifier="pf-m-clickable pf-m-selectable pf-m-current" card--IsSelectable="true"}}
  {{#> card-header}}
    {{#> card-actions card-actions--modifier="pf-m-no-offset"}}
      {{#> card-selectable-actions}}
        {{> card--check}}
      {{/card-selectable-actions}}
    {{/card-actions}}
    {{#> card-header-main}}
      {{#> card-title card-title--attribute=(concat 'id="' card--id '-title"')}}
        {{#> button button--modifier="pf-m-link pf-m-inline"}}Current card (clicked){{/button}}
      {{/card-title}}
    {{/card-header-main}}
  {{/card-header}}
  {{#> card-body}}
    Body
  {{/card-body}}
  {{#> card-footer}}
    Footer
  {{/card-footer}}
{{/card}}

{{#> card card--id="card-clickable-selectable-example-disabled" card--modifier="pf-m-clickable pf-m-selectable pf-m-disabled" card--IsSelectable="true"}}
  {{#> card-header}}
    {{#> card-actions card-actions--modifier="pf-m-no-offset"}}
      {{#> card-selectable-actions}}
        {{> card--check check--IsDisabled=true}}
      {{/card-selectable-actions}}
    {{/card-actions}}
    {{#> card-header-main}}
      {{#> card-title card-title--attribute=(concat 'id="' card--id '-title"')}}
        {{#> button button--modifier="pf-m-link pf-m-inline pf-m-disabled" button--IsDisabled="true"}}Disabled card{{/button}}
      {{/card-title}}
    {{/card-header-main}}
  {{/card-header}}
  {{#> card-body}}
    Body
  {{/card-body}}
  {{#> card-footer}}
    Footer
  {{/card-footer}}
{{/card}}

{{#> card card--id="card-clickable-selectable-example-selected-disabled" card--modifier="pf-m-clickable pf-m-selectable pf-m-selected pf-m-disabled" card--IsSelectable="true"}}
  {{#> card-header}}
    {{#> card-actions card-actions--modifier="pf-m-no-offset"}}
      {{#> card-selectable-actions}}
        {{> card--check check-input--IsChecked=true check--IsDisabled=true}}
      {{/card-selectable-actions}}
    {{/card-actions}}
    {{#> card-header-main}}
      {{#> card-title card-title--attribute=(concat 'id="' card--id '-title"')}}
        {{#> button button--modifier="pf-m-link pf-m-inline pf-m-disabled" button--IsDisabled="true"}}Selected but disabled card{{/button}}
      {{/card-title}}
    {{/card-header-main}}
  {{/card-header}}
  {{#> card-body}}
    Body
  {{/card-body}}
  {{#> card-footer}}
    Footer
  {{/card-footer}}
{{/card}}

{{/gallery}}
```

### Hoverable raised
```hbs isDeprecated
{{#> card card--id="card-hoverable-example" card--modifier="pf-m-hoverable-raised"}}
  {{> card-title card-title-text--value="Title"}}
  {{#> card-body}}
    Body
  {{/card-body}}
  {{#> card-footer}}
    Footer
  {{/card-footer}}
{{/card}}
```

### Selectable raised
```hbs isDeprecated
{{#> card card--id="card-selectable-raised-example" card--modifier="pf-m-selectable-raised" card--attribute='tabindex="0"'}}
  {{> card-title card-title-text--value="Title"}}
  {{#> card-body}}
    Body
  {{/card-body}}
  {{#> card-footer}}
    Footer
  {{/card-footer}}
{{/card}}
```

### Selected raised
```hbs isDeprecated
{{#> card card--id="card-selected-raised-example" card--modifier="pf-m-selectable-raised pf-m-selected-raised" card--attribute='tabindex="0"'}}
  {{> card-title card-title-text--value="Title"}}
  {{#> card-body}}
    Body
  {{/card-body}}
  {{#> card-footer}}
    Footer
  {{/card-footer}}
{{/card}}
```

### Selectable raised with a hidden input for improved screen reader accessibility
```hbs isDeprecated
{{> card-sr-input card-sr-input--attribute="aria-label='Checkbox to improve screen reader accessibility of a selectable card'"}}
{{#> card card--id="card-selectable-raised-with-input-example" card--modifier="pf-m-selectable-raised" card--attribute='tabindex="0"'}}
  {{> card-title card-title-text--value="Title"}}
  {{#> card-body}}
    Body
  {{/card-body}}
  {{#> card-footer}}
    Footer
  {{/card-footer}}
{{/card}}
```

### Non selectable raised
```hbs isDeprecated
{{#> card card--id="card-non-selectable-raised-example" card--modifier="pf-m-non-selectable-raised"}}
  {{> card-title card-title-text--value="Title"}}
  {{#> card-body}}
    Body
  {{/card-body}}
  {{#> card-footer}}
    Footer
  {{/card-footer}}
{{/card}}
```

### Flat
```hbs
{{#> card card--id="card-flat-example" card--modifier="pf-m-flat"}}
  {{> card-title card-title-text--value="Title"}}
  {{#> card-body}}
    Body
  {{/card-body}}
  {{#> card-footer}}
    Footer
  {{/card-footer}}
{{/card}}
```

### Rounded
```hbs
{{#> card card--id="card-rounded-example" card--modifier="pf-m-rounded"}}
  {{> card-title card-title-text--value="Title"}}
  {{#> card-body}}
    Body
  {{/card-body}}
  {{#> card-footer}}
    Footer
  {{/card-footer}}
{{/card}}
```

### Plain
```hbs
{{#> card card--id="card-plain-example" card--modifier="pf-m-plain"}}
  {{> card-title card-title-text--value="Title"}}
  {{#> card-body}}
    Body
  {{/card-body}}
  {{#> card-footer}}
    Footer
  {{/card-footer}}
{{/card}}
```

### Expandable
```hbs
{{#> card card--id="card-expandable-example"}}
  {{#> card-header}}
    {{> card-header-toggle}}
    {{#> card-actions}}
      {{> card--dropdown}}
      {{> card--check}}
    {{/card-actions}}
    {{#> card-header-main}}
      {{> card-title card-title-text--value="Title" card-title-text--id=(concat card--id '-title')}}
    {{/card-header-main}}
  {{/card-header}}
{{/card}}
```

### Expandable with image
```hbs
{{#> card card--id="card-expandable-image-example"}}
  {{#> card-header}}
    {{> card-header-toggle}}
    {{#> card-header-main}}
      <img src="/assets/images/pf-logo-small.svg" alt="PatternFly logo" width="27px">
    {{/card-header-main}}
    {{#> card-actions}}
      {{> card--dropdown}}
      {{> card--check}}
    {{/card-actions}}
  {{/card-header}}
{{/card}}
```

### Expanded
```hbs
{{#> card card--id="card-expanded-example" card--modifier="pf-m-expanded"}}
  {{#> card-header}}
    {{> card-header-toggle}}
    {{#> card-actions}}
      {{> card--dropdown}}
      {{> card--check}}
    {{/card-actions}}
    {{#> card-header-main}}
      {{> card-title-text card-title-text--value="Title" card-title-text--id=(concat card--id '-title')}}
    {{/card-header-main}}
  {{/card-header}}
  {{#> card-expandable-content}}
    {{#> card-body}}
      Body
    {{/card-body}}
    {{#> card-footer}}
      Footer
    {{/card-footer}}
  {{/card-expandable-content}}
{{/card}}
```

### Full height card
```hbs
{{#> card card--id="card-full-height-example" card--modifier="pf-m-full-height"}}
  {{#> card-header}}
    {{#> card-actions}}
      {{> card--dropdown}}
      {{> card--check}}
    {{/card-actions}}
    {{#> card-header-main}}
      {{> card-title card-title-text--value="Title" card-title-text--id=(concat card--id '-title"')}}
    {{/card-header-main}}
  {{/card-header}}
  {{#> card-body}}
    Body
  {{/card-body}}
  {{#> card-footer}}
    Footer
  {{/card-footer}}
{{/card}}
```

### Expandable toggle on right
```hbs
{{#> card card--id="card-toggle-on-right-example"}}
  {{#> card-header card-header--modifier="pf-m-toggle-right"}}
    {{#> card-actions}}
      {{> card--dropdown}}
      {{> card--check}}
    {{/card-actions}}
    {{#> card-header-main}}
      {{> card-title card-title-text--value="Title" card-title-text--id=(concat card--id '-title')}}
    {{/card-header-main}}
    {{> card-header-toggle}}
  {{/card-header}}
{{/card}}
```

### Card with dividers between sections
```hbs
{{#> card}}
  {{> card-title card-title-text--value="Title"}}
  {{> divider}}
  {{#> card-body}}
    Body
  {{/card-body}}
  {{> divider}}
  {{#> card-body}}
    Body
  {{/card-body}}
  {{> divider}}
  {{#> card-footer}}
    Footer
  {{/card-footer}}
{{/card}}
```

## Documentation
### Overview
A card is a generic rectangular container that can be used to build other components. Use a default card for regular page content and the compact variation for dashboard or small cards.

### Usage
| Class | Applied | Outcome |
| ---- | ---- | ---- |
| `.pf-v5-c-card` | `<div>` | Creates a card component.  **Required** |
| `.pf-v5-c-card__title` | `<div>` | Creates a card title container. |
| `.pf-v5-c-card__title-text` | `<h1>`, `<h2>`, `<h3>`, `<h4>`, `<h5>`, `<h6>`, `<div>` | Creates a card title text element. |
| `.pf-v5-c-card__body` | `<div>` | Creates the body of a card. By default, the body element fills the available space in the card. You can use multiple `.pf-v5-c-card__body` elements. |
| `.pf-v5-c-card__footer` | `<div>` | Creates the footer of a card. |
| `.pf-v5-c-card__header` | `<div>` | Creates the header of the card where images, actions, and/or the card title can go. |
| `.pf-v5-c-card__header-toggle` | `<div>` | Creates the expandable card toggle. |
| `.pf-v5-c-card__header-toggle-icon` | `<span>` | Creates the expandable card toggle icon. |
| `.pf-v5-c-card__actions` | `<div>` | Creates an actions element to be used in the card header. |
| `.pf-v5-c-card__selectable-actions` | `<div>` | Creates an element to hold a checkbox or radio and the related label used to make a card selectable or clickable. |
| `.pf-v5-c-card__header-main` | `<div>` | Creates a wrapper element to be used in the card header when using an image, logo, or text. **Required if `.pf-v5-c-card__header` has content outside of a card header toggle or card header actions** |
| `.pf-v5-c-card__expandable-content` | `<div>` | Creates the expandable card's expandable content. |
| `.pf-v5-c-card__sr-input` | `<input>` | Creates an input which, when focused, makes a following `.pf-v5-c-card` appear focused. |
| `.pf-m-compact` | `.pf-v5-c-card` | Creates a compact variation of the card component that involves smaller font sizes and spacing. This variation is for use on dashboards and where a smaller card is preferred. |
| `.pf-m-display-lg` | `.pf-v5-c-card` | Creates a large variation of the card component that involves larger font sizes and spacing. This variation is for marketing use cases. |
| `.pf-m-no-fill` | `.pf-v5-c-card__body` | Sets a `.pf-v5-c-card__body` not to fill the available space in `.pf-v5-c-card`. `.pf-m-no-fill` can be added to multiple card bodies. |
| `.pf-m-selectable` | `.pf-v5-c-card` | Modifies a card to be selectable.  |
| `.pf-m-clickable` | `.pf-v5-c-card` | Modifies a card to be clickable. |
| `.pf-m-selected` | `.pf-v5-c-card` | Modifies a selectable card for selected state styling. Can be used in addition to indicating selection via the `.pf-v5-c-card__input`. |
| `.pf-m-current` | `.pf-v5-c-card` | Modifies a card that is both clickable and selectable for clicked state styling. |
| `.pf-m-disabled` | `.pf-v5-c-card` | Modifies a card so it is not selectable or clickable.  |
| `.pf-m-hoverable-raised` | `.pf-v5-c-card` | Modifies the card to include hover styles on `:hover`. |
| `.pf-m-selectable-raised` | `.pf-v5-c-card` | Modifies a selectable card so that it is selectable. |
| `.pf-m-selected-raised` | `.pf-v5-c-card.pf-m-selectable-raised` | Modifies a selectable card for the selected state. |
| `.pf-m-non-selectable-raised` | `.pf-v5-c-card` | Modifies a selectable card so that it is not selectable. |
| `.pf-m-flat` | `.pf-v5-c-card` | Modifies the card to have a border instead of a shadow. `.pf-m-flat` is for use in layouts where cards are against a white background. |
| `.pf-m-rounded` | `.pf-v5-c-card` | Modifies the card to have rounded corners. |
| `.pf-m-plain` | `.pf-v5-c-card` | Modifies the card to have no box shadow and no background color. |
| `.pf-m-expanded` | `.pf-v5-c-card` | Modifies the card for the expanded state. |
| `.pf-m-toggle-right` | `.pf-v5-c-card__header` | Modifies the expandable card header toggle to be positioned at flex-end. |
| `.pf-m-full-height` | `.pf-v5-c-card` | Modifies the card to full height of its parent. |
| `.pf-m-no-offset` | `.pf-v5-c-card__actions` | Removes the negative vertical margins on the actions element intended to align the action content with the card title. |
