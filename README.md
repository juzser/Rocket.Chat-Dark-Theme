# Rocket.Chat dark mode

Dark mode toggle for Rocket.Chat. This is compatible with the latest version of Rocket.Chat.
Please star this repo if you like it.

### Customizable

You can customize the colors by change the `:root` & `:root .dark-mode` css variables in custom css field.
I also customized the sidebar a bit, you can change the sidebar width by changing the `--sidebar-width` variable.

Have fun!

<img width="227" alt="Screenshot 2023-01-10 at 10 28 16" src="https://user-images.githubusercontent.com/5735071/211455601-1f7bee07-9d30-46db-ab48-692ff81bfc71.png">


## Installation

Go to Admin > Settings > Layout.
Then add the following code to the fields:

1. Custom CSS:

```css
:root {
  --primary-font-color: #222;
  --info-font-color: #737373;
  --var-yahoo-width: 40px;
  --mention-link-text-color: #164faf;
  --mention-link-background: #ddecff;
  --mention-link-group-text-color: #3c3c3c;
  --mention-link-group-background: #f9e661;
  --rcx-tooltip-text-color: #fff;
  --sidebar-width: 230px;
  --tags-color: #b45817;
  --tags-border-color: #d3d3d3;
}

/**
 * ==== DARK MODE variables ====
 */
:root .dark-mode {
  --dark-background: #242629;
  --dark-background-secondary: #333;
  --dark-background-hover: #16171a;
  --dark-color: #fff;
  --dark-color-neutral: #8a8a8a;
  --rcx-color-neutral-100: #303236;
  --rcx-color-neutral-400: #434343;
  --rcx-color-neutral-500: #4e5052;
  --rcx-color-neutral-600: #898c8f;
  --rcx-color-neutral-700: #a9adbe;
  --dark-color-secondary: #c4c8ce;
  --dark-color-icon-neutral: #b2b2b2;
  --dark-border-color-dim: #41474c;
  --dark-color-danger: #ee7663;
  --tags-color: #ff984f;
  --tags-background-color: #313538;
  --tags-border-color: #46474a;
  --message-header-name-color: #c2c7cf;
  --icon-background-color: #2f3b46;
  --sidebar-background-color: #292b2f;

  --mention-link-text-color: var(--color-light-blue);
  --mention-link-background: var(--color-dark-medium);

  /* Overwritten */
  --secondary-background-color: var(--dark-background-secondary);
  --rcx-color-surface-tint: var(--dark-background);
  --primary-font-color: var(--dark-color);
  --info-font-color: var(--dark-color-secondary);
  --rcx-color-font-hint: #828a9a;
  --rcx-color-primary-500: #5698f8;
  --rcx-button-primary-background-color: #156ff5;
  --rcx-button-primary-border-color: #156ff5;
  --input-icon-color: var(--dark-color-neutral);
  --rcx-input-colors-focus-shadow-color: #3c3c3c;
  --rcx-color-surface-light: var(--dark-background);
  --rcx-color-font-default: var(--dark-color);
  --rcx-color-font-danger: var(--dark-color-danger);
  --rcx-color-stroke-extra-light: var(--dark-border-color-dim);
  --rcx-button-icon-color: var(--dark-color-icon-neutral);
  --rcx-option-color-variant-danger: var(--dark-color-danger);
  --rcx-color-danger-700: var(--dark-color-danger);
  --rcx-color-font-secondary-info: #84888d;
  --rcx-color-button-background-primary-hover: #4b8ef1;
  --rcx-color-stroke-highlight: #2d71d5;
  --rcx-color-primary-600: #5393f1;
  --rc-color-button-primary: #4f91f3;
  --rcx-button-secondary-background-color: #eceff2;
  --rcx-button-secondary-border-color: #eceff2;
  --rcx-button-secondary-hover-background-color: #d3e9ff;
  --rcx-button-secondary-hover-border-color: #d3e9ff;
  --rcx-button-danger-background-color: #f0203b;
  --rcx-button-danger-border-color: #f0203b;
  --rcx-color-status-background-warning-2: #42413e;
  --rcx-message-background-color-editing: #373a40;

  /* Message Box */
  --message-box-color: var(--dark-color);
  --message-box-markdown-hover-color: var(--dark-color);
  --rcx-message-background-color: var(--dark-background);
  --rcx-message-background-color-focus: #202123;
  --rcx-color-surface-hover: #282b33;
  --rcx-button-icon-hover-background-color: var(--dark-background-hover);
  --rcx-button-icon-hover-border-color: var(--dark-background-hover);
  --rcx-message-divider-color: var(--dark-color-neutral);
  --rcx-message-divider-background-color: var(--dark-border-color-dim);
  --message-box-container-border-color: var(--dark-border-color-dim);
  --rcx-button-icon-background-color: var(--rcx-color-surface-light);
  --message-box-user-activity-user-color: var(--rcx-color-neutral-700);
  --rcx-message-reaction-background-color: var(--rcx-color-surface-light);
  --rcx-message-reaction-color: var(--color-light-blue);
  --rcx-message-reaction-border-color: var(--rcx-color-neutral-700);
  --rcx-color-font-annotation: var(--rcx-color-neutral-600);

  /* Threads */
  --content-background-color: var(--dark-background);
  --component-color: var(--dark-border-color-dim);
  --color-darkest: var(--rcx-button-icon-color);
  --popover-background: var(--dark-background-hover);
  --popover-item-color: var(--dark-color);

  /* User preferences */
  --color-gray-lightest: var(--dark-background);
  --flex-nav-background: var(--dark-background);
  --sidebar-background-light-active: var(--dark-background-hover);
  --sidebar-background-light-hover: var(--dark-background-hover);
  --rcx-tag-colors-default-background-color: var(--dark-color);
  --rcx-tag-colors-secondary-background-color: #e4e7ea;

  /* Common inputs */
  --input-border-color: var(--dark-border-color-dim);
  --info-font-color: var(--dark-color-neutral);
  --input-text-color: var(--dark-color);
  --primary-background-color: var(--color-light-blue);
}

/**
 * ==== GLOBAL changes ====
 */

/* Sidebar */
.rcx-sidebar-topbar__wrapper .rcx-icon {
  font-size: 1.1rem !important;
}

.rcx-sidebar-topbar__wrapper .rcx-button--small-square {
  width: 20px;
  height: 20px;
}

.rcx-sidebar-topbar__wrapper .rcx-button--small-square:last-child {
  display: none;
}

.rcx-sidebar-topbar__wrapper .rcx-button-group {
  margin-right: -0.25rem;
}

.rcx-sidebar-topbar__wrapper .rcx-button-group .rcx-button-group__item {
  margin-left: .2rem;
  margin-right: .2rem;
}

.rcx-sidebar-footer {
  display: none;
}

/* Add gap to bottom of sidebar */
.rcx-box.rcx-box--full.rcx-css-1cb6i7s {
  padding-bottom: 30px;
}

@media (min-width: 1372px) {
  .sidebar {
    width: 15%;
    max-width: 15%;
  }
}

/* Code tags */
.rcx-box--with-inline-elements code,
.rcx-field__description code,
.rcx-field__error code,
.rcx-field__hint code,
.rcx-field__link code {
  color: var(--tags-color) !important;
}

.rc-old .code-colors {
  color: var(--tags-color);
}

/* Others */
.rc-old .message-popup-title {
  font-weight: 700;
}

.rcx-message-system__block .rcx-message-system__body,
.rcx-message-system__block .rcx-message-system__name,
.rcx-message-system__block .rcx-message-system__time {
  font-size: 0.8rem;
}

.rcx-message-system__block .rcx-message-system__name {
  opacity: .7;
}

/**
 * ==== DARK MODE styling ====
 */
.dark-mode .rcx-sidebar {
  background-color: var(--sidebar-background-color);
}

.dark-mode .rcx-sidebar-topbar__wrapper .rcx-button--icon {
  background-color: var(--sidebar-background-color);
  border-color: var(--sidebar-background-color);
}

.dark-mode .rc-message-box,
.dark-mode .message.active,
.dark-mode .message:hover {
  background-color: var(--dark-background);
}

.dark-mode .emoji-picker {
  background-color: rgba(26, 28, 29, 0.98);
}

.dark-mode .message .reactions > li,
.dark-mode .rcx-message-reactions__reaction {
  background-color: var(--icon-background-color);
  border-color: var(--icon-background-color);
}

.dark-mode .message-actions {
  background-color: var(--rcx-color-surface-light);
  border-color: var(--rcx-color-stroke-extra-light);
}

.dark-mode .rc-popover__item:hover {
  background-color: var(--dark-background);
}

.dark-mode .message.new-day:before {
  color: var(--rcx-message-divider-color);
}

.dark-mode .rc-old .code-colors {
  border-color: var(--tags-border-color);
  background-color: var(--tags-background-color);
}

.dark-mode .rcx-message-header__name {
  color: var(--message-header-name-color);
}

.dark-mode .rcx-css-1fbr01f {
  border-color: #3e91fc !important;
}

/* Quote & code */
.dark-mode .hljs-keyword,
.dark-mode .hljs-selector-tag,
.dark-mode .hljs-subst {
  color: var(--dark-color);
}

.dark-mode .hljs-section,
.dark-mode .hljs-selector-id,
.dark-mode .hljs-title {
  color: #e33c3c;
}

.dark-mode .hljs-literal,
.dark-mode .hljs-number,
.dark-mode .hljs-tag .hljs-attr,
.dark-mode .hljs-template-variable,
.dark-mode .hljs-variable {
  color: #20cbcb;
}

.dark-mode .hljs-attribute,
.dark-mode .hljs-name,
.dark-mode .hljs-tag {
  color: #9f9fee;
}

.dark-mode .hljs-doctag,
.dark-mode .hljs-string {
  color: #f595ad;
}

```


