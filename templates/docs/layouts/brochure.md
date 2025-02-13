---
wrapper_template: '_layouts/docs.html'
context:
  title: Brochure site | Layouts
---

<div class="p-strip">
  <div class="row">
    <div class="col-9 col-start-large-4">
      <h1 class="p-heading--2 u-no-margin--bottom">
        <strong>
          Brochure site layouts
        </strong>
      </h1>
      <p class="p-heading--2">
        The rules we use when designing<br class="u-hide--small"> and building pages with Vanilla
      </p>
      <div class="p-strip u-no-padding--bottom">
        <p class="u-no-margin--bottom">
          A page is a sequence of sections sandwiched between a header and a footer. To create a successful page, we need to get 3 things right:
        <p>
        <ul class="p-list--divided" style="max-width: 40rem">{# TODO: replace with max-width utility when implemented #}
          <li class="p-list__item has-bullet">choose section layouts that present content effectively,</li>
          <li class="p-list__item has-bullet">prevent adjacent sections from competing for attention,</li>
          <li class="p-list__item has-bullet">ensure the choices above, which are made individually per section, resulting in a coherent, well-paced page.</li>
        </ul>
      </div>
    </div>
  </div>
</div>

<div class="p-strip u-no-padding--top">
  <hr class="is-fixed-width">
  <div class="row">
    <div class="col-9 col-start-large-4">
      <h2>
          Layouts
      </h2>
      <div class="p-strip u-no-padding--bottom">
        <p>
          Layouts are controlled by a responsive grid that has 4, 6 or 12 columns depending on the browser window width.
          Having 12 columns is necessary in order to create versatile layouts, however, it provides far too many choices - few of which work well in a sequence of sections.
        </p>
        <p>
          To illustrate the problem, consider the following example. Place a 5 + 7 column layout followed by a 3 + 3 + 3 column layout with placeholder content. You should get something like the image below. The problem is, containers on the far right are staggered by one column, which looks like an unintentional misalignment:
        </p>
          {{ image (
            url="https://assets.ubuntu.com/v1/7a25ffa4-vanilla-stagered-grid-example.png",
            alt="",
            width="2244",
            height="672",
            hi_def=True,
            loading="auto|lazy"
            ) | safe
          }}
          <p>This happens every time containers with large blocks of copy in adjacent rows differ by one column - e.g. 5 followed by 6, 7 followed by 8, etc.</p>
      </div>
    </div>
  </div>
</div>

<div class="p-strip u-no-padding--top">
  <hr class="is-fixed-width">
  <div class="row">
    <div class="col-3">
      <h3 class="p-muted-heading">The 25% rule</h3>
    </div>
    <div class="col-9">
      <p>To remedy the “off by one column” problem, we use a system inspired by an oct-tree: Widths are multiples of 25% of the available space. This simple rule decimates the available choices, which has the following beneficial effects on our layouts:</p>
      <ul class="p-list--divided" style="max-width: 40rem">{# TODO: replace with max-width utility when implemented #}
        <li class="p-list__item has-bullet">creates up to 4 invisible "fault lines" (at 0%, 25%, 50%, 75%, or at the start of the first, fourth, sixth and ninth column), to one of which all content, across all sections, aligns</li>
        <li class="p-list__item has-bullet">facilitates scanning/skimming, enabling the reader to quickly navigate by headings for example </li>
        <li class="p-list__item has-bullet">induces a strong sense of internal coherence, order and consistency</li>
        <li class="p-list__item has-bullet">provides enough room for variation to avoid monotony:</li>
      </ul>
      {{ image (
        url="https://assets.ubuntu.com/v1/7bc80c1d-vanilla-example-25-layout.png",
        alt="",
        width="1258",
        height="1406",
        hi_def=True,
        loading="auto|lazy"
        ) | safe
      }}
    </div>
  </div>
</div>

<hr class="is-fixed-width">

<div class="p-strip u-no-padding--top">
  <div class="row">
    <div class="col-3">
      <h3 class="p-muted-heading">Further considerations</h3>
    </div>
    <div class="col-9">
      <p>Before we look at examples, let's highlight a couple of considerations used in conjunction with the 25% rule:</p>
      <ul class="p-list--divided" style="max-width: 40rem">{# TODO: replace with max-width utility when implemented #}
        <li class="p-list__item has-bullet">Place larger blocks on the right-hand side of smaller blocks.  For example, if a heading is longer than the accompanying text, it would work better directly above it, rather than to the left of the text.</li>
        <li class="p-list__item has-bullet">Do not allow the quest for consistency to lead to monotony. Be mindful of pacing, and aim to create a rhythm of contrasts (large vs small, white space vs dense copy, etc ). This helps keep the page interesting and engaging.</li>
      </ul>
    </div>
  </div>
</div>

<hr class="is-fixed-width">

<div class="p-strip u-no-padding--top">
  <div class="row">
    <div class="col-3">
      <h3 class="p-muted-heading">Example layouts<br class="u-hide--small"> built on the 25% system</h3>
    </div>
    <div class="col-9">
      <h2>
          The 50/50 split
      </h2>
      <p>The 50/50 split is a very versatile layout. It places a short scannable part of the content (usually a heading) on the left-hand side. The rest of the content goes into the right-hand side. A few of the benefits of this layout:</p>
      <ul class="p-list--divided" style="max-width: 40rem">{# TODO: replace with max-width utility when implemented #}
        <li class="p-list__item has-bullet">provides enough width for large headings (e.g. an h2) and long paragraphs;</li>
        <li class="p-list__item has-bullet">makes it easy to scan by headings;</li>
<li class="p-list__item has-bullet">
it is very compact - as the headings do not push the body text down.</li>
      </ul>
      <p>This layout is designed with two things in mind: the average time visitors spend on a brochure page (between 20sec - 1:35min), and the long length of our pages.</p>
      <p>For example, if you only give us 20sec of your time on a page that takes 5min to read top to bottom, our best chance of directing you to the part of the page you are interested in is to let you scan by headings - which you can do on most pages in under 20 sec. Then, only when you’ve found the part you came for, you move over to the right,  read the dense copy and hopefully click on a CTA.</p>
      {{ image (
        url="https://assets.ubuntu.com/v1/14e55e1e-vanilla-example-50-50-split.png",
        alt="",
        width="4182",
        height="2012",
        hi_def=True,
        loading="auto|lazy"
        ) | safe
      }}
      <p><a href="/docs/examples/layouts/brochure-site/50-50-split">View the example 50/50 split layout in the browser</a></p>
    </div>
  </div>
  <div class="embedded-example"><a href="/docs/examples/layouts/brochure-site/50-50-split-structure" class="js-example">View an example of 50/50 split</a></div>
</div>

<div class="p-strip u-no-padding--top">
  <div class="row">
    <div class="col-9 col-start-large-4">
      <hr>
      <h2>
          The 25/25/50 split
      </h2>
      <p>A variation of the 50/50 split, we subdivide one of the halves further to obtain a 25/25/50 layout.</p>
      {{ image (
        url="https://assets.ubuntu.com/v1/7b5a73f0-vanilla-example-25-25-50-split.png",
        alt="",
        width="3300",
        height="1345",
        hi_def=True,
        loading="auto|lazy"
        ) | safe
      }}
      <p><a href="/docs/examples/layouts/brochure-site/25-25-50-split">View the example 25/25/50 split layout in the browser</a></p>
    </div>
  </div>
  <div class="embedded-example"><a href="/docs/examples/layouts/brochure-site/25-25-50-split-structure" class="js-example">View an example of 25/25/50 split</a></div>
</div>

<div class="p-strip u-no-padding--top">
  <div class="row">
    <div class="col-9 col-start-large-4">
      <hr>
      <h2>
          The 25/75 split
      </h2>
      <p>The 25/75 split reserves 3 columns for small headings (or just “structural” white space) and a larger, 9-column area that can be used for long copy - or further subdivided into multiples of 25%.
      </p>
      <p>The simplest case: wayfinding heading + long h2 heading and some content:</p>
      {{ image (
        url="https://assets.ubuntu.com/v1/edd053ae-vanilla-example-25-75-split.png",
        alt="",
        width="1646",
        height="503",
        hi_def=True,
        loading="auto|lazy"
        ) | safe
      }}
      <p><a href="/docs/examples/layouts/brochure-site/25-75-split">View the example 25/75 split layout in the browser</a></p>
    </div>
  </div>
  <div class="embedded-example"><a href="/docs/examples/layouts/brochure-site/25-75-split-structure" class="js-example">View an example of 25/75 split</a></div>
</div>

<div class="p-notification--caution">
  <div class="p-notification__content">
    <h5 class="p-notification__title">Work in progress</h5>
    <p class="p-notification__message">Please note that this documentation is still a work in progress. If you have any suggestions on how to improve it feel free to <a href="https://github.com/canonical/vanilla-framework/issues/new">open an issue</a>.</p>
  </div>
</div>