2. Custom Script:


```javascript
// Dark mode toggle
const darkModeDefault = false;

const darkModeSymbol = `<svg id="icon-darkmode" viewBox="0 0 468 468" fill="currentColor">
  <path d="m428.75601,300.104c-0.664,-3.81 -2.33401,-7.047 -4.996,-9.71301c-5.89999,-5.90298 -12.75201,-7.142 -20.55399,-3.716c-20.93701,9.70801 -42.64102,14.55801 -65.09702,14.55801c-28.17099,0 -54.15201,-6.94 -77.94299,-20.83801c-23.791,-13.89398 -42.63101,-32.73599 -56.52501,-56.52998c-13.899,-23.793 -20.84399,-49.77299 -20.84399,-77.94499c0,-21.88802 4.33299,-42.68301 12.991,-62.384c8.66,-19.7 21.17599,-36.973 37.543,-51.82c6.283,-5.898 7.713,-12.752 4.287,-20.557c-3.23601,-7.801 -9.041,-11.511 -17.41501,-11.132c-29.12099,1.141 -56.71999,7.664 -82.797,19.556c-26.076,11.89499 -48.48901,27.54699 -67.23801,46.96499c-18.747,19.414 -33.595,42.39899 -44.54,68.94999c-10.942,26.55301 -16.416,54.39 -16.416,83.51102c0,29.694 5.806,58.05399 17.416,85.082c11.613,27.02798 27.218,50.34399 46.824,69.94897c19.604,19.599 42.92,35.207 69.951,46.82202c27.028,11.60699 55.38399,17.41498 85.075,17.41498c42.63998,0 81.987,-11.56299 118.05399,-34.69c36.069,-23.12399 63.05002,-54.00598 80.944,-92.64499c1.52402,-3.42297 1.95102,-7.03598 1.28003,-10.83798zm-122.19101,84.064c-24.646,11.711 -50.67599,17.56201 -78.08701,17.56201c-24.743,0 -48.38998,-4.853 -70.94699,-14.55801c-22.554,-9.70499 -41.97099,-22.69501 -58.24599,-38.97198c-16.271,-16.272 -29.259,-35.686 -38.97,-58.241c-9.707,-22.556 -14.561,-46.20302 -14.561,-70.94801c0,-40.922 12.135,-77.466 36.403,-109.636c24.266,-32.165 55.53099,-53.959 93.78799,-65.379c-19.795,31.405 -29.694,65.379 -29.694,101.926c0,34.644 8.564,66.715 25.69701,96.22301c17.12799,29.49901 40.446,52.81099 69.95,69.94798c29.49899,17.129 61.565,25.694 96.211,25.694c10.65601,0 21.129,-0.85498 31.40799,-2.56998c-17.31799,20.93799 -38.30701,37.25497 -62.952,48.95099z"/>
</svg>`; // moon icon
const lightModeSymbol = `<svg id="icon-darkmode" viewBox="0 0 302.4 302.4" fill="currentColor">
  <path d="m204.8,97.6c-13.60001,-13.6 -32.8,-22.4 -53.60001,-22.4s-40,8.4 -53.6,22.4c-13.6,13.6 -22.4,32.8 -22.4,53.6s8.8,40 22.4,53.59999c13.6,13.60001 32.8,22.40001 53.6,22.40001s40,-8.40001 53.60001,-22.40001c13.59999,-13.59999 22.39999,-32.8 22.39999,-53.59999s-8.39999,-40 -22.39999,-53.6zm-14.40001,92.8c-10,10 -24,16 -39.2,16s-29.2,-6 -39.2,-16s-16,-24 -16,-39.2s6,-29.2 16,-39.2s23.99999,-16 39.2,-16s29.2,6 39.2,16s16,23.99999 16,39.2s-6,29.2 -16,39.2z"/>
  <path d="m292,140.8l-30.79999,0c-5.60001,0 -10.40001,4.8 -10.40001,10.39999c0,5.60001 4.8,10.40001 10.40001,10.40001l30.79999,0c5.60001,0 10.39999,-4.8 10.39999,-10.40001c0,-5.59999 -4.79999,-10.39999 -10.39999,-10.39999z"/>
  <path d="m151.2,250.8c-5.59999,0 -10.39999,4.8 -10.39999,10.40001l0,30.79999c0,5.60001 4.8,10.39999 10.39999,10.39999c5.60001,0 10.40001,-4.79999 10.40001,-10.39999l0,-30.79999c0,-5.60001 -4.8,-10.40001 -10.40001,-10.40001z"/>
  <path d="m258,243.60001l-22,-22c-3.60001,-4 -10.39999,-4 -14.39999,0s-4,10.40001 0,14.40001l22,21.99998c4,4 10.39999,4 14.39999,0s4,-10.39999 0,-14.39999z"/>
  <path d="m151.2,0c-5.59999,0 -10.39999,4.8 -10.39999,10.4l0,30.8c0,5.6 4.8,10.4 10.39999,10.4c5.60001,0 10.40001,-4.8 10.40001,-10.4l0,-30.8c0,-5.6 -4.8,-10.4 -10.40001,-10.4z"/>
  <path d="m258.39999,44.4c-4,-4 -10.40001,-4 -14.40001,0l-22,22c-4,4 -4,10.4 0,14.4c3.60001,4 10.40001,4 14.40001,0l22,-22c4,-4 4,-10.4 0,-14.4z"/>
  <path d="m41.2,140.8l-30.8,0c-5.6,0 -10.4,4.8 -10.4,10.39999s4.4,10.40001 10.4,10.40001l30.8,0c5.6,0 10.4,-4.8 10.4,-10.40001c0,-5.59999 -4.8,-10.39999 -10.4,-10.39999z"/>
  <path d="m80.4,221.60001c-3.6,-4 -10.4,-4 -14.4,0l-22,22c-4,4 -4,10.40001 0,14.39999s10.4,4 14.4,0l22,-21.99998c4,-4.00002 4,-10.40001 0,-14.40001z"/>
  <path d="m80.4,66.4l-22,-22c-4,-4 -10.4,-4 -14.4,0s-4,10.4 0,14.4l22,22c4,4 10.4,4 14.4,0s4,-10.4 0,-14.4z"/>
</svg>`; // sun icon
const toggleButton = '<button class="rcx-box rcx-box--full rcx-button--small-square rcx-button--square rcx-button--icon rcx-button  rcx-button-group__item" aria-label="Toggle Dark Mode">D</button>';

function isDarkModeSet() {
  return localStorage.getItem('dark-mode') === 'true';
}

function getDarkModeIcon() {
  return `<svg class="rc-icon sidebar__toolbar-button-icon sidebar__toolbar-button-icon--darkmode" aria-hidden="true">
    <use xlink:href="#icon-darkmode"></use>
    ${isDarkModeSet() ? lightModeSymbol : darkModeSymbol}
  </svg>`;
}

function toggleDarkMode() {
  document.body.classList.toggle('dark-mode');
  const setting = (!isDarkModeSet()).toString();
  localStorage.setItem('dark-mode', setting);
}

function addDarkModeToggle() {
  const sidebarToolbar = $('.rcx-sidebar-topbar__wrapper .rcx-button-group--medium');

  // wait for the sidebar toolbar to be visible
  // this will also be false if the toolbar doesn't exist yet
  if(!sidebarToolbar.is(':visible')) {
    setTimeout(addDarkModeToggle, 250);
    return;
  }

  var darkModeButton = $('.js-button[aria-label="Toggle Dark Mode"]');

  // do nothing if button is already on the screen
  if (darkModeButton.is(':visible')) {
  	return;
  }

  darkModeButton = $(toggleButton).prependTo(sidebarToolbar);
  darkModeButton.html(getDarkModeIcon());

  darkModeButton.on('click', function() {
    toggleDarkMode();
    darkModeButton.html(getDarkModeIcon());
  });
}

if (localStorage.getItem('dark-mode') !== 'false'
    && window.location.href.indexOf('admin') === -1) {
  document.body.classList.add('dark-mode');
}

$(addDarkModeToggle);
```

