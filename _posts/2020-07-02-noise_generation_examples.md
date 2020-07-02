---
layout: post
categories: posts
title: Noise Generation Examples
tags: [Python]
date-string: JULY 02, 2020
---

<!DOCTYPE html>
<html>
<head><meta charset="utf-8" />

<title>generate_noise_example</title>

<script src="https://cdnjs.cloudflare.com/ajax/libs/require.js/2.1.10/require.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/2.0.3/jquery.min.js"></script>



<style type="text/css">
    /*!
*
* Twitter Bootstrap
*
*/
/*!
 * Bootstrap v3.3.7 (http://getbootstrap.com)
 * Copyright 2011-2016 Twitter, Inc.
 * Licensed under MIT (https://github.com/twbs/bootstrap/blob/master/LICENSE)
 */
/*! normalize.css v3.0.3 | MIT License | github.com/necolas/normalize.css */
html {
  font-family: sans-serif;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
}
body {
  margin: 0;
}
article,
aside,
details,
figcaption,
figure,
footer,
header,
hgroup,
main,
menu,
nav,
section,
summary {
  display: block;
}
audio,
canvas,
progress,
video {
  display: inline-block;
  vertical-align: baseline;
}
audio:not([controls]) {
  display: none;
  height: 0;
}
[hidden],
template {
  display: none;
}
a {
  background-color: transparent;
}
a:active,
a:hover {
  outline: 0;
}
abbr[title] {
  border-bottom: 1px dotted;
}
b,
strong {
  font-weight: bold;
}
dfn {
  font-style: italic;
}
h1 {
  font-size: 2em;
  margin: 0.67em 0;
}
mark {
  background: #ff0;
  color: #000;
}
small {
  font-size: 80%;
}
sub,
sup {
  font-size: 75%;
  line-height: 0;
  position: relative;
  vertical-align: baseline;
}
sup {
  top: -0.5em;
}
sub {
  bottom: -0.25em;
}
img {
  border: 0;
}
svg:not(:root) {
  overflow: hidden;
}
figure {
  margin: 1em 40px;
}
hr {
  box-sizing: content-box;
  height: 0;
}
pre {
  overflow: auto;
}
code,
kbd,
pre,
samp {
  font-family: monospace, monospace;
  font-size: 1em;
}
button,
input,
optgroup,
select,
textarea {
  color: inherit;
  font: inherit;
  margin: 0;
}
button {
  overflow: visible;
}
button,
select {
  text-transform: none;
}
button,
html input[type="button"],
input[type="reset"],
input[type="submit"] {
  -webkit-appearance: button;
  cursor: pointer;
}
button[disabled],
html input[disabled] {
  cursor: default;
}
button::-moz-focus-inner,
input::-moz-focus-inner {
  border: 0;
  padding: 0;
}
input {
  line-height: normal;
}
input[type="checkbox"],
input[type="radio"] {
  box-sizing: border-box;
  padding: 0;
}
input[type="number"]::-webkit-inner-spin-button,
input[type="number"]::-webkit-outer-spin-button {
  height: auto;
}
input[type="search"] {
  -webkit-appearance: textfield;
  box-sizing: content-box;
}
input[type="search"]::-webkit-search-cancel-button,
input[type="search"]::-webkit-search-decoration {
  -webkit-appearance: none;
}
fieldset {
  border: 1px solid #c0c0c0;
  margin: 0 2px;
  padding: 0.35em 0.625em 0.75em;
}
legend {
  border: 0;
  padding: 0;
}
textarea {
  overflow: auto;
}
optgroup {
  font-weight: bold;
}
table {
  border-collapse: collapse;
  border-spacing: 0;
}
td,
th {
  padding: 0;
}
/*! Source: https://github.com/h5bp/html5-boilerplate/blob/master/src/css/main.css */
@media print {
  *,
  *:before,
  *:after {
    background: transparent !important;
    box-shadow: none !important;
    text-shadow: none !important;
  }
  a,
  a:visited {
    text-decoration: underline;
  }
  a[href]:after {
    content: " (" attr(href) ")";
  }
  abbr[title]:after {
    content: " (" attr(title) ")";
  }
  a[href^="#"]:after,
  a[href^="javascript:"]:after {
    content: "";
  }
  pre,
  blockquote {
    border: 1px solid #999;
    page-break-inside: avoid;
  }
  thead {
    display: table-header-group;
  }
  tr,
  img {
    page-break-inside: avoid;
  }
  img {
    max-width: 100% !important;
  }
  p,
  h2,
  h3 {
    orphans: 3;
    widows: 3;
  }
  h2,
  h3 {
    page-break-after: avoid;
  }
  .navbar {
    display: none;
  }
  .btn > .caret,
  .dropup > .btn > .caret {
    border-top-color: #000 !important;
  }
  .label {
    border: 1px solid #000;
  }
  .table {
    border-collapse: collapse !important;
  }
  .table td,
  .table th {
    background-color: #fff !important;
  }
  .table-bordered th,
  .table-bordered td {
    border: 1px solid #ddd !important;
  }
}
@font-face {
  font-family: 'Glyphicons Halflings';
  src: url('../components/bootstrap/fonts/glyphicons-halflings-regular.eot');
  src: url('../components/bootstrap/fonts/glyphicons-halflings-regular.eot?#iefix') format('embedded-opentype'), url('../components/bootstrap/fonts/glyphicons-halflings-regular.woff2') format('woff2'), url('../components/bootstrap/fonts/glyphicons-halflings-regular.woff') format('woff'), url('../components/bootstrap/fonts/glyphicons-halflings-regular.ttf') format('truetype'), url('../components/bootstrap/fonts/glyphicons-halflings-regular.svg#glyphicons_halflingsregular') format('svg');
}
.glyphicon {
  position: relative;
  top: 1px;
  display: inline-block;
  font-family: 'Glyphicons Halflings';
  font-style: normal;
  font-weight: normal;
  line-height: 1;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
.glyphicon-asterisk:before {
  content: "\002a";
}
.glyphicon-plus:before {
  content: "\002b";
}
.glyphicon-euro:before,
.glyphicon-eur:before {
  content: "\20ac";
}
.glyphicon-minus:before {
  content: "\2212";
}
.glyphicon-cloud:before {
  content: "\2601";
}
.glyphicon-envelope:before {
  content: "\2709";
}
.glyphicon-pencil:before {
  content: "\270f";
}
.glyphicon-glass:before {
  content: "\e001";
}
.glyphicon-music:before {
  content: "\e002";
}
.glyphicon-search:before {
  content: "\e003";
}
.glyphicon-heart:before {
  content: "\e005";
}
.glyphicon-star:before {
  content: "\e006";
}
.glyphicon-star-empty:before {
  content: "\e007";
}
.glyphicon-user:before {
  content: "\e008";
}
.glyphicon-film:before {
  content: "\e009";
}
.glyphicon-th-large:before {
  content: "\e010";
}
.glyphicon-th:before {
  content: "\e011";
}
.glyphicon-th-list:before {
  content: "\e012";
}
.glyphicon-ok:before {
  content: "\e013";
}
.glyphicon-remove:before {
  content: "\e014";
}
.glyphicon-zoom-in:before {
  content: "\e015";
}
.glyphicon-zoom-out:before {
  content: "\e016";
}
.glyphicon-off:before {
  content: "\e017";
}
.glyphicon-signal:before {
  content: "\e018";
}
.glyphicon-cog:before {
  content: "\e019";
}
.glyphicon-trash:before {
  content: "\e020";
}
.glyphicon-home:before {
  content: "\e021";
}
.glyphicon-file:before {
  content: "\e022";
}
.glyphicon-time:before {
  content: "\e023";
}
.glyphicon-road:before {
  content: "\e024";
}
.glyphicon-download-alt:before {
  content: "\e025";
}
.glyphicon-download:before {
  content: "\e026";
}
.glyphicon-upload:before {
  content: "\e027";
}
.glyphicon-inbox:before {
  content: "\e028";
}
.glyphicon-play-circle:before {
  content: "\e029";
}
.glyphicon-repeat:before {
  content: "\e030";
}
.glyphicon-refresh:before {
  content: "\e031";
}
.glyphicon-list-alt:before {
  content: "\e032";
}
.glyphicon-lock:before {
  content: "\e033";
}
.glyphicon-flag:before {
  content: "\e034";
}
.glyphicon-headphones:before {
  content: "\e035";
}
.glyphicon-volume-off:before {
  content: "\e036";
}
.glyphicon-volume-down:before {
  content: "\e037";
}
.glyphicon-volume-up:before {
  content: "\e038";
}
.glyphicon-qrcode:before {
  content: "\e039";
}
.glyphicon-barcode:before {
  content: "\e040";
}
.glyphicon-tag:before {
  content: "\e041";
}
.glyphicon-tags:before {
  content: "\e042";
}
.glyphicon-book:before {
  content: "\e043";
}
.glyphicon-bookmark:before {
  content: "\e044";
}
.glyphicon-print:before {
  content: "\e045";
}
.glyphicon-camera:before {
  content: "\e046";
}
.glyphicon-font:before {
  content: "\e047";
}
.glyphicon-bold:before {
  content: "\e048";
}
.glyphicon-italic:before {
  content: "\e049";
}
.glyphicon-text-height:before {
  content: "\e050";
}
.glyphicon-text-width:before {
  content: "\e051";
}
.glyphicon-align-left:before {
  content: "\e052";
}
.glyphicon-align-center:before {
  content: "\e053";
}
.glyphicon-align-right:before {
  content: "\e054";
}
.glyphicon-align-justify:before {
  content: "\e055";
}
.glyphicon-list:before {
  content: "\e056";
}
.glyphicon-indent-left:before {
  content: "\e057";
}
.glyphicon-indent-right:before {
  content: "\e058";
}
.glyphicon-facetime-video:before {
  content: "\e059";
}
.glyphicon-picture:before {
  content: "\e060";
}
.glyphicon-map-marker:before {
  content: "\e062";
}
.glyphicon-adjust:before {
  content: "\e063";
}
.glyphicon-tint:before {
  content: "\e064";
}
.glyphicon-edit:before {
  content: "\e065";
}
.glyphicon-share:before {
  content: "\e066";
}
.glyphicon-check:before {
  content: "\e067";
}
.glyphicon-move:before {
  content: "\e068";
}
.glyphicon-step-backward:before {
  content: "\e069";
}
.glyphicon-fast-backward:before {
  content: "\e070";
}
.glyphicon-backward:before {
  content: "\e071";
}
.glyphicon-play:before {
  content: "\e072";
}
.glyphicon-pause:before {
  content: "\e073";
}
.glyphicon-stop:before {
  content: "\e074";
}
.glyphicon-forward:before {
  content: "\e075";
}
.glyphicon-fast-forward:before {
  content: "\e076";
}
.glyphicon-step-forward:before {
  content: "\e077";
}
.glyphicon-eject:before {
  content: "\e078";
}
.glyphicon-chevron-left:before {
  content: "\e079";
}
.glyphicon-chevron-right:before {
  content: "\e080";
}
.glyphicon-plus-sign:before {
  content: "\e081";
}
.glyphicon-minus-sign:before {
  content: "\e082";
}
.glyphicon-remove-sign:before {
  content: "\e083";
}
.glyphicon-ok-sign:before {
  content: "\e084";
}
.glyphicon-question-sign:before {
  content: "\e085";
}
.glyphicon-info-sign:before {
  content: "\e086";
}
.glyphicon-screenshot:before {
  content: "\e087";
}
.glyphicon-remove-circle:before {
  content: "\e088";
}
.glyphicon-ok-circle:before {
  content: "\e089";
}
.glyphicon-ban-circle:before {
  content: "\e090";
}
.glyphicon-arrow-left:before {
  content: "\e091";
}
.glyphicon-arrow-right:before {
  content: "\e092";
}
.glyphicon-arrow-up:before {
  content: "\e093";
}
.glyphicon-arrow-down:before {
  content: "\e094";
}
.glyphicon-share-alt:before {
  content: "\e095";
}
.glyphicon-resize-full:before {
  content: "\e096";
}
.glyphicon-resize-small:before {
  content: "\e097";
}
.glyphicon-exclamation-sign:before {
  content: "\e101";
}
.glyphicon-gift:before {
  content: "\e102";
}
.glyphicon-leaf:before {
  content: "\e103";
}
.glyphicon-fire:before {
  content: "\e104";
}
.glyphicon-eye-open:before {
  content: "\e105";
}
.glyphicon-eye-close:before {
  content: "\e106";
}
.glyphicon-warning-sign:before {
  content: "\e107";
}
.glyphicon-plane:before {
  content: "\e108";
}
.glyphicon-calendar:before {
  content: "\e109";
}
.glyphicon-random:before {
  content: "\e110";
}
.glyphicon-comment:before {
  content: "\e111";
}
.glyphicon-magnet:before {
  content: "\e112";
}
.glyphicon-chevron-up:before {
  content: "\e113";
}
.glyphicon-chevron-down:before {
  content: "\e114";
}
.glyphicon-retweet:before {
  content: "\e115";
}
.glyphicon-shopping-cart:before {
  content: "\e116";
}
.glyphicon-folder-close:before {
  content: "\e117";
}
.glyphicon-folder-open:before {
  content: "\e118";
}
.glyphicon-resize-vertical:before {
  content: "\e119";
}
.glyphicon-resize-horizontal:before {
  content: "\e120";
}
.glyphicon-hdd:before {
  content: "\e121";
}
.glyphicon-bullhorn:before {
  content: "\e122";
}
.glyphicon-bell:before {
  content: "\e123";
}
.glyphicon-certificate:before {
  content: "\e124";
}
.glyphicon-thumbs-up:before {
  content: "\e125";
}
.glyphicon-thumbs-down:before {
  content: "\e126";
}
.glyphicon-hand-right:before {
  content: "\e127";
}
.glyphicon-hand-left:before {
  content: "\e128";
}
.glyphicon-hand-up:before {
  content: "\e129";
}
.glyphicon-hand-down:before {
  content: "\e130";
}
.glyphicon-circle-arrow-right:before {
  content: "\e131";
}
.glyphicon-circle-arrow-left:before {
  content: "\e132";
}
.glyphicon-circle-arrow-up:before {
  content: "\e133";
}
.glyphicon-circle-arrow-down:before {
  content: "\e134";
}
.glyphicon-globe:before {
  content: "\e135";
}
.glyphicon-wrench:before {
  content: "\e136";
}
.glyphicon-tasks:before {
  content: "\e137";
}
.glyphicon-filter:before {
  content: "\e138";
}
.glyphicon-briefcase:before {
  content: "\e139";
}
.glyphicon-fullscreen:before {
  content: "\e140";
}
.glyphicon-dashboard:before {
  content: "\e141";
}
.glyphicon-paperclip:before {
  content: "\e142";
}
.glyphicon-heart-empty:before {
  content: "\e143";
}
.glyphicon-link:before {
  content: "\e144";
}
.glyphicon-phone:before {
  content: "\e145";
}
.glyphicon-pushpin:before {
  content: "\e146";
}
.glyphicon-usd:before {
  content: "\e148";
}
.glyphicon-gbp:before {
  content: "\e149";
}
.glyphicon-sort:before {
  content: "\e150";
}
.glyphicon-sort-by-alphabet:before {
  content: "\e151";
}
.glyphicon-sort-by-alphabet-alt:before {
  content: "\e152";
}
.glyphicon-sort-by-order:before {
  content: "\e153";
}
.glyphicon-sort-by-order-alt:before {
  content: "\e154";
}
.glyphicon-sort-by-attributes:before {
  content: "\e155";
}
.glyphicon-sort-by-attributes-alt:before {
  content: "\e156";
}
.glyphicon-unchecked:before {
  content: "\e157";
}
.glyphicon-expand:before {
  content: "\e158";
}
.glyphicon-collapse-down:before {
  content: "\e159";
}
.glyphicon-collapse-up:before {
  content: "\e160";
}
.glyphicon-log-in:before {
  content: "\e161";
}
.glyphicon-flash:before {
  content: "\e162";
}
.glyphicon-log-out:before {
  content: "\e163";
}
.glyphicon-new-window:before {
  content: "\e164";
}
.glyphicon-record:before {
  content: "\e165";
}
.glyphicon-save:before {
  content: "\e166";
}
.glyphicon-open:before {
  content: "\e167";
}
.glyphicon-saved:before {
  content: "\e168";
}
.glyphicon-import:before {
  content: "\e169";
}
.glyphicon-export:before {
  content: "\e170";
}
.glyphicon-send:before {
  content: "\e171";
}
.glyphicon-floppy-disk:before {
  content: "\e172";
}
.glyphicon-floppy-saved:before {
  content: "\e173";
}
.glyphicon-floppy-remove:before {
  content: "\e174";
}
.glyphicon-floppy-save:before {
  content: "\e175";
}
.glyphicon-floppy-open:before {
  content: "\e176";
}
.glyphicon-credit-card:before {
  content: "\e177";
}
.glyphicon-transfer:before {
  content: "\e178";
}
.glyphicon-cutlery:before {
  content: "\e179";
}
.glyphicon-header:before {
  content: "\e180";
}
.glyphicon-compressed:before {
  content: "\e181";
}
.glyphicon-earphone:before {
  content: "\e182";
}
.glyphicon-phone-alt:before {
  content: "\e183";
}
.glyphicon-tower:before {
  content: "\e184";
}
.glyphicon-stats:before {
  content: "\e185";
}
.glyphicon-sd-video:before {
  content: "\e186";
}
.glyphicon-hd-video:before {
  content: "\e187";
}
.glyphicon-subtitles:before {
  content: "\e188";
}
.glyphicon-sound-stereo:before {
  content: "\e189";
}
.glyphicon-sound-dolby:before {
  content: "\e190";
}
.glyphicon-sound-5-1:before {
  content: "\e191";
}
.glyphicon-sound-6-1:before {
  content: "\e192";
}
.glyphicon-sound-7-1:before {
  content: "\e193";
}
.glyphicon-copyright-mark:before {
  content: "\e194";
}
.glyphicon-registration-mark:before {
  content: "\e195";
}
.glyphicon-cloud-download:before {
  content: "\e197";
}
.glyphicon-cloud-upload:before {
  content: "\e198";
}
.glyphicon-tree-conifer:before {
  content: "\e199";
}
.glyphicon-tree-deciduous:before {
  content: "\e200";
}
.glyphicon-cd:before {
  content: "\e201";
}
.glyphicon-save-file:before {
  content: "\e202";
}
.glyphicon-open-file:before {
  content: "\e203";
}
.glyphicon-level-up:before {
  content: "\e204";
}
.glyphicon-copy:before {
  content: "\e205";
}
.glyphicon-paste:before {
  content: "\e206";
}
.glyphicon-alert:before {
  content: "\e209";
}
.glyphicon-equalizer:before {
  content: "\e210";
}
.glyphicon-king:before {
  content: "\e211";
}
.glyphicon-queen:before {
  content: "\e212";
}
.glyphicon-pawn:before {
  content: "\e213";
}
.glyphicon-bishop:before {
  content: "\e214";
}
.glyphicon-knight:before {
  content: "\e215";
}
.glyphicon-baby-formula:before {
  content: "\e216";
}
.glyphicon-tent:before {
  content: "\26fa";
}
.glyphicon-blackboard:before {
  content: "\e218";
}
.glyphicon-bed:before {
  content: "\e219";
}
.glyphicon-apple:before {
  content: "\f8ff";
}
.glyphicon-erase:before {
  content: "\e221";
}
.glyphicon-hourglass:before {
  content: "\231b";
}
.glyphicon-lamp:before {
  content: "\e223";
}
.glyphicon-duplicate:before {
  content: "\e224";
}
.glyphicon-piggy-bank:before {
  content: "\e225";
}
.glyphicon-scissors:before {
  content: "\e226";
}
.glyphicon-bitcoin:before {
  content: "\e227";
}
.glyphicon-btc:before {
  content: "\e227";
}
.glyphicon-xbt:before {
  content: "\e227";
}
.glyphicon-yen:before {
  content: "\00a5";
}
.glyphicon-jpy:before {
  content: "\00a5";
}
.glyphicon-ruble:before {
  content: "\20bd";
}
.glyphicon-rub:before {
  content: "\20bd";
}
.glyphicon-scale:before {
  content: "\e230";
}
.glyphicon-ice-lolly:before {
  content: "\e231";
}
.glyphicon-ice-lolly-tasted:before {
  content: "\e232";
}
.glyphicon-education:before {
  content: "\e233";
}
.glyphicon-option-horizontal:before {
  content: "\e234";
}
.glyphicon-option-vertical:before {
  content: "\e235";
}
.glyphicon-menu-hamburger:before {
  content: "\e236";
}
.glyphicon-modal-window:before {
  content: "\e237";
}
.glyphicon-oil:before {
  content: "\e238";
}
.glyphicon-grain:before {
  content: "\e239";
}
.glyphicon-sunglasses:before {
  content: "\e240";
}
.glyphicon-text-size:before {
  content: "\e241";
}
.glyphicon-text-color:before {
  content: "\e242";
}
.glyphicon-text-background:before {
  content: "\e243";
}
.glyphicon-object-align-top:before {
  content: "\e244";
}
.glyphicon-object-align-bottom:before {
  content: "\e245";
}
.glyphicon-object-align-horizontal:before {
  content: "\e246";
}
.glyphicon-object-align-left:before {
  content: "\e247";
}
.glyphicon-object-align-vertical:before {
  content: "\e248";
}
.glyphicon-object-align-right:before {
  content: "\e249";
}
.glyphicon-triangle-right:before {
  content: "\e250";
}
.glyphicon-triangle-left:before {
  content: "\e251";
}
.glyphicon-triangle-bottom:before {
  content: "\e252";
}
.glyphicon-triangle-top:before {
  content: "\e253";
}
.glyphicon-console:before {
  content: "\e254";
}
.glyphicon-superscript:before {
  content: "\e255";
}
.glyphicon-subscript:before {
  content: "\e256";
}
.glyphicon-menu-left:before {
  content: "\e257";
}
.glyphicon-menu-right:before {
  content: "\e258";
}
.glyphicon-menu-down:before {
  content: "\e259";
}
.glyphicon-menu-up:before {
  content: "\e260";
}
* {
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
}
*:before,
*:after {
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
}
html {
  font-size: 10px;
  -webkit-tap-highlight-color: rgba(0, 0, 0, 0);
}
body {
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
  font-size: 13px;
  line-height: 1.42857143;
  color: #000;
  background-color: #fff;
}
input,
button,
select,
textarea {
  font-family: inherit;
  font-size: inherit;
  line-height: inherit;
}
a {
  color: #337ab7;
  text-decoration: none;
}
a:hover,
a:focus {
  color: #23527c;
  text-decoration: underline;
}
a:focus {
  outline: 5px auto -webkit-focus-ring-color;
  outline-offset: -2px;
}
figure {
  margin: 0;
}
img {
  vertical-align: middle;
}
.img-responsive,
.thumbnail > img,
.thumbnail a > img,
.carousel-inner > .item > img,
.carousel-inner > .item > a > img {
  display: block;
  max-width: 100%;
  height: auto;
}
.img-rounded {
  border-radius: 3px;
}
.img-thumbnail {
  padding: 4px;
  line-height: 1.42857143;
  background-color: #fff;
  border: 1px solid #ddd;
  border-radius: 2px;
  -webkit-transition: all 0.2s ease-in-out;
  -o-transition: all 0.2s ease-in-out;
  transition: all 0.2s ease-in-out;
  display: inline-block;
  max-width: 100%;
  height: auto;
}
.img-circle {
  border-radius: 50%;
}
hr {
  margin-top: 18px;
  margin-bottom: 18px;
  border: 0;
  border-top: 1px solid #eeeeee;
}
.sr-only {
  position: absolute;
  width: 1px;
  height: 1px;
  margin: -1px;
  padding: 0;
  overflow: hidden;
  clip: rect(0, 0, 0, 0);
  border: 0;
}
.sr-only-focusable:active,
.sr-only-focusable:focus {
  position: static;
  width: auto;
  height: auto;
  margin: 0;
  overflow: visible;
  clip: auto;
}
[role="button"] {
  cursor: pointer;
}
h1,
h2,
h3,
h4,
h5,
h6,
.h1,
.h2,
.h3,
.h4,
.h5,
.h6 {
  font-family: inherit;
  font-weight: 500;
  line-height: 1.1;
  color: inherit;
}
h1 small,
h2 small,
h3 small,
h4 small,
h5 small,
h6 small,
.h1 small,
.h2 small,
.h3 small,
.h4 small,
.h5 small,
.h6 small,
h1 .small,
h2 .small,
h3 .small,
h4 .small,
h5 .small,
h6 .small,
.h1 .small,
.h2 .small,
.h3 .small,
.h4 .small,
.h5 .small,
.h6 .small {
  font-weight: normal;
  line-height: 1;
  color: #777777;
}
h1,
.h1,
h2,
.h2,
h3,
.h3 {
  margin-top: 18px;
  margin-bottom: 9px;
}
h1 small,
.h1 small,
h2 small,
.h2 small,
h3 small,
.h3 small,
h1 .small,
.h1 .small,
h2 .small,
.h2 .small,
h3 .small,
.h3 .small {
  font-size: 65%;
}
h4,
.h4,
h5,
.h5,
h6,
.h6 {
  margin-top: 9px;
  margin-bottom: 9px;
}
h4 small,
.h4 small,
h5 small,
.h5 small,
h6 small,
.h6 small,
h4 .small,
.h4 .small,
h5 .small,
.h5 .small,
h6 .small,
.h6 .small {
  font-size: 75%;
}
h1,
.h1 {
  font-size: 33px;
}
h2,
.h2 {
  font-size: 27px;
}
h3,
.h3 {
  font-size: 23px;
}
h4,
.h4 {
  font-size: 17px;
}
h5,
.h5 {
  font-size: 13px;
}
h6,
.h6 {
  font-size: 12px;
}
p {
  margin: 0 0 9px;
}
.lead {
  margin-bottom: 18px;
  font-size: 14px;
  font-weight: 300;
  line-height: 1.4;
}
@media (min-width: 768px) {
  .lead {
    font-size: 19.5px;
  }
}
small,
.small {
  font-size: 92%;
}
mark,
.mark {
  background-color: #fcf8e3;
  padding: .2em;
}
.text-left {
  text-align: left;
}
.text-right {
  text-align: right;
}
.text-center {
  text-align: center;
}
.text-justify {
  text-align: justify;
}
.text-nowrap {
  white-space: nowrap;
}
.text-lowercase {
  text-transform: lowercase;
}
.text-uppercase {
  text-transform: uppercase;
}
.text-capitalize {
  text-transform: capitalize;
}
.text-muted {
  color: #777777;
}
.text-primary {
  color: #337ab7;
}
a.text-primary:hover,
a.text-primary:focus {
  color: #286090;
}
.text-success {
  color: #3c763d;
}
a.text-success:hover,
a.text-success:focus {
  color: #2b542c;
}
.text-info {
  color: #31708f;
}
a.text-info:hover,
a.text-info:focus {
  color: #245269;
}
.text-warning {
  color: #8a6d3b;
}
a.text-warning:hover,
a.text-warning:focus {
  color: #66512c;
}
.text-danger {
  color: #a94442;
}
a.text-danger:hover,
a.text-danger:focus {
  color: #843534;
}
.bg-primary {
  color: #fff;
  background-color: #337ab7;
}
a.bg-primary:hover,
a.bg-primary:focus {
  background-color: #286090;
}
.bg-success {
  background-color: #dff0d8;
}
a.bg-success:hover,
a.bg-success:focus {
  background-color: #c1e2b3;
}
.bg-info {
  background-color: #d9edf7;
}
a.bg-info:hover,
a.bg-info:focus {
  background-color: #afd9ee;
}
.bg-warning {
  background-color: #fcf8e3;
}
a.bg-warning:hover,
a.bg-warning:focus {
  background-color: #f7ecb5;
}
.bg-danger {
  background-color: #f2dede;
}
a.bg-danger:hover,
a.bg-danger:focus {
  background-color: #e4b9b9;
}
.page-header {
  padding-bottom: 8px;
  margin: 36px 0 18px;
  border-bottom: 1px solid #eeeeee;
}
ul,
ol {
  margin-top: 0;
  margin-bottom: 9px;
}
ul ul,
ol ul,
ul ol,
ol ol {
  margin-bottom: 0;
}
.list-unstyled {
  padding-left: 0;
  list-style: none;
}
.list-inline {
  padding-left: 0;
  list-style: none;
  margin-left: -5px;
}
.list-inline > li {
  display: inline-block;
  padding-left: 5px;
  padding-right: 5px;
}
dl {
  margin-top: 0;
  margin-bottom: 18px;
}
dt,
dd {
  line-height: 1.42857143;
}
dt {
  font-weight: bold;
}
dd {
  margin-left: 0;
}
@media (min-width: 541px) {
  .dl-horizontal dt {
    float: left;
    width: 160px;
    clear: left;
    text-align: right;
    overflow: hidden;
    text-overflow: ellipsis;
    white-space: nowrap;
  }
  .dl-horizontal dd {
    margin-left: 180px;
  }
}
abbr[title],
abbr[data-original-title] {
  cursor: help;
  border-bottom: 1px dotted #777777;
}
.initialism {
  font-size: 90%;
  text-transform: uppercase;
}
blockquote {
  padding: 9px 18px;
  margin: 0 0 18px;
  font-size: inherit;
  border-left: 5px solid #eeeeee;
}
blockquote p:last-child,
blockquote ul:last-child,
blockquote ol:last-child {
  margin-bottom: 0;
}
blockquote footer,
blockquote small,
blockquote .small {
  display: block;
  font-size: 80%;
  line-height: 1.42857143;
  color: #777777;
}
blockquote footer:before,
blockquote small:before,
blockquote .small:before {
  content: '\2014 \00A0';
}
.blockquote-reverse,
blockquote.pull-right {
  padding-right: 15px;
  padding-left: 0;
  border-right: 5px solid #eeeeee;
  border-left: 0;
  text-align: right;
}
.blockquote-reverse footer:before,
blockquote.pull-right footer:before,
.blockquote-reverse small:before,
blockquote.pull-right small:before,
.blockquote-reverse .small:before,
blockquote.pull-right .small:before {
  content: '';
}
.blockquote-reverse footer:after,
blockquote.pull-right footer:after,
.blockquote-reverse small:after,
blockquote.pull-right small:after,
.blockquote-reverse .small:after,
blockquote.pull-right .small:after {
  content: '\00A0 \2014';
}
address {
  margin-bottom: 18px;
  font-style: normal;
  line-height: 1.42857143;
}
code,
kbd,
pre,
samp {
  font-family: monospace;
}
code {
  padding: 2px 4px;
  font-size: 90%;
  color: #c7254e;
  background-color: #f9f2f4;
  border-radius: 2px;
}
kbd {
  padding: 2px 4px;
  font-size: 90%;
  color: #888;
  background-color: transparent;
  border-radius: 1px;
  box-shadow: inset 0 -1px 0 rgba(0, 0, 0, 0.25);
}
kbd kbd {
  padding: 0;
  font-size: 100%;
  font-weight: bold;
  box-shadow: none;
}
pre {
  display: block;
  padding: 8.5px;
  margin: 0 0 9px;
  font-size: 12px;
  line-height: 1.42857143;
  word-break: break-all;
  word-wrap: break-word;
  color: #333333;
  background-color: #f5f5f5;
  border: 1px solid #ccc;
  border-radius: 2px;
}
pre code {
  padding: 0;
  font-size: inherit;
  color: inherit;
  white-space: pre-wrap;
  background-color: transparent;
  border-radius: 0;
}
.pre-scrollable {
  max-height: 340px;
  overflow-y: scroll;
}
.container {
  margin-right: auto;
  margin-left: auto;
  padding-left: 0px;
  padding-right: 0px;
}
@media (min-width: 768px) {
  .container {
    width: 768px;
  }
}
@media (min-width: 992px) {
  .container {
    width: 940px;
  }
}
@media (min-width: 1200px) {
  .container {
    width: 1140px;
  }
}
.container-fluid {
  margin-right: auto;
  margin-left: auto;
  padding-left: 0px;
  padding-right: 0px;
}
.row {
  margin-left: 0px;
  margin-right: 0px;
}
.col-xs-1, .col-sm-1, .col-md-1, .col-lg-1, .col-xs-2, .col-sm-2, .col-md-2, .col-lg-2, .col-xs-3, .col-sm-3, .col-md-3, .col-lg-3, .col-xs-4, .col-sm-4, .col-md-4, .col-lg-4, .col-xs-5, .col-sm-5, .col-md-5, .col-lg-5, .col-xs-6, .col-sm-6, .col-md-6, .col-lg-6, .col-xs-7, .col-sm-7, .col-md-7, .col-lg-7, .col-xs-8, .col-sm-8, .col-md-8, .col-lg-8, .col-xs-9, .col-sm-9, .col-md-9, .col-lg-9, .col-xs-10, .col-sm-10, .col-md-10, .col-lg-10, .col-xs-11, .col-sm-11, .col-md-11, .col-lg-11, .col-xs-12, .col-sm-12, .col-md-12, .col-lg-12 {
  position: relative;
  min-height: 1px;
  padding-left: 0px;
  padding-right: 0px;
}
.col-xs-1, .col-xs-2, .col-xs-3, .col-xs-4, .col-xs-5, .col-xs-6, .col-xs-7, .col-xs-8, .col-xs-9, .col-xs-10, .col-xs-11, .col-xs-12 {
  float: left;
}
.col-xs-12 {
  width: 100%;
}
.col-xs-11 {
  width: 91.66666667%;
}
.col-xs-10 {
  width: 83.33333333%;
}
.col-xs-9 {
  width: 75%;
}
.col-xs-8 {
  width: 66.66666667%;
}
.col-xs-7 {
  width: 58.33333333%;
}
.col-xs-6 {
  width: 50%;
}
.col-xs-5 {
  width: 41.66666667%;
}
.col-xs-4 {
  width: 33.33333333%;
}
.col-xs-3 {
  width: 25%;
}
.col-xs-2 {
  width: 16.66666667%;
}
.col-xs-1 {
  width: 8.33333333%;
}
.col-xs-pull-12 {
  right: 100%;
}
.col-xs-pull-11 {
  right: 91.66666667%;
}
.col-xs-pull-10 {
  right: 83.33333333%;
}
.col-xs-pull-9 {
  right: 75%;
}
.col-xs-pull-8 {
  right: 66.66666667%;
}
.col-xs-pull-7 {
  right: 58.33333333%;
}
.col-xs-pull-6 {
  right: 50%;
}
.col-xs-pull-5 {
  right: 41.66666667%;
}
.col-xs-pull-4 {
  right: 33.33333333%;
}
.col-xs-pull-3 {
  right: 25%;
}
.col-xs-pull-2 {
  right: 16.66666667%;
}
.col-xs-pull-1 {
  right: 8.33333333%;
}
.col-xs-pull-0 {
  right: auto;
}
.col-xs-push-12 {
  left: 100%;
}
.col-xs-push-11 {
  left: 91.66666667%;
}
.col-xs-push-10 {
  left: 83.33333333%;
}
.col-xs-push-9 {
  left: 75%;
}
.col-xs-push-8 {
  left: 66.66666667%;
}
.col-xs-push-7 {
  left: 58.33333333%;
}
.col-xs-push-6 {
  left: 50%;
}
.col-xs-push-5 {
  left: 41.66666667%;
}
.col-xs-push-4 {
  left: 33.33333333%;
}
.col-xs-push-3 {
  left: 25%;
}
.col-xs-push-2 {
  left: 16.66666667%;
}
.col-xs-push-1 {
  left: 8.33333333%;
}
.col-xs-push-0 {
  left: auto;
}
.col-xs-offset-12 {
  margin-left: 100%;
}
.col-xs-offset-11 {
  margin-left: 91.66666667%;
}
.col-xs-offset-10 {
  margin-left: 83.33333333%;
}
.col-xs-offset-9 {
  margin-left: 75%;
}
.col-xs-offset-8 {
  margin-left: 66.66666667%;
}
.col-xs-offset-7 {
  margin-left: 58.33333333%;
}
.col-xs-offset-6 {
  margin-left: 50%;
}
.col-xs-offset-5 {
  margin-left: 41.66666667%;
}
.col-xs-offset-4 {
  margin-left: 33.33333333%;
}
.col-xs-offset-3 {
  margin-left: 25%;
}
.col-xs-offset-2 {
  margin-left: 16.66666667%;
}
.col-xs-offset-1 {
  margin-left: 8.33333333%;
}
.col-xs-offset-0 {
  margin-left: 0%;
}
@media (min-width: 768px) {
  .col-sm-1, .col-sm-2, .col-sm-3, .col-sm-4, .col-sm-5, .col-sm-6, .col-sm-7, .col-sm-8, .col-sm-9, .col-sm-10, .col-sm-11, .col-sm-12 {
    float: left;
  }
  .col-sm-12 {
    width: 100%;
  }
  .col-sm-11 {
    width: 91.66666667%;
  }
  .col-sm-10 {
    width: 83.33333333%;
  }
  .col-sm-9 {
    width: 75%;
  }
  .col-sm-8 {
    width: 66.66666667%;
  }
  .col-sm-7 {
    width: 58.33333333%;
  }
  .col-sm-6 {
    width: 50%;
  }
  .col-sm-5 {
    width: 41.66666667%;
  }
  .col-sm-4 {
    width: 33.33333333%;
  }
  .col-sm-3 {
    width: 25%;
  }
  .col-sm-2 {
    width: 16.66666667%;
  }
  .col-sm-1 {
    width: 8.33333333%;
  }
  .col-sm-pull-12 {
    right: 100%;
  }
  .col-sm-pull-11 {
    right: 91.66666667%;
  }
  .col-sm-pull-10 {
    right: 83.33333333%;
  }
  .col-sm-pull-9 {
    right: 75%;
  }
  .col-sm-pull-8 {
    right: 66.66666667%;
  }
  .col-sm-pull-7 {
    right: 58.33333333%;
  }
  .col-sm-pull-6 {
    right: 50%;
  }
  .col-sm-pull-5 {
    right: 41.66666667%;
  }
  .col-sm-pull-4 {
    right: 33.33333333%;
  }
  .col-sm-pull-3 {
    right: 25%;
  }
  .col-sm-pull-2 {
    right: 16.66666667%;
  }
  .col-sm-pull-1 {
    right: 8.33333333%;
  }
  .col-sm-pull-0 {
    right: auto;
  }
  .col-sm-push-12 {
    left: 100%;
  }
  .col-sm-push-11 {
    left: 91.66666667%;
  }
  .col-sm-push-10 {
    left: 83.33333333%;
  }
  .col-sm-push-9 {
    left: 75%;
  }
  .col-sm-push-8 {
    left: 66.66666667%;
  }
  .col-sm-push-7 {
    left: 58.33333333%;
  }
  .col-sm-push-6 {
    left: 50%;
  }
  .col-sm-push-5 {
    left: 41.66666667%;
  }
  .col-sm-push-4 {
    left: 33.33333333%;
  }
  .col-sm-push-3 {
    left: 25%;
  }
  .col-sm-push-2 {
    left: 16.66666667%;
  }
  .col-sm-push-1 {
    left: 8.33333333%;
  }
  .col-sm-push-0 {
    left: auto;
  }
  .col-sm-offset-12 {
    margin-left: 100%;
  }
  .col-sm-offset-11 {
    margin-left: 91.66666667%;
  }
  .col-sm-offset-10 {
    margin-left: 83.33333333%;
  }
  .col-sm-offset-9 {
    margin-left: 75%;
  }
  .col-sm-offset-8 {
    margin-left: 66.66666667%;
  }
  .col-sm-offset-7 {
    margin-left: 58.33333333%;
  }
  .col-sm-offset-6 {
    margin-left: 50%;
  }
  .col-sm-offset-5 {
    margin-left: 41.66666667%;
  }
  .col-sm-offset-4 {
    margin-left: 33.33333333%;
  }
  .col-sm-offset-3 {
    margin-left: 25%;
  }
  .col-sm-offset-2 {
    margin-left: 16.66666667%;
  }
  .col-sm-offset-1 {
    margin-left: 8.33333333%;
  }
  .col-sm-offset-0 {
    margin-left: 0%;
  }
}
@media (min-width: 992px) {
  .col-md-1, .col-md-2, .col-md-3, .col-md-4, .col-md-5, .col-md-6, .col-md-7, .col-md-8, .col-md-9, .col-md-10, .col-md-11, .col-md-12 {
    float: left;
  }
  .col-md-12 {
    width: 100%;
  }
  .col-md-11 {
    width: 91.66666667%;
  }
  .col-md-10 {
    width: 83.33333333%;
  }
  .col-md-9 {
    width: 75%;
  }
  .col-md-8 {
    width: 66.66666667%;
  }
  .col-md-7 {
    width: 58.33333333%;
  }
  .col-md-6 {
    width: 50%;
  }
  .col-md-5 {
    width: 41.66666667%;
  }
  .col-md-4 {
    width: 33.33333333%;
  }
  .col-md-3 {
    width: 25%;
  }
  .col-md-2 {
    width: 16.66666667%;
  }
  .col-md-1 {
    width: 8.33333333%;
  }
  .col-md-pull-12 {
    right: 100%;
  }
  .col-md-pull-11 {
    right: 91.66666667%;
  }
  .col-md-pull-10 {
    right: 83.33333333%;
  }
  .col-md-pull-9 {
    right: 75%;
  }
  .col-md-pull-8 {
    right: 66.66666667%;
  }
  .col-md-pull-7 {
    right: 58.33333333%;
  }
  .col-md-pull-6 {
    right: 50%;
  }
  .col-md-pull-5 {
    right: 41.66666667%;
  }
  .col-md-pull-4 {
    right: 33.33333333%;
  }
  .col-md-pull-3 {
    right: 25%;
  }
  .col-md-pull-2 {
    right: 16.66666667%;
  }
  .col-md-pull-1 {
    right: 8.33333333%;
  }
  .col-md-pull-0 {
    right: auto;
  }
  .col-md-push-12 {
    left: 100%;
  }
  .col-md-push-11 {
    left: 91.66666667%;
  }
  .col-md-push-10 {
    left: 83.33333333%;
  }
  .col-md-push-9 {
    left: 75%;
  }
  .col-md-push-8 {
    left: 66.66666667%;
  }
  .col-md-push-7 {
    left: 58.33333333%;
  }
  .col-md-push-6 {
    left: 50%;
  }
  .col-md-push-5 {
    left: 41.66666667%;
  }
  .col-md-push-4 {
    left: 33.33333333%;
  }
  .col-md-push-3 {
    left: 25%;
  }
  .col-md-push-2 {
    left: 16.66666667%;
  }
  .col-md-push-1 {
    left: 8.33333333%;
  }
  .col-md-push-0 {
    left: auto;
  }
  .col-md-offset-12 {
    margin-left: 100%;
  }
  .col-md-offset-11 {
    margin-left: 91.66666667%;
  }
  .col-md-offset-10 {
    margin-left: 83.33333333%;
  }
  .col-md-offset-9 {
    margin-left: 75%;
  }
  .col-md-offset-8 {
    margin-left: 66.66666667%;
  }
  .col-md-offset-7 {
    margin-left: 58.33333333%;
  }
  .col-md-offset-6 {
    margin-left: 50%;
  }
  .col-md-offset-5 {
    margin-left: 41.66666667%;
  }
  .col-md-offset-4 {
    margin-left: 33.33333333%;
  }
  .col-md-offset-3 {
    margin-left: 25%;
  }
  .col-md-offset-2 {
    margin-left: 16.66666667%;
  }
  .col-md-offset-1 {
    margin-left: 8.33333333%;
  }
  .col-md-offset-0 {
    margin-left: 0%;
  }
}
@media (min-width: 1200px) {
  .col-lg-1, .col-lg-2, .col-lg-3, .col-lg-4, .col-lg-5, .col-lg-6, .col-lg-7, .col-lg-8, .col-lg-9, .col-lg-10, .col-lg-11, .col-lg-12 {
    float: left;
  }
  .col-lg-12 {
    width: 100%;
  }
  .col-lg-11 {
    width: 91.66666667%;
  }
  .col-lg-10 {
    width: 83.33333333%;
  }
  .col-lg-9 {
    width: 75%;
  }
  .col-lg-8 {
    width: 66.66666667%;
  }
  .col-lg-7 {
    width: 58.33333333%;
  }
  .col-lg-6 {
    width: 50%;
  }
  .col-lg-5 {
    width: 41.66666667%;
  }
  .col-lg-4 {
    width: 33.33333333%;
  }
  .col-lg-3 {
    width: 25%;
  }
  .col-lg-2 {
    width: 16.66666667%;
  }
  .col-lg-1 {
    width: 8.33333333%;
  }
  .col-lg-pull-12 {
    right: 100%;
  }
  .col-lg-pull-11 {
    right: 91.66666667%;
  }
  .col-lg-pull-10 {
    right: 83.33333333%;
  }
  .col-lg-pull-9 {
    right: 75%;
  }
  .col-lg-pull-8 {
    right: 66.66666667%;
  }
  .col-lg-pull-7 {
    right: 58.33333333%;
  }
  .col-lg-pull-6 {
    right: 50%;
  }
  .col-lg-pull-5 {
    right: 41.66666667%;
  }
  .col-lg-pull-4 {
    right: 33.33333333%;
  }
  .col-lg-pull-3 {
    right: 25%;
  }
  .col-lg-pull-2 {
    right: 16.66666667%;
  }
  .col-lg-pull-1 {
    right: 8.33333333%;
  }
  .col-lg-pull-0 {
    right: auto;
  }
  .col-lg-push-12 {
    left: 100%;
  }
  .col-lg-push-11 {
    left: 91.66666667%;
  }
  .col-lg-push-10 {
    left: 83.33333333%;
  }
  .col-lg-push-9 {
    left: 75%;
  }
  .col-lg-push-8 {
    left: 66.66666667%;
  }
  .col-lg-push-7 {
    left: 58.33333333%;
  }
  .col-lg-push-6 {
    left: 50%;
  }
  .col-lg-push-5 {
    left: 41.66666667%;
  }
  .col-lg-push-4 {
    left: 33.33333333%;
  }
  .col-lg-push-3 {
    left: 25%;
  }
  .col-lg-push-2 {
    left: 16.66666667%;
  }
  .col-lg-push-1 {
    left: 8.33333333%;
  }
  .col-lg-push-0 {
    left: auto;
  }
  .col-lg-offset-12 {
    margin-left: 100%;
  }
  .col-lg-offset-11 {
    margin-left: 91.66666667%;
  }
  .col-lg-offset-10 {
    margin-left: 83.33333333%;
  }
  .col-lg-offset-9 {
    margin-left: 75%;
  }
  .col-lg-offset-8 {
    margin-left: 66.66666667%;
  }
  .col-lg-offset-7 {
    margin-left: 58.33333333%;
  }
  .col-lg-offset-6 {
    margin-left: 50%;
  }
  .col-lg-offset-5 {
    margin-left: 41.66666667%;
  }
  .col-lg-offset-4 {
    margin-left: 33.33333333%;
  }
  .col-lg-offset-3 {
    margin-left: 25%;
  }
  .col-lg-offset-2 {
    margin-left: 16.66666667%;
  }
  .col-lg-offset-1 {
    margin-left: 8.33333333%;
  }
  .col-lg-offset-0 {
    margin-left: 0%;
  }
}
table {
  background-color: transparent;
}
caption {
  padding-top: 8px;
  padding-bottom: 8px;
  color: #777777;
  text-align: left;
}
th {
  text-align: left;
}
.table {
  width: 100%;
  max-width: 100%;
  margin-bottom: 18px;
}
.table > thead > tr > th,
.table > tbody > tr > th,
.table > tfoot > tr > th,
.table > thead > tr > td,
.table > tbody > tr > td,
.table > tfoot > tr > td {
  padding: 8px;
  line-height: 1.42857143;
  vertical-align: top;
  border-top: 1px solid #ddd;
}
.table > thead > tr > th {
  vertical-align: bottom;
  border-bottom: 2px solid #ddd;
}
.table > caption + thead > tr:first-child > th,
.table > colgroup + thead > tr:first-child > th,
.table > thead:first-child > tr:first-child > th,
.table > caption + thead > tr:first-child > td,
.table > colgroup + thead > tr:first-child > td,
.table > thead:first-child > tr:first-child > td {
  border-top: 0;
}
.table > tbody + tbody {
  border-top: 2px solid #ddd;
}
.table .table {
  background-color: #fff;
}
.table-condensed > thead > tr > th,
.table-condensed > tbody > tr > th,
.table-condensed > tfoot > tr > th,
.table-condensed > thead > tr > td,
.table-condensed > tbody > tr > td,
.table-condensed > tfoot > tr > td {
  padding: 5px;
}
.table-bordered {
  border: 1px solid #ddd;
}
.table-bordered > thead > tr > th,
.table-bordered > tbody > tr > th,
.table-bordered > tfoot > tr > th,
.table-bordered > thead > tr > td,
.table-bordered > tbody > tr > td,
.table-bordered > tfoot > tr > td {
  border: 1px solid #ddd;
}
.table-bordered > thead > tr > th,
.table-bordered > thead > tr > td {
  border-bottom-width: 2px;
}
.table-striped > tbody > tr:nth-of-type(odd) {
  background-color: #f9f9f9;
}
.table-hover > tbody > tr:hover {
  background-color: #f5f5f5;
}
table col[class*="col-"] {
  position: static;
  float: none;
  display: table-column;
}
table td[class*="col-"],
table th[class*="col-"] {
  position: static;
  float: none;
  display: table-cell;
}
.table > thead > tr > td.active,
.table > tbody > tr > td.active,
.table > tfoot > tr > td.active,
.table > thead > tr > th.active,
.table > tbody > tr > th.active,
.table > tfoot > tr > th.active,
.table > thead > tr.active > td,
.table > tbody > tr.active > td,
.table > tfoot > tr.active > td,
.table > thead > tr.active > th,
.table > tbody > tr.active > th,
.table > tfoot > tr.active > th {
  background-color: #f5f5f5;
}
.table-hover > tbody > tr > td.active:hover,
.table-hover > tbody > tr > th.active:hover,
.table-hover > tbody > tr.active:hover > td,
.table-hover > tbody > tr:hover > .active,
.table-hover > tbody > tr.active:hover > th {
  background-color: #e8e8e8;
}
.table > thead > tr > td.success,
.table > tbody > tr > td.success,
.table > tfoot > tr > td.success,
.table > thead > tr > th.success,
.table > tbody > tr > th.success,
.table > tfoot > tr > th.success,
.table > thead > tr.success > td,
.table > tbody > tr.success > td,
.table > tfoot > tr.success > td,
.table > thead > tr.success > th,
.table > tbody > tr.success > th,
.table > tfoot > tr.success > th {
  background-color: #dff0d8;
}
.table-hover > tbody > tr > td.success:hover,
.table-hover > tbody > tr > th.success:hover,
.table-hover > tbody > tr.success:hover > td,
.table-hover > tbody > tr:hover > .success,
.table-hover > tbody > tr.success:hover > th {
  background-color: #d0e9c6;
}
.table > thead > tr > td.info,
.table > tbody > tr > td.info,
.table > tfoot > tr > td.info,
.table > thead > tr > th.info,
.table > tbody > tr > th.info,
.table > tfoot > tr > th.info,
.table > thead > tr.info > td,
.table > tbody > tr.info > td,
.table > tfoot > tr.info > td,
.table > thead > tr.info > th,
.table > tbody > tr.info > th,
.table > tfoot > tr.info > th {
  background-color: #d9edf7;
}
.table-hover > tbody > tr > td.info:hover,
.table-hover > tbody > tr > th.info:hover,
.table-hover > tbody > tr.info:hover > td,
.table-hover > tbody > tr:hover > .info,
.table-hover > tbody > tr.info:hover > th {
  background-color: #c4e3f3;
}
.table > thead > tr > td.warning,
.table > tbody > tr > td.warning,
.table > tfoot > tr > td.warning,
.table > thead > tr > th.warning,
.table > tbody > tr > th.warning,
.table > tfoot > tr > th.warning,
.table > thead > tr.warning > td,
.table > tbody > tr.warning > td,
.table > tfoot > tr.warning > td,
.table > thead > tr.warning > th,
.table > tbody > tr.warning > th,
.table > tfoot > tr.warning > th {
  background-color: #fcf8e3;
}
.table-hover > tbody > tr > td.warning:hover,
.table-hover > tbody > tr > th.warning:hover,
.table-hover > tbody > tr.warning:hover > td,
.table-hover > tbody > tr:hover > .warning,
.table-hover > tbody > tr.warning:hover > th {
  background-color: #faf2cc;
}
.table > thead > tr > td.danger,
.table > tbody > tr > td.danger,
.table > tfoot > tr > td.danger,
.table > thead > tr > th.danger,
.table > tbody > tr > th.danger,
.table > tfoot > tr > th.danger,
.table > thead > tr.danger > td,
.table > tbody > tr.danger > td,
.table > tfoot > tr.danger > td,
.table > thead > tr.danger > th,
.table > tbody > tr.danger > th,
.table > tfoot > tr.danger > th {
  background-color: #f2dede;
}
.table-hover > tbody > tr > td.danger:hover,
.table-hover > tbody > tr > th.danger:hover,
.table-hover > tbody > tr.danger:hover > td,
.table-hover > tbody > tr:hover > .danger,
.table-hover > tbody > tr.danger:hover > th {
  background-color: #ebcccc;
}
.table-responsive {
  overflow-x: auto;
  min-height: 0.01%;
}
@media screen and (max-width: 767px) {
  .table-responsive {
    width: 100%;
    margin-bottom: 13.5px;
    overflow-y: hidden;
    -ms-overflow-style: -ms-autohiding-scrollbar;
    border: 1px solid #ddd;
  }
  .table-responsive > .table {
    margin-bottom: 0;
  }
  .table-responsive > .table > thead > tr > th,
  .table-responsive > .table > tbody > tr > th,
  .table-responsive > .table > tfoot > tr > th,
  .table-responsive > .table > thead > tr > td,
  .table-responsive > .table > tbody > tr > td,
  .table-responsive > .table > tfoot > tr > td {
    white-space: nowrap;
  }
  .table-responsive > .table-bordered {
    border: 0;
  }
  .table-responsive > .table-bordered > thead > tr > th:first-child,
  .table-responsive > .table-bordered > tbody > tr > th:first-child,
  .table-responsive > .table-bordered > tfoot > tr > th:first-child,
  .table-responsive > .table-bordered > thead > tr > td:first-child,
  .table-responsive > .table-bordered > tbody > tr > td:first-child,
  .table-responsive > .table-bordered > tfoot > tr > td:first-child {
    border-left: 0;
  }
  .table-responsive > .table-bordered > thead > tr > th:last-child,
  .table-responsive > .table-bordered > tbody > tr > th:last-child,
  .table-responsive > .table-bordered > tfoot > tr > th:last-child,
  .table-responsive > .table-bordered > thead > tr > td:last-child,
  .table-responsive > .table-bordered > tbody > tr > td:last-child,
  .table-responsive > .table-bordered > tfoot > tr > td:last-child {
    border-right: 0;
  }
  .table-responsive > .table-bordered > tbody > tr:last-child > th,
  .table-responsive > .table-bordered > tfoot > tr:last-child > th,
  .table-responsive > .table-bordered > tbody > tr:last-child > td,
  .table-responsive > .table-bordered > tfoot > tr:last-child > td {
    border-bottom: 0;
  }
}
fieldset {
  padding: 0;
  margin: 0;
  border: 0;
  min-width: 0;
}
legend {
  display: block;
  width: 100%;
  padding: 0;
  margin-bottom: 18px;
  font-size: 19.5px;
  line-height: inherit;
  color: #333333;
  border: 0;
  border-bottom: 1px solid #e5e5e5;
}
label {
  display: inline-block;
  max-width: 100%;
  margin-bottom: 5px;
  font-weight: bold;
}
input[type="search"] {
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
}
input[type="radio"],
input[type="checkbox"] {
  margin: 4px 0 0;
  margin-top: 1px \9;
  line-height: normal;
}
input[type="file"] {
  display: block;
}
input[type="range"] {
  display: block;
  width: 100%;
}
select[multiple],
select[size] {
  height: auto;
}
input[type="file"]:focus,
input[type="radio"]:focus,
input[type="checkbox"]:focus {
  outline: 5px auto -webkit-focus-ring-color;
  outline-offset: -2px;
}
output {
  display: block;
  padding-top: 7px;
  font-size: 13px;
  line-height: 1.42857143;
  color: #555555;
}
.form-control {
  display: block;
  width: 100%;
  height: 32px;
  padding: 6px 12px;
  font-size: 13px;
  line-height: 1.42857143;
  color: #555555;
  background-color: #fff;
  background-image: none;
  border: 1px solid #ccc;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  -webkit-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  -o-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
}
.form-control:focus {
  border-color: #66afe9;
  outline: 0;
  -webkit-box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
  box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
}
.form-control::-moz-placeholder {
  color: #999;
  opacity: 1;
}
.form-control:-ms-input-placeholder {
  color: #999;
}
.form-control::-webkit-input-placeholder {
  color: #999;
}
.form-control::-ms-expand {
  border: 0;
  background-color: transparent;
}
.form-control[disabled],
.form-control[readonly],
fieldset[disabled] .form-control {
  background-color: #eeeeee;
  opacity: 1;
}
.form-control[disabled],
fieldset[disabled] .form-control {
  cursor: not-allowed;
}
textarea.form-control {
  height: auto;
}
input[type="search"] {
  -webkit-appearance: none;
}
@media screen and (-webkit-min-device-pixel-ratio: 0) {
  input[type="date"].form-control,
  input[type="time"].form-control,
  input[type="datetime-local"].form-control,
  input[type="month"].form-control {
    line-height: 32px;
  }
  input[type="date"].input-sm,
  input[type="time"].input-sm,
  input[type="datetime-local"].input-sm,
  input[type="month"].input-sm,
  .input-group-sm input[type="date"],
  .input-group-sm input[type="time"],
  .input-group-sm input[type="datetime-local"],
  .input-group-sm input[type="month"] {
    line-height: 30px;
  }
  input[type="date"].input-lg,
  input[type="time"].input-lg,
  input[type="datetime-local"].input-lg,
  input[type="month"].input-lg,
  .input-group-lg input[type="date"],
  .input-group-lg input[type="time"],
  .input-group-lg input[type="datetime-local"],
  .input-group-lg input[type="month"] {
    line-height: 45px;
  }
}
.form-group {
  margin-bottom: 15px;
}
.radio,
.checkbox {
  position: relative;
  display: block;
  margin-top: 10px;
  margin-bottom: 10px;
}
.radio label,
.checkbox label {
  min-height: 18px;
  padding-left: 20px;
  margin-bottom: 0;
  font-weight: normal;
  cursor: pointer;
}
.radio input[type="radio"],
.radio-inline input[type="radio"],
.checkbox input[type="checkbox"],
.checkbox-inline input[type="checkbox"] {
  position: absolute;
  margin-left: -20px;
  margin-top: 4px \9;
}
.radio + .radio,
.checkbox + .checkbox {
  margin-top: -5px;
}
.radio-inline,
.checkbox-inline {
  position: relative;
  display: inline-block;
  padding-left: 20px;
  margin-bottom: 0;
  vertical-align: middle;
  font-weight: normal;
  cursor: pointer;
}
.radio-inline + .radio-inline,
.checkbox-inline + .checkbox-inline {
  margin-top: 0;
  margin-left: 10px;
}
input[type="radio"][disabled],
input[type="checkbox"][disabled],
input[type="radio"].disabled,
input[type="checkbox"].disabled,
fieldset[disabled] input[type="radio"],
fieldset[disabled] input[type="checkbox"] {
  cursor: not-allowed;
}
.radio-inline.disabled,
.checkbox-inline.disabled,
fieldset[disabled] .radio-inline,
fieldset[disabled] .checkbox-inline {
  cursor: not-allowed;
}
.radio.disabled label,
.checkbox.disabled label,
fieldset[disabled] .radio label,
fieldset[disabled] .checkbox label {
  cursor: not-allowed;
}
.form-control-static {
  padding-top: 7px;
  padding-bottom: 7px;
  margin-bottom: 0;
  min-height: 31px;
}
.form-control-static.input-lg,
.form-control-static.input-sm {
  padding-left: 0;
  padding-right: 0;
}
.input-sm {
  height: 30px;
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
select.input-sm {
  height: 30px;
  line-height: 30px;
}
textarea.input-sm,
select[multiple].input-sm {
  height: auto;
}
.form-group-sm .form-control {
  height: 30px;
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
.form-group-sm select.form-control {
  height: 30px;
  line-height: 30px;
}
.form-group-sm textarea.form-control,
.form-group-sm select[multiple].form-control {
  height: auto;
}
.form-group-sm .form-control-static {
  height: 30px;
  min-height: 30px;
  padding: 6px 10px;
  font-size: 12px;
  line-height: 1.5;
}
.input-lg {
  height: 45px;
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
  border-radius: 3px;
}
select.input-lg {
  height: 45px;
  line-height: 45px;
}
textarea.input-lg,
select[multiple].input-lg {
  height: auto;
}
.form-group-lg .form-control {
  height: 45px;
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
  border-radius: 3px;
}
.form-group-lg select.form-control {
  height: 45px;
  line-height: 45px;
}
.form-group-lg textarea.form-control,
.form-group-lg select[multiple].form-control {
  height: auto;
}
.form-group-lg .form-control-static {
  height: 45px;
  min-height: 35px;
  padding: 11px 16px;
  font-size: 17px;
  line-height: 1.3333333;
}
.has-feedback {
  position: relative;
}
.has-feedback .form-control {
  padding-right: 40px;
}
.form-control-feedback {
  position: absolute;
  top: 0;
  right: 0;
  z-index: 2;
  display: block;
  width: 32px;
  height: 32px;
  line-height: 32px;
  text-align: center;
  pointer-events: none;
}
.input-lg + .form-control-feedback,
.input-group-lg + .form-control-feedback,
.form-group-lg .form-control + .form-control-feedback {
  width: 45px;
  height: 45px;
  line-height: 45px;
}
.input-sm + .form-control-feedback,
.input-group-sm + .form-control-feedback,
.form-group-sm .form-control + .form-control-feedback {
  width: 30px;
  height: 30px;
  line-height: 30px;
}
.has-success .help-block,
.has-success .control-label,
.has-success .radio,
.has-success .checkbox,
.has-success .radio-inline,
.has-success .checkbox-inline,
.has-success.radio label,
.has-success.checkbox label,
.has-success.radio-inline label,
.has-success.checkbox-inline label {
  color: #3c763d;
}
.has-success .form-control {
  border-color: #3c763d;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
}
.has-success .form-control:focus {
  border-color: #2b542c;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #67b168;
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #67b168;
}
.has-success .input-group-addon {
  color: #3c763d;
  border-color: #3c763d;
  background-color: #dff0d8;
}
.has-success .form-control-feedback {
  color: #3c763d;
}
.has-warning .help-block,
.has-warning .control-label,
.has-warning .radio,
.has-warning .checkbox,
.has-warning .radio-inline,
.has-warning .checkbox-inline,
.has-warning.radio label,
.has-warning.checkbox label,
.has-warning.radio-inline label,
.has-warning.checkbox-inline label {
  color: #8a6d3b;
}
.has-warning .form-control {
  border-color: #8a6d3b;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
}
.has-warning .form-control:focus {
  border-color: #66512c;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #c0a16b;
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #c0a16b;
}
.has-warning .input-group-addon {
  color: #8a6d3b;
  border-color: #8a6d3b;
  background-color: #fcf8e3;
}
.has-warning .form-control-feedback {
  color: #8a6d3b;
}
.has-error .help-block,
.has-error .control-label,
.has-error .radio,
.has-error .checkbox,
.has-error .radio-inline,
.has-error .checkbox-inline,
.has-error.radio label,
.has-error.checkbox label,
.has-error.radio-inline label,
.has-error.checkbox-inline label {
  color: #a94442;
}
.has-error .form-control {
  border-color: #a94442;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
}
.has-error .form-control:focus {
  border-color: #843534;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #ce8483;
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075), 0 0 6px #ce8483;
}
.has-error .input-group-addon {
  color: #a94442;
  border-color: #a94442;
  background-color: #f2dede;
}
.has-error .form-control-feedback {
  color: #a94442;
}
.has-feedback label ~ .form-control-feedback {
  top: 23px;
}
.has-feedback label.sr-only ~ .form-control-feedback {
  top: 0;
}
.help-block {
  display: block;
  margin-top: 5px;
  margin-bottom: 10px;
  color: #404040;
}
@media (min-width: 768px) {
  .form-inline .form-group {
    display: inline-block;
    margin-bottom: 0;
    vertical-align: middle;
  }
  .form-inline .form-control {
    display: inline-block;
    width: auto;
    vertical-align: middle;
  }
  .form-inline .form-control-static {
    display: inline-block;
  }
  .form-inline .input-group {
    display: inline-table;
    vertical-align: middle;
  }
  .form-inline .input-group .input-group-addon,
  .form-inline .input-group .input-group-btn,
  .form-inline .input-group .form-control {
    width: auto;
  }
  .form-inline .input-group > .form-control {
    width: 100%;
  }
  .form-inline .control-label {
    margin-bottom: 0;
    vertical-align: middle;
  }
  .form-inline .radio,
  .form-inline .checkbox {
    display: inline-block;
    margin-top: 0;
    margin-bottom: 0;
    vertical-align: middle;
  }
  .form-inline .radio label,
  .form-inline .checkbox label {
    padding-left: 0;
  }
  .form-inline .radio input[type="radio"],
  .form-inline .checkbox input[type="checkbox"] {
    position: relative;
    margin-left: 0;
  }
  .form-inline .has-feedback .form-control-feedback {
    top: 0;
  }
}
.form-horizontal .radio,
.form-horizontal .checkbox,
.form-horizontal .radio-inline,
.form-horizontal .checkbox-inline {
  margin-top: 0;
  margin-bottom: 0;
  padding-top: 7px;
}
.form-horizontal .radio,
.form-horizontal .checkbox {
  min-height: 25px;
}
.form-horizontal .form-group {
  margin-left: 0px;
  margin-right: 0px;
}
@media (min-width: 768px) {
  .form-horizontal .control-label {
    text-align: right;
    margin-bottom: 0;
    padding-top: 7px;
  }
}
.form-horizontal .has-feedback .form-control-feedback {
  right: 0px;
}
@media (min-width: 768px) {
  .form-horizontal .form-group-lg .control-label {
    padding-top: 11px;
    font-size: 17px;
  }
}
@media (min-width: 768px) {
  .form-horizontal .form-group-sm .control-label {
    padding-top: 6px;
    font-size: 12px;
  }
}
.btn {
  display: inline-block;
  margin-bottom: 0;
  font-weight: normal;
  text-align: center;
  vertical-align: middle;
  touch-action: manipulation;
  cursor: pointer;
  background-image: none;
  border: 1px solid transparent;
  white-space: nowrap;
  padding: 6px 12px;
  font-size: 13px;
  line-height: 1.42857143;
  border-radius: 2px;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}
.btn:focus,
.btn:active:focus,
.btn.active:focus,
.btn.focus,
.btn:active.focus,
.btn.active.focus {
  outline: 5px auto -webkit-focus-ring-color;
  outline-offset: -2px;
}
.btn:hover,
.btn:focus,
.btn.focus {
  color: #333;
  text-decoration: none;
}
.btn:active,
.btn.active {
  outline: 0;
  background-image: none;
  -webkit-box-shadow: inset 0 3px 5px rgba(0, 0, 0, 0.125);
  box-shadow: inset 0 3px 5px rgba(0, 0, 0, 0.125);
}
.btn.disabled,
.btn[disabled],
fieldset[disabled] .btn {
  cursor: not-allowed;
  opacity: 0.65;
  filter: alpha(opacity=65);
  -webkit-box-shadow: none;
  box-shadow: none;
}
a.btn.disabled,
fieldset[disabled] a.btn {
  pointer-events: none;
}
.btn-default {
  color: #333;
  background-color: #fff;
  border-color: #ccc;
}
.btn-default:focus,
.btn-default.focus {
  color: #333;
  background-color: #e6e6e6;
  border-color: #8c8c8c;
}
.btn-default:hover {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
.btn-default:active,
.btn-default.active,
.open > .dropdown-toggle.btn-default {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
.btn-default:active:hover,
.btn-default.active:hover,
.open > .dropdown-toggle.btn-default:hover,
.btn-default:active:focus,
.btn-default.active:focus,
.open > .dropdown-toggle.btn-default:focus,
.btn-default:active.focus,
.btn-default.active.focus,
.open > .dropdown-toggle.btn-default.focus {
  color: #333;
  background-color: #d4d4d4;
  border-color: #8c8c8c;
}
.btn-default:active,
.btn-default.active,
.open > .dropdown-toggle.btn-default {
  background-image: none;
}
.btn-default.disabled:hover,
.btn-default[disabled]:hover,
fieldset[disabled] .btn-default:hover,
.btn-default.disabled:focus,
.btn-default[disabled]:focus,
fieldset[disabled] .btn-default:focus,
.btn-default.disabled.focus,
.btn-default[disabled].focus,
fieldset[disabled] .btn-default.focus {
  background-color: #fff;
  border-color: #ccc;
}
.btn-default .badge {
  color: #fff;
  background-color: #333;
}
.btn-primary {
  color: #fff;
  background-color: #337ab7;
  border-color: #2e6da4;
}
.btn-primary:focus,
.btn-primary.focus {
  color: #fff;
  background-color: #286090;
  border-color: #122b40;
}
.btn-primary:hover {
  color: #fff;
  background-color: #286090;
  border-color: #204d74;
}
.btn-primary:active,
.btn-primary.active,
.open > .dropdown-toggle.btn-primary {
  color: #fff;
  background-color: #286090;
  border-color: #204d74;
}
.btn-primary:active:hover,
.btn-primary.active:hover,
.open > .dropdown-toggle.btn-primary:hover,
.btn-primary:active:focus,
.btn-primary.active:focus,
.open > .dropdown-toggle.btn-primary:focus,
.btn-primary:active.focus,
.btn-primary.active.focus,
.open > .dropdown-toggle.btn-primary.focus {
  color: #fff;
  background-color: #204d74;
  border-color: #122b40;
}
.btn-primary:active,
.btn-primary.active,
.open > .dropdown-toggle.btn-primary {
  background-image: none;
}
.btn-primary.disabled:hover,
.btn-primary[disabled]:hover,
fieldset[disabled] .btn-primary:hover,
.btn-primary.disabled:focus,
.btn-primary[disabled]:focus,
fieldset[disabled] .btn-primary:focus,
.btn-primary.disabled.focus,
.btn-primary[disabled].focus,
fieldset[disabled] .btn-primary.focus {
  background-color: #337ab7;
  border-color: #2e6da4;
}
.btn-primary .badge {
  color: #337ab7;
  background-color: #fff;
}
.btn-success {
  color: #fff;
  background-color: #5cb85c;
  border-color: #4cae4c;
}
.btn-success:focus,
.btn-success.focus {
  color: #fff;
  background-color: #449d44;
  border-color: #255625;
}
.btn-success:hover {
  color: #fff;
  background-color: #449d44;
  border-color: #398439;
}
.btn-success:active,
.btn-success.active,
.open > .dropdown-toggle.btn-success {
  color: #fff;
  background-color: #449d44;
  border-color: #398439;
}
.btn-success:active:hover,
.btn-success.active:hover,
.open > .dropdown-toggle.btn-success:hover,
.btn-success:active:focus,
.btn-success.active:focus,
.open > .dropdown-toggle.btn-success:focus,
.btn-success:active.focus,
.btn-success.active.focus,
.open > .dropdown-toggle.btn-success.focus {
  color: #fff;
  background-color: #398439;
  border-color: #255625;
}
.btn-success:active,
.btn-success.active,
.open > .dropdown-toggle.btn-success {
  background-image: none;
}
.btn-success.disabled:hover,
.btn-success[disabled]:hover,
fieldset[disabled] .btn-success:hover,
.btn-success.disabled:focus,
.btn-success[disabled]:focus,
fieldset[disabled] .btn-success:focus,
.btn-success.disabled.focus,
.btn-success[disabled].focus,
fieldset[disabled] .btn-success.focus {
  background-color: #5cb85c;
  border-color: #4cae4c;
}
.btn-success .badge {
  color: #5cb85c;
  background-color: #fff;
}
.btn-info {
  color: #fff;
  background-color: #5bc0de;
  border-color: #46b8da;
}
.btn-info:focus,
.btn-info.focus {
  color: #fff;
  background-color: #31b0d5;
  border-color: #1b6d85;
}
.btn-info:hover {
  color: #fff;
  background-color: #31b0d5;
  border-color: #269abc;
}
.btn-info:active,
.btn-info.active,
.open > .dropdown-toggle.btn-info {
  color: #fff;
  background-color: #31b0d5;
  border-color: #269abc;
}
.btn-info:active:hover,
.btn-info.active:hover,
.open > .dropdown-toggle.btn-info:hover,
.btn-info:active:focus,
.btn-info.active:focus,
.open > .dropdown-toggle.btn-info:focus,
.btn-info:active.focus,
.btn-info.active.focus,
.open > .dropdown-toggle.btn-info.focus {
  color: #fff;
  background-color: #269abc;
  border-color: #1b6d85;
}
.btn-info:active,
.btn-info.active,
.open > .dropdown-toggle.btn-info {
  background-image: none;
}
.btn-info.disabled:hover,
.btn-info[disabled]:hover,
fieldset[disabled] .btn-info:hover,
.btn-info.disabled:focus,
.btn-info[disabled]:focus,
fieldset[disabled] .btn-info:focus,
.btn-info.disabled.focus,
.btn-info[disabled].focus,
fieldset[disabled] .btn-info.focus {
  background-color: #5bc0de;
  border-color: #46b8da;
}
.btn-info .badge {
  color: #5bc0de;
  background-color: #fff;
}
.btn-warning {
  color: #fff;
  background-color: #f0ad4e;
  border-color: #eea236;
}
.btn-warning:focus,
.btn-warning.focus {
  color: #fff;
  background-color: #ec971f;
  border-color: #985f0d;
}
.btn-warning:hover {
  color: #fff;
  background-color: #ec971f;
  border-color: #d58512;
}
.btn-warning:active,
.btn-warning.active,
.open > .dropdown-toggle.btn-warning {
  color: #fff;
  background-color: #ec971f;
  border-color: #d58512;
}
.btn-warning:active:hover,
.btn-warning.active:hover,
.open > .dropdown-toggle.btn-warning:hover,
.btn-warning:active:focus,
.btn-warning.active:focus,
.open > .dropdown-toggle.btn-warning:focus,
.btn-warning:active.focus,
.btn-warning.active.focus,
.open > .dropdown-toggle.btn-warning.focus {
  color: #fff;
  background-color: #d58512;
  border-color: #985f0d;
}
.btn-warning:active,
.btn-warning.active,
.open > .dropdown-toggle.btn-warning {
  background-image: none;
}
.btn-warning.disabled:hover,
.btn-warning[disabled]:hover,
fieldset[disabled] .btn-warning:hover,
.btn-warning.disabled:focus,
.btn-warning[disabled]:focus,
fieldset[disabled] .btn-warning:focus,
.btn-warning.disabled.focus,
.btn-warning[disabled].focus,
fieldset[disabled] .btn-warning.focus {
  background-color: #f0ad4e;
  border-color: #eea236;
}
.btn-warning .badge {
  color: #f0ad4e;
  background-color: #fff;
}
.btn-danger {
  color: #fff;
  background-color: #d9534f;
  border-color: #d43f3a;
}
.btn-danger:focus,
.btn-danger.focus {
  color: #fff;
  background-color: #c9302c;
  border-color: #761c19;
}
.btn-danger:hover {
  color: #fff;
  background-color: #c9302c;
  border-color: #ac2925;
}
.btn-danger:active,
.btn-danger.active,
.open > .dropdown-toggle.btn-danger {
  color: #fff;
  background-color: #c9302c;
  border-color: #ac2925;
}
.btn-danger:active:hover,
.btn-danger.active:hover,
.open > .dropdown-toggle.btn-danger:hover,
.btn-danger:active:focus,
.btn-danger.active:focus,
.open > .dropdown-toggle.btn-danger:focus,
.btn-danger:active.focus,
.btn-danger.active.focus,
.open > .dropdown-toggle.btn-danger.focus {
  color: #fff;
  background-color: #ac2925;
  border-color: #761c19;
}
.btn-danger:active,
.btn-danger.active,
.open > .dropdown-toggle.btn-danger {
  background-image: none;
}
.btn-danger.disabled:hover,
.btn-danger[disabled]:hover,
fieldset[disabled] .btn-danger:hover,
.btn-danger.disabled:focus,
.btn-danger[disabled]:focus,
fieldset[disabled] .btn-danger:focus,
.btn-danger.disabled.focus,
.btn-danger[disabled].focus,
fieldset[disabled] .btn-danger.focus {
  background-color: #d9534f;
  border-color: #d43f3a;
}
.btn-danger .badge {
  color: #d9534f;
  background-color: #fff;
}
.btn-link {
  color: #337ab7;
  font-weight: normal;
  border-radius: 0;
}
.btn-link,
.btn-link:active,
.btn-link.active,
.btn-link[disabled],
fieldset[disabled] .btn-link {
  background-color: transparent;
  -webkit-box-shadow: none;
  box-shadow: none;
}
.btn-link,
.btn-link:hover,
.btn-link:focus,
.btn-link:active {
  border-color: transparent;
}
.btn-link:hover,
.btn-link:focus {
  color: #23527c;
  text-decoration: underline;
  background-color: transparent;
}
.btn-link[disabled]:hover,
fieldset[disabled] .btn-link:hover,
.btn-link[disabled]:focus,
fieldset[disabled] .btn-link:focus {
  color: #777777;
  text-decoration: none;
}
.btn-lg,
.btn-group-lg > .btn {
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
  border-radius: 3px;
}
.btn-sm,
.btn-group-sm > .btn {
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
.btn-xs,
.btn-group-xs > .btn {
  padding: 1px 5px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
.btn-block {
  display: block;
  width: 100%;
}
.btn-block + .btn-block {
  margin-top: 5px;
}
input[type="submit"].btn-block,
input[type="reset"].btn-block,
input[type="button"].btn-block {
  width: 100%;
}
.fade {
  opacity: 0;
  -webkit-transition: opacity 0.15s linear;
  -o-transition: opacity 0.15s linear;
  transition: opacity 0.15s linear;
}
.fade.in {
  opacity: 1;
}
.collapse {
  display: none;
}
.collapse.in {
  display: block;
}
tr.collapse.in {
  display: table-row;
}
tbody.collapse.in {
  display: table-row-group;
}
.collapsing {
  position: relative;
  height: 0;
  overflow: hidden;
  -webkit-transition-property: height, visibility;
  transition-property: height, visibility;
  -webkit-transition-duration: 0.35s;
  transition-duration: 0.35s;
  -webkit-transition-timing-function: ease;
  transition-timing-function: ease;
}
.caret {
  display: inline-block;
  width: 0;
  height: 0;
  margin-left: 2px;
  vertical-align: middle;
  border-top: 4px dashed;
  border-top: 4px solid \9;
  border-right: 4px solid transparent;
  border-left: 4px solid transparent;
}
.dropup,
.dropdown {
  position: relative;
}
.dropdown-toggle:focus {
  outline: 0;
}
.dropdown-menu {
  position: absolute;
  top: 100%;
  left: 0;
  z-index: 1000;
  display: none;
  float: left;
  min-width: 160px;
  padding: 5px 0;
  margin: 2px 0 0;
  list-style: none;
  font-size: 13px;
  text-align: left;
  background-color: #fff;
  border: 1px solid #ccc;
  border: 1px solid rgba(0, 0, 0, 0.15);
  border-radius: 2px;
  -webkit-box-shadow: 0 6px 12px rgba(0, 0, 0, 0.175);
  box-shadow: 0 6px 12px rgba(0, 0, 0, 0.175);
  background-clip: padding-box;
}
.dropdown-menu.pull-right {
  right: 0;
  left: auto;
}
.dropdown-menu .divider {
  height: 1px;
  margin: 8px 0;
  overflow: hidden;
  background-color: #e5e5e5;
}
.dropdown-menu > li > a {
  display: block;
  padding: 3px 20px;
  clear: both;
  font-weight: normal;
  line-height: 1.42857143;
  color: #333333;
  white-space: nowrap;
}
.dropdown-menu > li > a:hover,
.dropdown-menu > li > a:focus {
  text-decoration: none;
  color: #262626;
  background-color: #f5f5f5;
}
.dropdown-menu > .active > a,
.dropdown-menu > .active > a:hover,
.dropdown-menu > .active > a:focus {
  color: #fff;
  text-decoration: none;
  outline: 0;
  background-color: #337ab7;
}
.dropdown-menu > .disabled > a,
.dropdown-menu > .disabled > a:hover,
.dropdown-menu > .disabled > a:focus {
  color: #777777;
}
.dropdown-menu > .disabled > a:hover,
.dropdown-menu > .disabled > a:focus {
  text-decoration: none;
  background-color: transparent;
  background-image: none;
  filter: progid:DXImageTransform.Microsoft.gradient(enabled = false);
  cursor: not-allowed;
}
.open > .dropdown-menu {
  display: block;
}
.open > a {
  outline: 0;
}
.dropdown-menu-right {
  left: auto;
  right: 0;
}
.dropdown-menu-left {
  left: 0;
  right: auto;
}
.dropdown-header {
  display: block;
  padding: 3px 20px;
  font-size: 12px;
  line-height: 1.42857143;
  color: #777777;
  white-space: nowrap;
}
.dropdown-backdrop {
  position: fixed;
  left: 0;
  right: 0;
  bottom: 0;
  top: 0;
  z-index: 990;
}
.pull-right > .dropdown-menu {
  right: 0;
  left: auto;
}
.dropup .caret,
.navbar-fixed-bottom .dropdown .caret {
  border-top: 0;
  border-bottom: 4px dashed;
  border-bottom: 4px solid \9;
  content: "";
}
.dropup .dropdown-menu,
.navbar-fixed-bottom .dropdown .dropdown-menu {
  top: auto;
  bottom: 100%;
  margin-bottom: 2px;
}
@media (min-width: 541px) {
  .navbar-right .dropdown-menu {
    left: auto;
    right: 0;
  }
  .navbar-right .dropdown-menu-left {
    left: 0;
    right: auto;
  }
}
.btn-group,
.btn-group-vertical {
  position: relative;
  display: inline-block;
  vertical-align: middle;
}
.btn-group > .btn,
.btn-group-vertical > .btn {
  position: relative;
  float: left;
}
.btn-group > .btn:hover,
.btn-group-vertical > .btn:hover,
.btn-group > .btn:focus,
.btn-group-vertical > .btn:focus,
.btn-group > .btn:active,
.btn-group-vertical > .btn:active,
.btn-group > .btn.active,
.btn-group-vertical > .btn.active {
  z-index: 2;
}
.btn-group .btn + .btn,
.btn-group .btn + .btn-group,
.btn-group .btn-group + .btn,
.btn-group .btn-group + .btn-group {
  margin-left: -1px;
}
.btn-toolbar {
  margin-left: -5px;
}
.btn-toolbar .btn,
.btn-toolbar .btn-group,
.btn-toolbar .input-group {
  float: left;
}
.btn-toolbar > .btn,
.btn-toolbar > .btn-group,
.btn-toolbar > .input-group {
  margin-left: 5px;
}
.btn-group > .btn:not(:first-child):not(:last-child):not(.dropdown-toggle) {
  border-radius: 0;
}
.btn-group > .btn:first-child {
  margin-left: 0;
}
.btn-group > .btn:first-child:not(:last-child):not(.dropdown-toggle) {
  border-bottom-right-radius: 0;
  border-top-right-radius: 0;
}
.btn-group > .btn:last-child:not(:first-child),
.btn-group > .dropdown-toggle:not(:first-child) {
  border-bottom-left-radius: 0;
  border-top-left-radius: 0;
}
.btn-group > .btn-group {
  float: left;
}
.btn-group > .btn-group:not(:first-child):not(:last-child) > .btn {
  border-radius: 0;
}
.btn-group > .btn-group:first-child:not(:last-child) > .btn:last-child,
.btn-group > .btn-group:first-child:not(:last-child) > .dropdown-toggle {
  border-bottom-right-radius: 0;
  border-top-right-radius: 0;
}
.btn-group > .btn-group:last-child:not(:first-child) > .btn:first-child {
  border-bottom-left-radius: 0;
  border-top-left-radius: 0;
}
.btn-group .dropdown-toggle:active,
.btn-group.open .dropdown-toggle {
  outline: 0;
}
.btn-group > .btn + .dropdown-toggle {
  padding-left: 8px;
  padding-right: 8px;
}
.btn-group > .btn-lg + .dropdown-toggle {
  padding-left: 12px;
  padding-right: 12px;
}
.btn-group.open .dropdown-toggle {
  -webkit-box-shadow: inset 0 3px 5px rgba(0, 0, 0, 0.125);
  box-shadow: inset 0 3px 5px rgba(0, 0, 0, 0.125);
}
.btn-group.open .dropdown-toggle.btn-link {
  -webkit-box-shadow: none;
  box-shadow: none;
}
.btn .caret {
  margin-left: 0;
}
.btn-lg .caret {
  border-width: 5px 5px 0;
  border-bottom-width: 0;
}
.dropup .btn-lg .caret {
  border-width: 0 5px 5px;
}
.btn-group-vertical > .btn,
.btn-group-vertical > .btn-group,
.btn-group-vertical > .btn-group > .btn {
  display: block;
  float: none;
  width: 100%;
  max-width: 100%;
}
.btn-group-vertical > .btn-group > .btn {
  float: none;
}
.btn-group-vertical > .btn + .btn,
.btn-group-vertical > .btn + .btn-group,
.btn-group-vertical > .btn-group + .btn,
.btn-group-vertical > .btn-group + .btn-group {
  margin-top: -1px;
  margin-left: 0;
}
.btn-group-vertical > .btn:not(:first-child):not(:last-child) {
  border-radius: 0;
}
.btn-group-vertical > .btn:first-child:not(:last-child) {
  border-top-right-radius: 2px;
  border-top-left-radius: 2px;
  border-bottom-right-radius: 0;
  border-bottom-left-radius: 0;
}
.btn-group-vertical > .btn:last-child:not(:first-child) {
  border-top-right-radius: 0;
  border-top-left-radius: 0;
  border-bottom-right-radius: 2px;
  border-bottom-left-radius: 2px;
}
.btn-group-vertical > .btn-group:not(:first-child):not(:last-child) > .btn {
  border-radius: 0;
}
.btn-group-vertical > .btn-group:first-child:not(:last-child) > .btn:last-child,
.btn-group-vertical > .btn-group:first-child:not(:last-child) > .dropdown-toggle {
  border-bottom-right-radius: 0;
  border-bottom-left-radius: 0;
}
.btn-group-vertical > .btn-group:last-child:not(:first-child) > .btn:first-child {
  border-top-right-radius: 0;
  border-top-left-radius: 0;
}
.btn-group-justified {
  display: table;
  width: 100%;
  table-layout: fixed;
  border-collapse: separate;
}
.btn-group-justified > .btn,
.btn-group-justified > .btn-group {
  float: none;
  display: table-cell;
  width: 1%;
}
.btn-group-justified > .btn-group .btn {
  width: 100%;
}
.btn-group-justified > .btn-group .dropdown-menu {
  left: auto;
}
[data-toggle="buttons"] > .btn input[type="radio"],
[data-toggle="buttons"] > .btn-group > .btn input[type="radio"],
[data-toggle="buttons"] > .btn input[type="checkbox"],
[data-toggle="buttons"] > .btn-group > .btn input[type="checkbox"] {
  position: absolute;
  clip: rect(0, 0, 0, 0);
  pointer-events: none;
}
.input-group {
  position: relative;
  display: table;
  border-collapse: separate;
}
.input-group[class*="col-"] {
  float: none;
  padding-left: 0;
  padding-right: 0;
}
.input-group .form-control {
  position: relative;
  z-index: 2;
  float: left;
  width: 100%;
  margin-bottom: 0;
}
.input-group .form-control:focus {
  z-index: 3;
}
.input-group-lg > .form-control,
.input-group-lg > .input-group-addon,
.input-group-lg > .input-group-btn > .btn {
  height: 45px;
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
  border-radius: 3px;
}
select.input-group-lg > .form-control,
select.input-group-lg > .input-group-addon,
select.input-group-lg > .input-group-btn > .btn {
  height: 45px;
  line-height: 45px;
}
textarea.input-group-lg > .form-control,
textarea.input-group-lg > .input-group-addon,
textarea.input-group-lg > .input-group-btn > .btn,
select[multiple].input-group-lg > .form-control,
select[multiple].input-group-lg > .input-group-addon,
select[multiple].input-group-lg > .input-group-btn > .btn {
  height: auto;
}
.input-group-sm > .form-control,
.input-group-sm > .input-group-addon,
.input-group-sm > .input-group-btn > .btn {
  height: 30px;
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
}
select.input-group-sm > .form-control,
select.input-group-sm > .input-group-addon,
select.input-group-sm > .input-group-btn > .btn {
  height: 30px;
  line-height: 30px;
}
textarea.input-group-sm > .form-control,
textarea.input-group-sm > .input-group-addon,
textarea.input-group-sm > .input-group-btn > .btn,
select[multiple].input-group-sm > .form-control,
select[multiple].input-group-sm > .input-group-addon,
select[multiple].input-group-sm > .input-group-btn > .btn {
  height: auto;
}
.input-group-addon,
.input-group-btn,
.input-group .form-control {
  display: table-cell;
}
.input-group-addon:not(:first-child):not(:last-child),
.input-group-btn:not(:first-child):not(:last-child),
.input-group .form-control:not(:first-child):not(:last-child) {
  border-radius: 0;
}
.input-group-addon,
.input-group-btn {
  width: 1%;
  white-space: nowrap;
  vertical-align: middle;
}
.input-group-addon {
  padding: 6px 12px;
  font-size: 13px;
  font-weight: normal;
  line-height: 1;
  color: #555555;
  text-align: center;
  background-color: #eeeeee;
  border: 1px solid #ccc;
  border-radius: 2px;
}
.input-group-addon.input-sm {
  padding: 5px 10px;
  font-size: 12px;
  border-radius: 1px;
}
.input-group-addon.input-lg {
  padding: 10px 16px;
  font-size: 17px;
  border-radius: 3px;
}
.input-group-addon input[type="radio"],
.input-group-addon input[type="checkbox"] {
  margin-top: 0;
}
.input-group .form-control:first-child,
.input-group-addon:first-child,
.input-group-btn:first-child > .btn,
.input-group-btn:first-child > .btn-group > .btn,
.input-group-btn:first-child > .dropdown-toggle,
.input-group-btn:last-child > .btn:not(:last-child):not(.dropdown-toggle),
.input-group-btn:last-child > .btn-group:not(:last-child) > .btn {
  border-bottom-right-radius: 0;
  border-top-right-radius: 0;
}
.input-group-addon:first-child {
  border-right: 0;
}
.input-group .form-control:last-child,
.input-group-addon:last-child,
.input-group-btn:last-child > .btn,
.input-group-btn:last-child > .btn-group > .btn,
.input-group-btn:last-child > .dropdown-toggle,
.input-group-btn:first-child > .btn:not(:first-child),
.input-group-btn:first-child > .btn-group:not(:first-child) > .btn {
  border-bottom-left-radius: 0;
  border-top-left-radius: 0;
}
.input-group-addon:last-child {
  border-left: 0;
}
.input-group-btn {
  position: relative;
  font-size: 0;
  white-space: nowrap;
}
.input-group-btn > .btn {
  position: relative;
}
.input-group-btn > .btn + .btn {
  margin-left: -1px;
}
.input-group-btn > .btn:hover,
.input-group-btn > .btn:focus,
.input-group-btn > .btn:active {
  z-index: 2;
}
.input-group-btn:first-child > .btn,
.input-group-btn:first-child > .btn-group {
  margin-right: -1px;
}
.input-group-btn:last-child > .btn,
.input-group-btn:last-child > .btn-group {
  z-index: 2;
  margin-left: -1px;
}
.nav {
  margin-bottom: 0;
  padding-left: 0;
  list-style: none;
}
.nav > li {
  position: relative;
  display: block;
}
.nav > li > a {
  position: relative;
  display: block;
  padding: 10px 15px;
}
.nav > li > a:hover,
.nav > li > a:focus {
  text-decoration: none;
  background-color: #eeeeee;
}
.nav > li.disabled > a {
  color: #777777;
}
.nav > li.disabled > a:hover,
.nav > li.disabled > a:focus {
  color: #777777;
  text-decoration: none;
  background-color: transparent;
  cursor: not-allowed;
}
.nav .open > a,
.nav .open > a:hover,
.nav .open > a:focus {
  background-color: #eeeeee;
  border-color: #337ab7;
}
.nav .nav-divider {
  height: 1px;
  margin: 8px 0;
  overflow: hidden;
  background-color: #e5e5e5;
}
.nav > li > a > img {
  max-width: none;
}
.nav-tabs {
  border-bottom: 1px solid #ddd;
}
.nav-tabs > li {
  float: left;
  margin-bottom: -1px;
}
.nav-tabs > li > a {
  margin-right: 2px;
  line-height: 1.42857143;
  border: 1px solid transparent;
  border-radius: 2px 2px 0 0;
}
.nav-tabs > li > a:hover {
  border-color: #eeeeee #eeeeee #ddd;
}
.nav-tabs > li.active > a,
.nav-tabs > li.active > a:hover,
.nav-tabs > li.active > a:focus {
  color: #555555;
  background-color: #fff;
  border: 1px solid #ddd;
  border-bottom-color: transparent;
  cursor: default;
}
.nav-tabs.nav-justified {
  width: 100%;
  border-bottom: 0;
}
.nav-tabs.nav-justified > li {
  float: none;
}
.nav-tabs.nav-justified > li > a {
  text-align: center;
  margin-bottom: 5px;
}
.nav-tabs.nav-justified > .dropdown .dropdown-menu {
  top: auto;
  left: auto;
}
@media (min-width: 768px) {
  .nav-tabs.nav-justified > li {
    display: table-cell;
    width: 1%;
  }
  .nav-tabs.nav-justified > li > a {
    margin-bottom: 0;
  }
}
.nav-tabs.nav-justified > li > a {
  margin-right: 0;
  border-radius: 2px;
}
.nav-tabs.nav-justified > .active > a,
.nav-tabs.nav-justified > .active > a:hover,
.nav-tabs.nav-justified > .active > a:focus {
  border: 1px solid #ddd;
}
@media (min-width: 768px) {
  .nav-tabs.nav-justified > li > a {
    border-bottom: 1px solid #ddd;
    border-radius: 2px 2px 0 0;
  }
  .nav-tabs.nav-justified > .active > a,
  .nav-tabs.nav-justified > .active > a:hover,
  .nav-tabs.nav-justified > .active > a:focus {
    border-bottom-color: #fff;
  }
}
.nav-pills > li {
  float: left;
}
.nav-pills > li > a {
  border-radius: 2px;
}
.nav-pills > li + li {
  margin-left: 2px;
}
.nav-pills > li.active > a,
.nav-pills > li.active > a:hover,
.nav-pills > li.active > a:focus {
  color: #fff;
  background-color: #337ab7;
}
.nav-stacked > li {
  float: none;
}
.nav-stacked > li + li {
  margin-top: 2px;
  margin-left: 0;
}
.nav-justified {
  width: 100%;
}
.nav-justified > li {
  float: none;
}
.nav-justified > li > a {
  text-align: center;
  margin-bottom: 5px;
}
.nav-justified > .dropdown .dropdown-menu {
  top: auto;
  left: auto;
}
@media (min-width: 768px) {
  .nav-justified > li {
    display: table-cell;
    width: 1%;
  }
  .nav-justified > li > a {
    margin-bottom: 0;
  }
}
.nav-tabs-justified {
  border-bottom: 0;
}
.nav-tabs-justified > li > a {
  margin-right: 0;
  border-radius: 2px;
}
.nav-tabs-justified > .active > a,
.nav-tabs-justified > .active > a:hover,
.nav-tabs-justified > .active > a:focus {
  border: 1px solid #ddd;
}
@media (min-width: 768px) {
  .nav-tabs-justified > li > a {
    border-bottom: 1px solid #ddd;
    border-radius: 2px 2px 0 0;
  }
  .nav-tabs-justified > .active > a,
  .nav-tabs-justified > .active > a:hover,
  .nav-tabs-justified > .active > a:focus {
    border-bottom-color: #fff;
  }
}
.tab-content > .tab-pane {
  display: none;
}
.tab-content > .active {
  display: block;
}
.nav-tabs .dropdown-menu {
  margin-top: -1px;
  border-top-right-radius: 0;
  border-top-left-radius: 0;
}
.navbar {
  position: relative;
  min-height: 30px;
  margin-bottom: 18px;
  border: 1px solid transparent;
}
@media (min-width: 541px) {
  .navbar {
    border-radius: 2px;
  }
}
@media (min-width: 541px) {
  .navbar-header {
    float: left;
  }
}
.navbar-collapse {
  overflow-x: visible;
  padding-right: 0px;
  padding-left: 0px;
  border-top: 1px solid transparent;
  box-shadow: inset 0 1px 0 rgba(255, 255, 255, 0.1);
  -webkit-overflow-scrolling: touch;
}
.navbar-collapse.in {
  overflow-y: auto;
}
@media (min-width: 541px) {
  .navbar-collapse {
    width: auto;
    border-top: 0;
    box-shadow: none;
  }
  .navbar-collapse.collapse {
    display: block !important;
    height: auto !important;
    padding-bottom: 0;
    overflow: visible !important;
  }
  .navbar-collapse.in {
    overflow-y: visible;
  }
  .navbar-fixed-top .navbar-collapse,
  .navbar-static-top .navbar-collapse,
  .navbar-fixed-bottom .navbar-collapse {
    padding-left: 0;
    padding-right: 0;
  }
}
.navbar-fixed-top .navbar-collapse,
.navbar-fixed-bottom .navbar-collapse {
  max-height: 340px;
}
@media (max-device-width: 540px) and (orientation: landscape) {
  .navbar-fixed-top .navbar-collapse,
  .navbar-fixed-bottom .navbar-collapse {
    max-height: 200px;
  }
}
.container > .navbar-header,
.container-fluid > .navbar-header,
.container > .navbar-collapse,
.container-fluid > .navbar-collapse {
  margin-right: 0px;
  margin-left: 0px;
}
@media (min-width: 541px) {
  .container > .navbar-header,
  .container-fluid > .navbar-header,
  .container > .navbar-collapse,
  .container-fluid > .navbar-collapse {
    margin-right: 0;
    margin-left: 0;
  }
}
.navbar-static-top {
  z-index: 1000;
  border-width: 0 0 1px;
}
@media (min-width: 541px) {
  .navbar-static-top {
    border-radius: 0;
  }
}
.navbar-fixed-top,
.navbar-fixed-bottom {
  position: fixed;
  right: 0;
  left: 0;
  z-index: 1030;
}
@media (min-width: 541px) {
  .navbar-fixed-top,
  .navbar-fixed-bottom {
    border-radius: 0;
  }
}
.navbar-fixed-top {
  top: 0;
  border-width: 0 0 1px;
}
.navbar-fixed-bottom {
  bottom: 0;
  margin-bottom: 0;
  border-width: 1px 0 0;
}
.navbar-brand {
  float: left;
  padding: 6px 0px;
  font-size: 17px;
  line-height: 18px;
  height: 30px;
}
.navbar-brand:hover,
.navbar-brand:focus {
  text-decoration: none;
}
.navbar-brand > img {
  display: block;
}
@media (min-width: 541px) {
  .navbar > .container .navbar-brand,
  .navbar > .container-fluid .navbar-brand {
    margin-left: 0px;
  }
}
.navbar-toggle {
  position: relative;
  float: right;
  margin-right: 0px;
  padding: 9px 10px;
  margin-top: -2px;
  margin-bottom: -2px;
  background-color: transparent;
  background-image: none;
  border: 1px solid transparent;
  border-radius: 2px;
}
.navbar-toggle:focus {
  outline: 0;
}
.navbar-toggle .icon-bar {
  display: block;
  width: 22px;
  height: 2px;
  border-radius: 1px;
}
.navbar-toggle .icon-bar + .icon-bar {
  margin-top: 4px;
}
@media (min-width: 541px) {
  .navbar-toggle {
    display: none;
  }
}
.navbar-nav {
  margin: 3px 0px;
}
.navbar-nav > li > a {
  padding-top: 10px;
  padding-bottom: 10px;
  line-height: 18px;
}
@media (max-width: 540px) {
  .navbar-nav .open .dropdown-menu {
    position: static;
    float: none;
    width: auto;
    margin-top: 0;
    background-color: transparent;
    border: 0;
    box-shadow: none;
  }
  .navbar-nav .open .dropdown-menu > li > a,
  .navbar-nav .open .dropdown-menu .dropdown-header {
    padding: 5px 15px 5px 25px;
  }
  .navbar-nav .open .dropdown-menu > li > a {
    line-height: 18px;
  }
  .navbar-nav .open .dropdown-menu > li > a:hover,
  .navbar-nav .open .dropdown-menu > li > a:focus {
    background-image: none;
  }
}
@media (min-width: 541px) {
  .navbar-nav {
    float: left;
    margin: 0;
  }
  .navbar-nav > li {
    float: left;
  }
  .navbar-nav > li > a {
    padding-top: 6px;
    padding-bottom: 6px;
  }
}
.navbar-form {
  margin-left: 0px;
  margin-right: 0px;
  padding: 10px 0px;
  border-top: 1px solid transparent;
  border-bottom: 1px solid transparent;
  -webkit-box-shadow: inset 0 1px 0 rgba(255, 255, 255, 0.1), 0 1px 0 rgba(255, 255, 255, 0.1);
  box-shadow: inset 0 1px 0 rgba(255, 255, 255, 0.1), 0 1px 0 rgba(255, 255, 255, 0.1);
  margin-top: -1px;
  margin-bottom: -1px;
}
@media (min-width: 768px) {
  .navbar-form .form-group {
    display: inline-block;
    margin-bottom: 0;
    vertical-align: middle;
  }
  .navbar-form .form-control {
    display: inline-block;
    width: auto;
    vertical-align: middle;
  }
  .navbar-form .form-control-static {
    display: inline-block;
  }
  .navbar-form .input-group {
    display: inline-table;
    vertical-align: middle;
  }
  .navbar-form .input-group .input-group-addon,
  .navbar-form .input-group .input-group-btn,
  .navbar-form .input-group .form-control {
    width: auto;
  }
  .navbar-form .input-group > .form-control {
    width: 100%;
  }
  .navbar-form .control-label {
    margin-bottom: 0;
    vertical-align: middle;
  }
  .navbar-form .radio,
  .navbar-form .checkbox {
    display: inline-block;
    margin-top: 0;
    margin-bottom: 0;
    vertical-align: middle;
  }
  .navbar-form .radio label,
  .navbar-form .checkbox label {
    padding-left: 0;
  }
  .navbar-form .radio input[type="radio"],
  .navbar-form .checkbox input[type="checkbox"] {
    position: relative;
    margin-left: 0;
  }
  .navbar-form .has-feedback .form-control-feedback {
    top: 0;
  }
}
@media (max-width: 540px) {
  .navbar-form .form-group {
    margin-bottom: 5px;
  }
  .navbar-form .form-group:last-child {
    margin-bottom: 0;
  }
}
@media (min-width: 541px) {
  .navbar-form {
    width: auto;
    border: 0;
    margin-left: 0;
    margin-right: 0;
    padding-top: 0;
    padding-bottom: 0;
    -webkit-box-shadow: none;
    box-shadow: none;
  }
}
.navbar-nav > li > .dropdown-menu {
  margin-top: 0;
  border-top-right-radius: 0;
  border-top-left-radius: 0;
}
.navbar-fixed-bottom .navbar-nav > li > .dropdown-menu {
  margin-bottom: 0;
  border-top-right-radius: 2px;
  border-top-left-radius: 2px;
  border-bottom-right-radius: 0;
  border-bottom-left-radius: 0;
}
.navbar-btn {
  margin-top: -1px;
  margin-bottom: -1px;
}
.navbar-btn.btn-sm {
  margin-top: 0px;
  margin-bottom: 0px;
}
.navbar-btn.btn-xs {
  margin-top: 4px;
  margin-bottom: 4px;
}
.navbar-text {
  margin-top: 6px;
  margin-bottom: 6px;
}
@media (min-width: 541px) {
  .navbar-text {
    float: left;
    margin-left: 0px;
    margin-right: 0px;
  }
}
@media (min-width: 541px) {
  .navbar-left {
    float: left !important;
    float: left;
  }
  .navbar-right {
    float: right !important;
    float: right;
    margin-right: 0px;
  }
  .navbar-right ~ .navbar-right {
    margin-right: 0;
  }
}
.navbar-default {
  background-color: #f8f8f8;
  border-color: #e7e7e7;
}
.navbar-default .navbar-brand {
  color: #777;
}
.navbar-default .navbar-brand:hover,
.navbar-default .navbar-brand:focus {
  color: #5e5e5e;
  background-color: transparent;
}
.navbar-default .navbar-text {
  color: #777;
}
.navbar-default .navbar-nav > li > a {
  color: #777;
}
.navbar-default .navbar-nav > li > a:hover,
.navbar-default .navbar-nav > li > a:focus {
  color: #333;
  background-color: transparent;
}
.navbar-default .navbar-nav > .active > a,
.navbar-default .navbar-nav > .active > a:hover,
.navbar-default .navbar-nav > .active > a:focus {
  color: #555;
  background-color: #e7e7e7;
}
.navbar-default .navbar-nav > .disabled > a,
.navbar-default .navbar-nav > .disabled > a:hover,
.navbar-default .navbar-nav > .disabled > a:focus {
  color: #ccc;
  background-color: transparent;
}
.navbar-default .navbar-toggle {
  border-color: #ddd;
}
.navbar-default .navbar-toggle:hover,
.navbar-default .navbar-toggle:focus {
  background-color: #ddd;
}
.navbar-default .navbar-toggle .icon-bar {
  background-color: #888;
}
.navbar-default .navbar-collapse,
.navbar-default .navbar-form {
  border-color: #e7e7e7;
}
.navbar-default .navbar-nav > .open > a,
.navbar-default .navbar-nav > .open > a:hover,
.navbar-default .navbar-nav > .open > a:focus {
  background-color: #e7e7e7;
  color: #555;
}
@media (max-width: 540px) {
  .navbar-default .navbar-nav .open .dropdown-menu > li > a {
    color: #777;
  }
  .navbar-default .navbar-nav .open .dropdown-menu > li > a:hover,
  .navbar-default .navbar-nav .open .dropdown-menu > li > a:focus {
    color: #333;
    background-color: transparent;
  }
  .navbar-default .navbar-nav .open .dropdown-menu > .active > a,
  .navbar-default .navbar-nav .open .dropdown-menu > .active > a:hover,
  .navbar-default .navbar-nav .open .dropdown-menu > .active > a:focus {
    color: #555;
    background-color: #e7e7e7;
  }
  .navbar-default .navbar-nav .open .dropdown-menu > .disabled > a,
  .navbar-default .navbar-nav .open .dropdown-menu > .disabled > a:hover,
  .navbar-default .navbar-nav .open .dropdown-menu > .disabled > a:focus {
    color: #ccc;
    background-color: transparent;
  }
}
.navbar-default .navbar-link {
  color: #777;
}
.navbar-default .navbar-link:hover {
  color: #333;
}
.navbar-default .btn-link {
  color: #777;
}
.navbar-default .btn-link:hover,
.navbar-default .btn-link:focus {
  color: #333;
}
.navbar-default .btn-link[disabled]:hover,
fieldset[disabled] .navbar-default .btn-link:hover,
.navbar-default .btn-link[disabled]:focus,
fieldset[disabled] .navbar-default .btn-link:focus {
  color: #ccc;
}
.navbar-inverse {
  background-color: #222;
  border-color: #080808;
}
.navbar-inverse .navbar-brand {
  color: #9d9d9d;
}
.navbar-inverse .navbar-brand:hover,
.navbar-inverse .navbar-brand:focus {
  color: #fff;
  background-color: transparent;
}
.navbar-inverse .navbar-text {
  color: #9d9d9d;
}
.navbar-inverse .navbar-nav > li > a {
  color: #9d9d9d;
}
.navbar-inverse .navbar-nav > li > a:hover,
.navbar-inverse .navbar-nav > li > a:focus {
  color: #fff;
  background-color: transparent;
}
.navbar-inverse .navbar-nav > .active > a,
.navbar-inverse .navbar-nav > .active > a:hover,
.navbar-inverse .navbar-nav > .active > a:focus {
  color: #fff;
  background-color: #080808;
}
.navbar-inverse .navbar-nav > .disabled > a,
.navbar-inverse .navbar-nav > .disabled > a:hover,
.navbar-inverse .navbar-nav > .disabled > a:focus {
  color: #444;
  background-color: transparent;
}
.navbar-inverse .navbar-toggle {
  border-color: #333;
}
.navbar-inverse .navbar-toggle:hover,
.navbar-inverse .navbar-toggle:focus {
  background-color: #333;
}
.navbar-inverse .navbar-toggle .icon-bar {
  background-color: #fff;
}
.navbar-inverse .navbar-collapse,
.navbar-inverse .navbar-form {
  border-color: #101010;
}
.navbar-inverse .navbar-nav > .open > a,
.navbar-inverse .navbar-nav > .open > a:hover,
.navbar-inverse .navbar-nav > .open > a:focus {
  background-color: #080808;
  color: #fff;
}
@media (max-width: 540px) {
  .navbar-inverse .navbar-nav .open .dropdown-menu > .dropdown-header {
    border-color: #080808;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu .divider {
    background-color: #080808;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu > li > a {
    color: #9d9d9d;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu > li > a:hover,
  .navbar-inverse .navbar-nav .open .dropdown-menu > li > a:focus {
    color: #fff;
    background-color: transparent;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu > .active > a,
  .navbar-inverse .navbar-nav .open .dropdown-menu > .active > a:hover,
  .navbar-inverse .navbar-nav .open .dropdown-menu > .active > a:focus {
    color: #fff;
    background-color: #080808;
  }
  .navbar-inverse .navbar-nav .open .dropdown-menu > .disabled > a,
  .navbar-inverse .navbar-nav .open .dropdown-menu > .disabled > a:hover,
  .navbar-inverse .navbar-nav .open .dropdown-menu > .disabled > a:focus {
    color: #444;
    background-color: transparent;
  }
}
.navbar-inverse .navbar-link {
  color: #9d9d9d;
}
.navbar-inverse .navbar-link:hover {
  color: #fff;
}
.navbar-inverse .btn-link {
  color: #9d9d9d;
}
.navbar-inverse .btn-link:hover,
.navbar-inverse .btn-link:focus {
  color: #fff;
}
.navbar-inverse .btn-link[disabled]:hover,
fieldset[disabled] .navbar-inverse .btn-link:hover,
.navbar-inverse .btn-link[disabled]:focus,
fieldset[disabled] .navbar-inverse .btn-link:focus {
  color: #444;
}
.breadcrumb {
  padding: 8px 15px;
  margin-bottom: 18px;
  list-style: none;
  background-color: #f5f5f5;
  border-radius: 2px;
}
.breadcrumb > li {
  display: inline-block;
}
.breadcrumb > li + li:before {
  content: "/\00a0";
  padding: 0 5px;
  color: #5e5e5e;
}
.breadcrumb > .active {
  color: #777777;
}
.pagination {
  display: inline-block;
  padding-left: 0;
  margin: 18px 0;
  border-radius: 2px;
}
.pagination > li {
  display: inline;
}
.pagination > li > a,
.pagination > li > span {
  position: relative;
  float: left;
  padding: 6px 12px;
  line-height: 1.42857143;
  text-decoration: none;
  color: #337ab7;
  background-color: #fff;
  border: 1px solid #ddd;
  margin-left: -1px;
}
.pagination > li:first-child > a,
.pagination > li:first-child > span {
  margin-left: 0;
  border-bottom-left-radius: 2px;
  border-top-left-radius: 2px;
}
.pagination > li:last-child > a,
.pagination > li:last-child > span {
  border-bottom-right-radius: 2px;
  border-top-right-radius: 2px;
}
.pagination > li > a:hover,
.pagination > li > span:hover,
.pagination > li > a:focus,
.pagination > li > span:focus {
  z-index: 2;
  color: #23527c;
  background-color: #eeeeee;
  border-color: #ddd;
}
.pagination > .active > a,
.pagination > .active > span,
.pagination > .active > a:hover,
.pagination > .active > span:hover,
.pagination > .active > a:focus,
.pagination > .active > span:focus {
  z-index: 3;
  color: #fff;
  background-color: #337ab7;
  border-color: #337ab7;
  cursor: default;
}
.pagination > .disabled > span,
.pagination > .disabled > span:hover,
.pagination > .disabled > span:focus,
.pagination > .disabled > a,
.pagination > .disabled > a:hover,
.pagination > .disabled > a:focus {
  color: #777777;
  background-color: #fff;
  border-color: #ddd;
  cursor: not-allowed;
}
.pagination-lg > li > a,
.pagination-lg > li > span {
  padding: 10px 16px;
  font-size: 17px;
  line-height: 1.3333333;
}
.pagination-lg > li:first-child > a,
.pagination-lg > li:first-child > span {
  border-bottom-left-radius: 3px;
  border-top-left-radius: 3px;
}
.pagination-lg > li:last-child > a,
.pagination-lg > li:last-child > span {
  border-bottom-right-radius: 3px;
  border-top-right-radius: 3px;
}
.pagination-sm > li > a,
.pagination-sm > li > span {
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
}
.pagination-sm > li:first-child > a,
.pagination-sm > li:first-child > span {
  border-bottom-left-radius: 1px;
  border-top-left-radius: 1px;
}
.pagination-sm > li:last-child > a,
.pagination-sm > li:last-child > span {
  border-bottom-right-radius: 1px;
  border-top-right-radius: 1px;
}
.pager {
  padding-left: 0;
  margin: 18px 0;
  list-style: none;
  text-align: center;
}
.pager li {
  display: inline;
}
.pager li > a,
.pager li > span {
  display: inline-block;
  padding: 5px 14px;
  background-color: #fff;
  border: 1px solid #ddd;
  border-radius: 15px;
}
.pager li > a:hover,
.pager li > a:focus {
  text-decoration: none;
  background-color: #eeeeee;
}
.pager .next > a,
.pager .next > span {
  float: right;
}
.pager .previous > a,
.pager .previous > span {
  float: left;
}
.pager .disabled > a,
.pager .disabled > a:hover,
.pager .disabled > a:focus,
.pager .disabled > span {
  color: #777777;
  background-color: #fff;
  cursor: not-allowed;
}
.label {
  display: inline;
  padding: .2em .6em .3em;
  font-size: 75%;
  font-weight: bold;
  line-height: 1;
  color: #fff;
  text-align: center;
  white-space: nowrap;
  vertical-align: baseline;
  border-radius: .25em;
}
a.label:hover,
a.label:focus {
  color: #fff;
  text-decoration: none;
  cursor: pointer;
}
.label:empty {
  display: none;
}
.btn .label {
  position: relative;
  top: -1px;
}
.label-default {
  background-color: #777777;
}
.label-default[href]:hover,
.label-default[href]:focus {
  background-color: #5e5e5e;
}
.label-primary {
  background-color: #337ab7;
}
.label-primary[href]:hover,
.label-primary[href]:focus {
  background-color: #286090;
}
.label-success {
  background-color: #5cb85c;
}
.label-success[href]:hover,
.label-success[href]:focus {
  background-color: #449d44;
}
.label-info {
  background-color: #5bc0de;
}
.label-info[href]:hover,
.label-info[href]:focus {
  background-color: #31b0d5;
}
.label-warning {
  background-color: #f0ad4e;
}
.label-warning[href]:hover,
.label-warning[href]:focus {
  background-color: #ec971f;
}
.label-danger {
  background-color: #d9534f;
}
.label-danger[href]:hover,
.label-danger[href]:focus {
  background-color: #c9302c;
}
.badge {
  display: inline-block;
  min-width: 10px;
  padding: 3px 7px;
  font-size: 12px;
  font-weight: bold;
  color: #fff;
  line-height: 1;
  vertical-align: middle;
  white-space: nowrap;
  text-align: center;
  background-color: #777777;
  border-radius: 10px;
}
.badge:empty {
  display: none;
}
.btn .badge {
  position: relative;
  top: -1px;
}
.btn-xs .badge,
.btn-group-xs > .btn .badge {
  top: 0;
  padding: 1px 5px;
}
a.badge:hover,
a.badge:focus {
  color: #fff;
  text-decoration: none;
  cursor: pointer;
}
.list-group-item.active > .badge,
.nav-pills > .active > a > .badge {
  color: #337ab7;
  background-color: #fff;
}
.list-group-item > .badge {
  float: right;
}
.list-group-item > .badge + .badge {
  margin-right: 5px;
}
.nav-pills > li > a > .badge {
  margin-left: 3px;
}
.jumbotron {
  padding-top: 30px;
  padding-bottom: 30px;
  margin-bottom: 30px;
  color: inherit;
  background-color: #eeeeee;
}
.jumbotron h1,
.jumbotron .h1 {
  color: inherit;
}
.jumbotron p {
  margin-bottom: 15px;
  font-size: 20px;
  font-weight: 200;
}
.jumbotron > hr {
  border-top-color: #d5d5d5;
}
.container .jumbotron,
.container-fluid .jumbotron {
  border-radius: 3px;
  padding-left: 0px;
  padding-right: 0px;
}
.jumbotron .container {
  max-width: 100%;
}
@media screen and (min-width: 768px) {
  .jumbotron {
    padding-top: 48px;
    padding-bottom: 48px;
  }
  .container .jumbotron,
  .container-fluid .jumbotron {
    padding-left: 60px;
    padding-right: 60px;
  }
  .jumbotron h1,
  .jumbotron .h1 {
    font-size: 59px;
  }
}
.thumbnail {
  display: block;
  padding: 4px;
  margin-bottom: 18px;
  line-height: 1.42857143;
  background-color: #fff;
  border: 1px solid #ddd;
  border-radius: 2px;
  -webkit-transition: border 0.2s ease-in-out;
  -o-transition: border 0.2s ease-in-out;
  transition: border 0.2s ease-in-out;
}
.thumbnail > img,
.thumbnail a > img {
  margin-left: auto;
  margin-right: auto;
}
a.thumbnail:hover,
a.thumbnail:focus,
a.thumbnail.active {
  border-color: #337ab7;
}
.thumbnail .caption {
  padding: 9px;
  color: #000;
}
.alert {
  padding: 15px;
  margin-bottom: 18px;
  border: 1px solid transparent;
  border-radius: 2px;
}
.alert h4 {
  margin-top: 0;
  color: inherit;
}
.alert .alert-link {
  font-weight: bold;
}
.alert > p,
.alert > ul {
  margin-bottom: 0;
}
.alert > p + p {
  margin-top: 5px;
}
.alert-dismissable,
.alert-dismissible {
  padding-right: 35px;
}
.alert-dismissable .close,
.alert-dismissible .close {
  position: relative;
  top: -2px;
  right: -21px;
  color: inherit;
}
.alert-success {
  background-color: #dff0d8;
  border-color: #d6e9c6;
  color: #3c763d;
}
.alert-success hr {
  border-top-color: #c9e2b3;
}
.alert-success .alert-link {
  color: #2b542c;
}
.alert-info {
  background-color: #d9edf7;
  border-color: #bce8f1;
  color: #31708f;
}
.alert-info hr {
  border-top-color: #a6e1ec;
}
.alert-info .alert-link {
  color: #245269;
}
.alert-warning {
  background-color: #fcf8e3;
  border-color: #faebcc;
  color: #8a6d3b;
}
.alert-warning hr {
  border-top-color: #f7e1b5;
}
.alert-warning .alert-link {
  color: #66512c;
}
.alert-danger {
  background-color: #f2dede;
  border-color: #ebccd1;
  color: #a94442;
}
.alert-danger hr {
  border-top-color: #e4b9c0;
}
.alert-danger .alert-link {
  color: #843534;
}
@-webkit-keyframes progress-bar-stripes {
  from {
    background-position: 40px 0;
  }
  to {
    background-position: 0 0;
  }
}
@keyframes progress-bar-stripes {
  from {
    background-position: 40px 0;
  }
  to {
    background-position: 0 0;
  }
}
.progress {
  overflow: hidden;
  height: 18px;
  margin-bottom: 18px;
  background-color: #f5f5f5;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 1px 2px rgba(0, 0, 0, 0.1);
  box-shadow: inset 0 1px 2px rgba(0, 0, 0, 0.1);
}
.progress-bar {
  float: left;
  width: 0%;
  height: 100%;
  font-size: 12px;
  line-height: 18px;
  color: #fff;
  text-align: center;
  background-color: #337ab7;
  -webkit-box-shadow: inset 0 -1px 0 rgba(0, 0, 0, 0.15);
  box-shadow: inset 0 -1px 0 rgba(0, 0, 0, 0.15);
  -webkit-transition: width 0.6s ease;
  -o-transition: width 0.6s ease;
  transition: width 0.6s ease;
}
.progress-striped .progress-bar,
.progress-bar-striped {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-size: 40px 40px;
}
.progress.active .progress-bar,
.progress-bar.active {
  -webkit-animation: progress-bar-stripes 2s linear infinite;
  -o-animation: progress-bar-stripes 2s linear infinite;
  animation: progress-bar-stripes 2s linear infinite;
}
.progress-bar-success {
  background-color: #5cb85c;
}
.progress-striped .progress-bar-success {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
}
.progress-bar-info {
  background-color: #5bc0de;
}
.progress-striped .progress-bar-info {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
}
.progress-bar-warning {
  background-color: #f0ad4e;
}
.progress-striped .progress-bar-warning {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
}
.progress-bar-danger {
  background-color: #d9534f;
}
.progress-striped .progress-bar-danger {
  background-image: -webkit-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: -o-linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
  background-image: linear-gradient(45deg, rgba(255, 255, 255, 0.15) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.15) 50%, rgba(255, 255, 255, 0.15) 75%, transparent 75%, transparent);
}
.media {
  margin-top: 15px;
}
.media:first-child {
  margin-top: 0;
}
.media,
.media-body {
  zoom: 1;
  overflow: hidden;
}
.media-body {
  width: 10000px;
}
.media-object {
  display: block;
}
.media-object.img-thumbnail {
  max-width: none;
}
.media-right,
.media > .pull-right {
  padding-left: 10px;
}
.media-left,
.media > .pull-left {
  padding-right: 10px;
}
.media-left,
.media-right,
.media-body {
  display: table-cell;
  vertical-align: top;
}
.media-middle {
  vertical-align: middle;
}
.media-bottom {
  vertical-align: bottom;
}
.media-heading {
  margin-top: 0;
  margin-bottom: 5px;
}
.media-list {
  padding-left: 0;
  list-style: none;
}
.list-group {
  margin-bottom: 20px;
  padding-left: 0;
}
.list-group-item {
  position: relative;
  display: block;
  padding: 10px 15px;
  margin-bottom: -1px;
  background-color: #fff;
  border: 1px solid #ddd;
}
.list-group-item:first-child {
  border-top-right-radius: 2px;
  border-top-left-radius: 2px;
}
.list-group-item:last-child {
  margin-bottom: 0;
  border-bottom-right-radius: 2px;
  border-bottom-left-radius: 2px;
}
a.list-group-item,
button.list-group-item {
  color: #555;
}
a.list-group-item .list-group-item-heading,
button.list-group-item .list-group-item-heading {
  color: #333;
}
a.list-group-item:hover,
button.list-group-item:hover,
a.list-group-item:focus,
button.list-group-item:focus {
  text-decoration: none;
  color: #555;
  background-color: #f5f5f5;
}
button.list-group-item {
  width: 100%;
  text-align: left;
}
.list-group-item.disabled,
.list-group-item.disabled:hover,
.list-group-item.disabled:focus {
  background-color: #eeeeee;
  color: #777777;
  cursor: not-allowed;
}
.list-group-item.disabled .list-group-item-heading,
.list-group-item.disabled:hover .list-group-item-heading,
.list-group-item.disabled:focus .list-group-item-heading {
  color: inherit;
}
.list-group-item.disabled .list-group-item-text,
.list-group-item.disabled:hover .list-group-item-text,
.list-group-item.disabled:focus .list-group-item-text {
  color: #777777;
}
.list-group-item.active,
.list-group-item.active:hover,
.list-group-item.active:focus {
  z-index: 2;
  color: #fff;
  background-color: #337ab7;
  border-color: #337ab7;
}
.list-group-item.active .list-group-item-heading,
.list-group-item.active:hover .list-group-item-heading,
.list-group-item.active:focus .list-group-item-heading,
.list-group-item.active .list-group-item-heading > small,
.list-group-item.active:hover .list-group-item-heading > small,
.list-group-item.active:focus .list-group-item-heading > small,
.list-group-item.active .list-group-item-heading > .small,
.list-group-item.active:hover .list-group-item-heading > .small,
.list-group-item.active:focus .list-group-item-heading > .small {
  color: inherit;
}
.list-group-item.active .list-group-item-text,
.list-group-item.active:hover .list-group-item-text,
.list-group-item.active:focus .list-group-item-text {
  color: #c7ddef;
}
.list-group-item-success {
  color: #3c763d;
  background-color: #dff0d8;
}
a.list-group-item-success,
button.list-group-item-success {
  color: #3c763d;
}
a.list-group-item-success .list-group-item-heading,
button.list-group-item-success .list-group-item-heading {
  color: inherit;
}
a.list-group-item-success:hover,
button.list-group-item-success:hover,
a.list-group-item-success:focus,
button.list-group-item-success:focus {
  color: #3c763d;
  background-color: #d0e9c6;
}
a.list-group-item-success.active,
button.list-group-item-success.active,
a.list-group-item-success.active:hover,
button.list-group-item-success.active:hover,
a.list-group-item-success.active:focus,
button.list-group-item-success.active:focus {
  color: #fff;
  background-color: #3c763d;
  border-color: #3c763d;
}
.list-group-item-info {
  color: #31708f;
  background-color: #d9edf7;
}
a.list-group-item-info,
button.list-group-item-info {
  color: #31708f;
}
a.list-group-item-info .list-group-item-heading,
button.list-group-item-info .list-group-item-heading {
  color: inherit;
}
a.list-group-item-info:hover,
button.list-group-item-info:hover,
a.list-group-item-info:focus,
button.list-group-item-info:focus {
  color: #31708f;
  background-color: #c4e3f3;
}
a.list-group-item-info.active,
button.list-group-item-info.active,
a.list-group-item-info.active:hover,
button.list-group-item-info.active:hover,
a.list-group-item-info.active:focus,
button.list-group-item-info.active:focus {
  color: #fff;
  background-color: #31708f;
  border-color: #31708f;
}
.list-group-item-warning {
  color: #8a6d3b;
  background-color: #fcf8e3;
}
a.list-group-item-warning,
button.list-group-item-warning {
  color: #8a6d3b;
}
a.list-group-item-warning .list-group-item-heading,
button.list-group-item-warning .list-group-item-heading {
  color: inherit;
}
a.list-group-item-warning:hover,
button.list-group-item-warning:hover,
a.list-group-item-warning:focus,
button.list-group-item-warning:focus {
  color: #8a6d3b;
  background-color: #faf2cc;
}
a.list-group-item-warning.active,
button.list-group-item-warning.active,
a.list-group-item-warning.active:hover,
button.list-group-item-warning.active:hover,
a.list-group-item-warning.active:focus,
button.list-group-item-warning.active:focus {
  color: #fff;
  background-color: #8a6d3b;
  border-color: #8a6d3b;
}
.list-group-item-danger {
  color: #a94442;
  background-color: #f2dede;
}
a.list-group-item-danger,
button.list-group-item-danger {
  color: #a94442;
}
a.list-group-item-danger .list-group-item-heading,
button.list-group-item-danger .list-group-item-heading {
  color: inherit;
}
a.list-group-item-danger:hover,
button.list-group-item-danger:hover,
a.list-group-item-danger:focus,
button.list-group-item-danger:focus {
  color: #a94442;
  background-color: #ebcccc;
}
a.list-group-item-danger.active,
button.list-group-item-danger.active,
a.list-group-item-danger.active:hover,
button.list-group-item-danger.active:hover,
a.list-group-item-danger.active:focus,
button.list-group-item-danger.active:focus {
  color: #fff;
  background-color: #a94442;
  border-color: #a94442;
}
.list-group-item-heading {
  margin-top: 0;
  margin-bottom: 5px;
}
.list-group-item-text {
  margin-bottom: 0;
  line-height: 1.3;
}
.panel {
  margin-bottom: 18px;
  background-color: #fff;
  border: 1px solid transparent;
  border-radius: 2px;
  -webkit-box-shadow: 0 1px 1px rgba(0, 0, 0, 0.05);
  box-shadow: 0 1px 1px rgba(0, 0, 0, 0.05);
}
.panel-body {
  padding: 15px;
}
.panel-heading {
  padding: 10px 15px;
  border-bottom: 1px solid transparent;
  border-top-right-radius: 1px;
  border-top-left-radius: 1px;
}
.panel-heading > .dropdown .dropdown-toggle {
  color: inherit;
}
.panel-title {
  margin-top: 0;
  margin-bottom: 0;
  font-size: 15px;
  color: inherit;
}
.panel-title > a,
.panel-title > small,
.panel-title > .small,
.panel-title > small > a,
.panel-title > .small > a {
  color: inherit;
}
.panel-footer {
  padding: 10px 15px;
  background-color: #f5f5f5;
  border-top: 1px solid #ddd;
  border-bottom-right-radius: 1px;
  border-bottom-left-radius: 1px;
}
.panel > .list-group,
.panel > .panel-collapse > .list-group {
  margin-bottom: 0;
}
.panel > .list-group .list-group-item,
.panel > .panel-collapse > .list-group .list-group-item {
  border-width: 1px 0;
  border-radius: 0;
}
.panel > .list-group:first-child .list-group-item:first-child,
.panel > .panel-collapse > .list-group:first-child .list-group-item:first-child {
  border-top: 0;
  border-top-right-radius: 1px;
  border-top-left-radius: 1px;
}
.panel > .list-group:last-child .list-group-item:last-child,
.panel > .panel-collapse > .list-group:last-child .list-group-item:last-child {
  border-bottom: 0;
  border-bottom-right-radius: 1px;
  border-bottom-left-radius: 1px;
}
.panel > .panel-heading + .panel-collapse > .list-group .list-group-item:first-child {
  border-top-right-radius: 0;
  border-top-left-radius: 0;
}
.panel-heading + .list-group .list-group-item:first-child {
  border-top-width: 0;
}
.list-group + .panel-footer {
  border-top-width: 0;
}
.panel > .table,
.panel > .table-responsive > .table,
.panel > .panel-collapse > .table {
  margin-bottom: 0;
}
.panel > .table caption,
.panel > .table-responsive > .table caption,
.panel > .panel-collapse > .table caption {
  padding-left: 15px;
  padding-right: 15px;
}
.panel > .table:first-child,
.panel > .table-responsive:first-child > .table:first-child {
  border-top-right-radius: 1px;
  border-top-left-radius: 1px;
}
.panel > .table:first-child > thead:first-child > tr:first-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child,
.panel > .table:first-child > tbody:first-child > tr:first-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child {
  border-top-left-radius: 1px;
  border-top-right-radius: 1px;
}
.panel > .table:first-child > thead:first-child > tr:first-child td:first-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child td:first-child,
.panel > .table:first-child > tbody:first-child > tr:first-child td:first-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child td:first-child,
.panel > .table:first-child > thead:first-child > tr:first-child th:first-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child th:first-child,
.panel > .table:first-child > tbody:first-child > tr:first-child th:first-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child th:first-child {
  border-top-left-radius: 1px;
}
.panel > .table:first-child > thead:first-child > tr:first-child td:last-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child td:last-child,
.panel > .table:first-child > tbody:first-child > tr:first-child td:last-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child td:last-child,
.panel > .table:first-child > thead:first-child > tr:first-child th:last-child,
.panel > .table-responsive:first-child > .table:first-child > thead:first-child > tr:first-child th:last-child,
.panel > .table:first-child > tbody:first-child > tr:first-child th:last-child,
.panel > .table-responsive:first-child > .table:first-child > tbody:first-child > tr:first-child th:last-child {
  border-top-right-radius: 1px;
}
.panel > .table:last-child,
.panel > .table-responsive:last-child > .table:last-child {
  border-bottom-right-radius: 1px;
  border-bottom-left-radius: 1px;
}
.panel > .table:last-child > tbody:last-child > tr:last-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child {
  border-bottom-left-radius: 1px;
  border-bottom-right-radius: 1px;
}
.panel > .table:last-child > tbody:last-child > tr:last-child td:first-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child td:first-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child td:first-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child td:first-child,
.panel > .table:last-child > tbody:last-child > tr:last-child th:first-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child th:first-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child th:first-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child th:first-child {
  border-bottom-left-radius: 1px;
}
.panel > .table:last-child > tbody:last-child > tr:last-child td:last-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child td:last-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child td:last-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child td:last-child,
.panel > .table:last-child > tbody:last-child > tr:last-child th:last-child,
.panel > .table-responsive:last-child > .table:last-child > tbody:last-child > tr:last-child th:last-child,
.panel > .table:last-child > tfoot:last-child > tr:last-child th:last-child,
.panel > .table-responsive:last-child > .table:last-child > tfoot:last-child > tr:last-child th:last-child {
  border-bottom-right-radius: 1px;
}
.panel > .panel-body + .table,
.panel > .panel-body + .table-responsive,
.panel > .table + .panel-body,
.panel > .table-responsive + .panel-body {
  border-top: 1px solid #ddd;
}
.panel > .table > tbody:first-child > tr:first-child th,
.panel > .table > tbody:first-child > tr:first-child td {
  border-top: 0;
}
.panel > .table-bordered,
.panel > .table-responsive > .table-bordered {
  border: 0;
}
.panel > .table-bordered > thead > tr > th:first-child,
.panel > .table-responsive > .table-bordered > thead > tr > th:first-child,
.panel > .table-bordered > tbody > tr > th:first-child,
.panel > .table-responsive > .table-bordered > tbody > tr > th:first-child,
.panel > .table-bordered > tfoot > tr > th:first-child,
.panel > .table-responsive > .table-bordered > tfoot > tr > th:first-child,
.panel > .table-bordered > thead > tr > td:first-child,
.panel > .table-responsive > .table-bordered > thead > tr > td:first-child,
.panel > .table-bordered > tbody > tr > td:first-child,
.panel > .table-responsive > .table-bordered > tbody > tr > td:first-child,
.panel > .table-bordered > tfoot > tr > td:first-child,
.panel > .table-responsive > .table-bordered > tfoot > tr > td:first-child {
  border-left: 0;
}
.panel > .table-bordered > thead > tr > th:last-child,
.panel > .table-responsive > .table-bordered > thead > tr > th:last-child,
.panel > .table-bordered > tbody > tr > th:last-child,
.panel > .table-responsive > .table-bordered > tbody > tr > th:last-child,
.panel > .table-bordered > tfoot > tr > th:last-child,
.panel > .table-responsive > .table-bordered > tfoot > tr > th:last-child,
.panel > .table-bordered > thead > tr > td:last-child,
.panel > .table-responsive > .table-bordered > thead > tr > td:last-child,
.panel > .table-bordered > tbody > tr > td:last-child,
.panel > .table-responsive > .table-bordered > tbody > tr > td:last-child,
.panel > .table-bordered > tfoot > tr > td:last-child,
.panel > .table-responsive > .table-bordered > tfoot > tr > td:last-child {
  border-right: 0;
}
.panel > .table-bordered > thead > tr:first-child > td,
.panel > .table-responsive > .table-bordered > thead > tr:first-child > td,
.panel > .table-bordered > tbody > tr:first-child > td,
.panel > .table-responsive > .table-bordered > tbody > tr:first-child > td,
.panel > .table-bordered > thead > tr:first-child > th,
.panel > .table-responsive > .table-bordered > thead > tr:first-child > th,
.panel > .table-bordered > tbody > tr:first-child > th,
.panel > .table-responsive > .table-bordered > tbody > tr:first-child > th {
  border-bottom: 0;
}
.panel > .table-bordered > tbody > tr:last-child > td,
.panel > .table-responsive > .table-bordered > tbody > tr:last-child > td,
.panel > .table-bordered > tfoot > tr:last-child > td,
.panel > .table-responsive > .table-bordered > tfoot > tr:last-child > td,
.panel > .table-bordered > tbody > tr:last-child > th,
.panel > .table-responsive > .table-bordered > tbody > tr:last-child > th,
.panel > .table-bordered > tfoot > tr:last-child > th,
.panel > .table-responsive > .table-bordered > tfoot > tr:last-child > th {
  border-bottom: 0;
}
.panel > .table-responsive {
  border: 0;
  margin-bottom: 0;
}
.panel-group {
  margin-bottom: 18px;
}
.panel-group .panel {
  margin-bottom: 0;
  border-radius: 2px;
}
.panel-group .panel + .panel {
  margin-top: 5px;
}
.panel-group .panel-heading {
  border-bottom: 0;
}
.panel-group .panel-heading + .panel-collapse > .panel-body,
.panel-group .panel-heading + .panel-collapse > .list-group {
  border-top: 1px solid #ddd;
}
.panel-group .panel-footer {
  border-top: 0;
}
.panel-group .panel-footer + .panel-collapse .panel-body {
  border-bottom: 1px solid #ddd;
}
.panel-default {
  border-color: #ddd;
}
.panel-default > .panel-heading {
  color: #333333;
  background-color: #f5f5f5;
  border-color: #ddd;
}
.panel-default > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #ddd;
}
.panel-default > .panel-heading .badge {
  color: #f5f5f5;
  background-color: #333333;
}
.panel-default > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #ddd;
}
.panel-primary {
  border-color: #337ab7;
}
.panel-primary > .panel-heading {
  color: #fff;
  background-color: #337ab7;
  border-color: #337ab7;
}
.panel-primary > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #337ab7;
}
.panel-primary > .panel-heading .badge {
  color: #337ab7;
  background-color: #fff;
}
.panel-primary > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #337ab7;
}
.panel-success {
  border-color: #d6e9c6;
}
.panel-success > .panel-heading {
  color: #3c763d;
  background-color: #dff0d8;
  border-color: #d6e9c6;
}
.panel-success > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #d6e9c6;
}
.panel-success > .panel-heading .badge {
  color: #dff0d8;
  background-color: #3c763d;
}
.panel-success > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #d6e9c6;
}
.panel-info {
  border-color: #bce8f1;
}
.panel-info > .panel-heading {
  color: #31708f;
  background-color: #d9edf7;
  border-color: #bce8f1;
}
.panel-info > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #bce8f1;
}
.panel-info > .panel-heading .badge {
  color: #d9edf7;
  background-color: #31708f;
}
.panel-info > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #bce8f1;
}
.panel-warning {
  border-color: #faebcc;
}
.panel-warning > .panel-heading {
  color: #8a6d3b;
  background-color: #fcf8e3;
  border-color: #faebcc;
}
.panel-warning > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #faebcc;
}
.panel-warning > .panel-heading .badge {
  color: #fcf8e3;
  background-color: #8a6d3b;
}
.panel-warning > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #faebcc;
}
.panel-danger {
  border-color: #ebccd1;
}
.panel-danger > .panel-heading {
  color: #a94442;
  background-color: #f2dede;
  border-color: #ebccd1;
}
.panel-danger > .panel-heading + .panel-collapse > .panel-body {
  border-top-color: #ebccd1;
}
.panel-danger > .panel-heading .badge {
  color: #f2dede;
  background-color: #a94442;
}
.panel-danger > .panel-footer + .panel-collapse > .panel-body {
  border-bottom-color: #ebccd1;
}
.embed-responsive {
  position: relative;
  display: block;
  height: 0;
  padding: 0;
  overflow: hidden;
}
.embed-responsive .embed-responsive-item,
.embed-responsive iframe,
.embed-responsive embed,
.embed-responsive object,
.embed-responsive video {
  position: absolute;
  top: 0;
  left: 0;
  bottom: 0;
  height: 100%;
  width: 100%;
  border: 0;
}
.embed-responsive-16by9 {
  padding-bottom: 56.25%;
}
.embed-responsive-4by3 {
  padding-bottom: 75%;
}
.well {
  min-height: 20px;
  padding: 19px;
  margin-bottom: 20px;
  background-color: #f5f5f5;
  border: 1px solid #e3e3e3;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.05);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.05);
}
.well blockquote {
  border-color: #ddd;
  border-color: rgba(0, 0, 0, 0.15);
}
.well-lg {
  padding: 24px;
  border-radius: 3px;
}
.well-sm {
  padding: 9px;
  border-radius: 1px;
}
.close {
  float: right;
  font-size: 19.5px;
  font-weight: bold;
  line-height: 1;
  color: #000;
  text-shadow: 0 1px 0 #fff;
  opacity: 0.2;
  filter: alpha(opacity=20);
}
.close:hover,
.close:focus {
  color: #000;
  text-decoration: none;
  cursor: pointer;
  opacity: 0.5;
  filter: alpha(opacity=50);
}
button.close {
  padding: 0;
  cursor: pointer;
  background: transparent;
  border: 0;
  -webkit-appearance: none;
}
.modal-open {
  overflow: hidden;
}
.modal {
  display: none;
  overflow: hidden;
  position: fixed;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  z-index: 1050;
  -webkit-overflow-scrolling: touch;
  outline: 0;
}
.modal.fade .modal-dialog {
  -webkit-transform: translate(0, -25%);
  -ms-transform: translate(0, -25%);
  -o-transform: translate(0, -25%);
  transform: translate(0, -25%);
  -webkit-transition: -webkit-transform 0.3s ease-out;
  -moz-transition: -moz-transform 0.3s ease-out;
  -o-transition: -o-transform 0.3s ease-out;
  transition: transform 0.3s ease-out;
}
.modal.in .modal-dialog {
  -webkit-transform: translate(0, 0);
  -ms-transform: translate(0, 0);
  -o-transform: translate(0, 0);
  transform: translate(0, 0);
}
.modal-open .modal {
  overflow-x: hidden;
  overflow-y: auto;
}
.modal-dialog {
  position: relative;
  width: auto;
  margin: 10px;
}
.modal-content {
  position: relative;
  background-color: #fff;
  border: 1px solid #999;
  border: 1px solid rgba(0, 0, 0, 0.2);
  border-radius: 3px;
  -webkit-box-shadow: 0 3px 9px rgba(0, 0, 0, 0.5);
  box-shadow: 0 3px 9px rgba(0, 0, 0, 0.5);
  background-clip: padding-box;
  outline: 0;
}
.modal-backdrop {
  position: fixed;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  z-index: 1040;
  background-color: #000;
}
.modal-backdrop.fade {
  opacity: 0;
  filter: alpha(opacity=0);
}
.modal-backdrop.in {
  opacity: 0.5;
  filter: alpha(opacity=50);
}
.modal-header {
  padding: 15px;
  border-bottom: 1px solid #e5e5e5;
}
.modal-header .close {
  margin-top: -2px;
}
.modal-title {
  margin: 0;
  line-height: 1.42857143;
}
.modal-body {
  position: relative;
  padding: 15px;
}
.modal-footer {
  padding: 15px;
  text-align: right;
  border-top: 1px solid #e5e5e5;
}
.modal-footer .btn + .btn {
  margin-left: 5px;
  margin-bottom: 0;
}
.modal-footer .btn-group .btn + .btn {
  margin-left: -1px;
}
.modal-footer .btn-block + .btn-block {
  margin-left: 0;
}
.modal-scrollbar-measure {
  position: absolute;
  top: -9999px;
  width: 50px;
  height: 50px;
  overflow: scroll;
}
@media (min-width: 768px) {
  .modal-dialog {
    width: 600px;
    margin: 30px auto;
  }
  .modal-content {
    -webkit-box-shadow: 0 5px 15px rgba(0, 0, 0, 0.5);
    box-shadow: 0 5px 15px rgba(0, 0, 0, 0.5);
  }
  .modal-sm {
    width: 300px;
  }
}
@media (min-width: 992px) {
  .modal-lg {
    width: 900px;
  }
}
.tooltip {
  position: absolute;
  z-index: 1070;
  display: block;
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
  font-style: normal;
  font-weight: normal;
  letter-spacing: normal;
  line-break: auto;
  line-height: 1.42857143;
  text-align: left;
  text-align: start;
  text-decoration: none;
  text-shadow: none;
  text-transform: none;
  white-space: normal;
  word-break: normal;
  word-spacing: normal;
  word-wrap: normal;
  font-size: 12px;
  opacity: 0;
  filter: alpha(opacity=0);
}
.tooltip.in {
  opacity: 0.9;
  filter: alpha(opacity=90);
}
.tooltip.top {
  margin-top: -3px;
  padding: 5px 0;
}
.tooltip.right {
  margin-left: 3px;
  padding: 0 5px;
}
.tooltip.bottom {
  margin-top: 3px;
  padding: 5px 0;
}
.tooltip.left {
  margin-left: -3px;
  padding: 0 5px;
}
.tooltip-inner {
  max-width: 200px;
  padding: 3px 8px;
  color: #fff;
  text-align: center;
  background-color: #000;
  border-radius: 2px;
}
.tooltip-arrow {
  position: absolute;
  width: 0;
  height: 0;
  border-color: transparent;
  border-style: solid;
}
.tooltip.top .tooltip-arrow {
  bottom: 0;
  left: 50%;
  margin-left: -5px;
  border-width: 5px 5px 0;
  border-top-color: #000;
}
.tooltip.top-left .tooltip-arrow {
  bottom: 0;
  right: 5px;
  margin-bottom: -5px;
  border-width: 5px 5px 0;
  border-top-color: #000;
}
.tooltip.top-right .tooltip-arrow {
  bottom: 0;
  left: 5px;
  margin-bottom: -5px;
  border-width: 5px 5px 0;
  border-top-color: #000;
}
.tooltip.right .tooltip-arrow {
  top: 50%;
  left: 0;
  margin-top: -5px;
  border-width: 5px 5px 5px 0;
  border-right-color: #000;
}
.tooltip.left .tooltip-arrow {
  top: 50%;
  right: 0;
  margin-top: -5px;
  border-width: 5px 0 5px 5px;
  border-left-color: #000;
}
.tooltip.bottom .tooltip-arrow {
  top: 0;
  left: 50%;
  margin-left: -5px;
  border-width: 0 5px 5px;
  border-bottom-color: #000;
}
.tooltip.bottom-left .tooltip-arrow {
  top: 0;
  right: 5px;
  margin-top: -5px;
  border-width: 0 5px 5px;
  border-bottom-color: #000;
}
.tooltip.bottom-right .tooltip-arrow {
  top: 0;
  left: 5px;
  margin-top: -5px;
  border-width: 0 5px 5px;
  border-bottom-color: #000;
}
.popover {
  position: absolute;
  top: 0;
  left: 0;
  z-index: 1060;
  display: none;
  max-width: 276px;
  padding: 1px;
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
  font-style: normal;
  font-weight: normal;
  letter-spacing: normal;
  line-break: auto;
  line-height: 1.42857143;
  text-align: left;
  text-align: start;
  text-decoration: none;
  text-shadow: none;
  text-transform: none;
  white-space: normal;
  word-break: normal;
  word-spacing: normal;
  word-wrap: normal;
  font-size: 13px;
  background-color: #fff;
  background-clip: padding-box;
  border: 1px solid #ccc;
  border: 1px solid rgba(0, 0, 0, 0.2);
  border-radius: 3px;
  -webkit-box-shadow: 0 5px 10px rgba(0, 0, 0, 0.2);
  box-shadow: 0 5px 10px rgba(0, 0, 0, 0.2);
}
.popover.top {
  margin-top: -10px;
}
.popover.right {
  margin-left: 10px;
}
.popover.bottom {
  margin-top: 10px;
}
.popover.left {
  margin-left: -10px;
}
.popover-title {
  margin: 0;
  padding: 8px 14px;
  font-size: 13px;
  background-color: #f7f7f7;
  border-bottom: 1px solid #ebebeb;
  border-radius: 2px 2px 0 0;
}
.popover-content {
  padding: 9px 14px;
}
.popover > .arrow,
.popover > .arrow:after {
  position: absolute;
  display: block;
  width: 0;
  height: 0;
  border-color: transparent;
  border-style: solid;
}
.popover > .arrow {
  border-width: 11px;
}
.popover > .arrow:after {
  border-width: 10px;
  content: "";
}
.popover.top > .arrow {
  left: 50%;
  margin-left: -11px;
  border-bottom-width: 0;
  border-top-color: #999999;
  border-top-color: rgba(0, 0, 0, 0.25);
  bottom: -11px;
}
.popover.top > .arrow:after {
  content: " ";
  bottom: 1px;
  margin-left: -10px;
  border-bottom-width: 0;
  border-top-color: #fff;
}
.popover.right > .arrow {
  top: 50%;
  left: -11px;
  margin-top: -11px;
  border-left-width: 0;
  border-right-color: #999999;
  border-right-color: rgba(0, 0, 0, 0.25);
}
.popover.right > .arrow:after {
  content: " ";
  left: 1px;
  bottom: -10px;
  border-left-width: 0;
  border-right-color: #fff;
}
.popover.bottom > .arrow {
  left: 50%;
  margin-left: -11px;
  border-top-width: 0;
  border-bottom-color: #999999;
  border-bottom-color: rgba(0, 0, 0, 0.25);
  top: -11px;
}
.popover.bottom > .arrow:after {
  content: " ";
  top: 1px;
  margin-left: -10px;
  border-top-width: 0;
  border-bottom-color: #fff;
}
.popover.left > .arrow {
  top: 50%;
  right: -11px;
  margin-top: -11px;
  border-right-width: 0;
  border-left-color: #999999;
  border-left-color: rgba(0, 0, 0, 0.25);
}
.popover.left > .arrow:after {
  content: " ";
  right: 1px;
  border-right-width: 0;
  border-left-color: #fff;
  bottom: -10px;
}
.carousel {
  position: relative;
}
.carousel-inner {
  position: relative;
  overflow: hidden;
  width: 100%;
}
.carousel-inner > .item {
  display: none;
  position: relative;
  -webkit-transition: 0.6s ease-in-out left;
  -o-transition: 0.6s ease-in-out left;
  transition: 0.6s ease-in-out left;
}
.carousel-inner > .item > img,
.carousel-inner > .item > a > img {
  line-height: 1;
}
@media all and (transform-3d), (-webkit-transform-3d) {
  .carousel-inner > .item {
    -webkit-transition: -webkit-transform 0.6s ease-in-out;
    -moz-transition: -moz-transform 0.6s ease-in-out;
    -o-transition: -o-transform 0.6s ease-in-out;
    transition: transform 0.6s ease-in-out;
    -webkit-backface-visibility: hidden;
    -moz-backface-visibility: hidden;
    backface-visibility: hidden;
    -webkit-perspective: 1000px;
    -moz-perspective: 1000px;
    perspective: 1000px;
  }
  .carousel-inner > .item.next,
  .carousel-inner > .item.active.right {
    -webkit-transform: translate3d(100%, 0, 0);
    transform: translate3d(100%, 0, 0);
    left: 0;
  }
  .carousel-inner > .item.prev,
  .carousel-inner > .item.active.left {
    -webkit-transform: translate3d(-100%, 0, 0);
    transform: translate3d(-100%, 0, 0);
    left: 0;
  }
  .carousel-inner > .item.next.left,
  .carousel-inner > .item.prev.right,
  .carousel-inner > .item.active {
    -webkit-transform: translate3d(0, 0, 0);
    transform: translate3d(0, 0, 0);
    left: 0;
  }
}
.carousel-inner > .active,
.carousel-inner > .next,
.carousel-inner > .prev {
  display: block;
}
.carousel-inner > .active {
  left: 0;
}
.carousel-inner > .next,
.carousel-inner > .prev {
  position: absolute;
  top: 0;
  width: 100%;
}
.carousel-inner > .next {
  left: 100%;
}
.carousel-inner > .prev {
  left: -100%;
}
.carousel-inner > .next.left,
.carousel-inner > .prev.right {
  left: 0;
}
.carousel-inner > .active.left {
  left: -100%;
}
.carousel-inner > .active.right {
  left: 100%;
}
.carousel-control {
  position: absolute;
  top: 0;
  left: 0;
  bottom: 0;
  width: 15%;
  opacity: 0.5;
  filter: alpha(opacity=50);
  font-size: 20px;
  color: #fff;
  text-align: center;
  text-shadow: 0 1px 2px rgba(0, 0, 0, 0.6);
  background-color: rgba(0, 0, 0, 0);
}
.carousel-control.left {
  background-image: -webkit-linear-gradient(left, rgba(0, 0, 0, 0.5) 0%, rgba(0, 0, 0, 0.0001) 100%);
  background-image: -o-linear-gradient(left, rgba(0, 0, 0, 0.5) 0%, rgba(0, 0, 0, 0.0001) 100%);
  background-image: linear-gradient(to right, rgba(0, 0, 0, 0.5) 0%, rgba(0, 0, 0, 0.0001) 100%);
  background-repeat: repeat-x;
  filter: progid:DXImageTransform.Microsoft.gradient(startColorstr='#80000000', endColorstr='#00000000', GradientType=1);
}
.carousel-control.right {
  left: auto;
  right: 0;
  background-image: -webkit-linear-gradient(left, rgba(0, 0, 0, 0.0001) 0%, rgba(0, 0, 0, 0.5) 100%);
  background-image: -o-linear-gradient(left, rgba(0, 0, 0, 0.0001) 0%, rgba(0, 0, 0, 0.5) 100%);
  background-image: linear-gradient(to right, rgba(0, 0, 0, 0.0001) 0%, rgba(0, 0, 0, 0.5) 100%);
  background-repeat: repeat-x;
  filter: progid:DXImageTransform.Microsoft.gradient(startColorstr='#00000000', endColorstr='#80000000', GradientType=1);
}
.carousel-control:hover,
.carousel-control:focus {
  outline: 0;
  color: #fff;
  text-decoration: none;
  opacity: 0.9;
  filter: alpha(opacity=90);
}
.carousel-control .icon-prev,
.carousel-control .icon-next,
.carousel-control .glyphicon-chevron-left,
.carousel-control .glyphicon-chevron-right {
  position: absolute;
  top: 50%;
  margin-top: -10px;
  z-index: 5;
  display: inline-block;
}
.carousel-control .icon-prev,
.carousel-control .glyphicon-chevron-left {
  left: 50%;
  margin-left: -10px;
}
.carousel-control .icon-next,
.carousel-control .glyphicon-chevron-right {
  right: 50%;
  margin-right: -10px;
}
.carousel-control .icon-prev,
.carousel-control .icon-next {
  width: 20px;
  height: 20px;
  line-height: 1;
  font-family: serif;
}
.carousel-control .icon-prev:before {
  content: '\2039';
}
.carousel-control .icon-next:before {
  content: '\203a';
}
.carousel-indicators {
  position: absolute;
  bottom: 10px;
  left: 50%;
  z-index: 15;
  width: 60%;
  margin-left: -30%;
  padding-left: 0;
  list-style: none;
  text-align: center;
}
.carousel-indicators li {
  display: inline-block;
  width: 10px;
  height: 10px;
  margin: 1px;
  text-indent: -999px;
  border: 1px solid #fff;
  border-radius: 10px;
  cursor: pointer;
  background-color: #000 \9;
  background-color: rgba(0, 0, 0, 0);
}
.carousel-indicators .active {
  margin: 0;
  width: 12px;
  height: 12px;
  background-color: #fff;
}
.carousel-caption {
  position: absolute;
  left: 15%;
  right: 15%;
  bottom: 20px;
  z-index: 10;
  padding-top: 20px;
  padding-bottom: 20px;
  color: #fff;
  text-align: center;
  text-shadow: 0 1px 2px rgba(0, 0, 0, 0.6);
}
.carousel-caption .btn {
  text-shadow: none;
}
@media screen and (min-width: 768px) {
  .carousel-control .glyphicon-chevron-left,
  .carousel-control .glyphicon-chevron-right,
  .carousel-control .icon-prev,
  .carousel-control .icon-next {
    width: 30px;
    height: 30px;
    margin-top: -10px;
    font-size: 30px;
  }
  .carousel-control .glyphicon-chevron-left,
  .carousel-control .icon-prev {
    margin-left: -10px;
  }
  .carousel-control .glyphicon-chevron-right,
  .carousel-control .icon-next {
    margin-right: -10px;
  }
  .carousel-caption {
    left: 20%;
    right: 20%;
    padding-bottom: 30px;
  }
  .carousel-indicators {
    bottom: 20px;
  }
}
.clearfix:before,
.clearfix:after,
.dl-horizontal dd:before,
.dl-horizontal dd:after,
.container:before,
.container:after,
.container-fluid:before,
.container-fluid:after,
.row:before,
.row:after,
.form-horizontal .form-group:before,
.form-horizontal .form-group:after,
.btn-toolbar:before,
.btn-toolbar:after,
.btn-group-vertical > .btn-group:before,
.btn-group-vertical > .btn-group:after,
.nav:before,
.nav:after,
.navbar:before,
.navbar:after,
.navbar-header:before,
.navbar-header:after,
.navbar-collapse:before,
.navbar-collapse:after,
.pager:before,
.pager:after,
.panel-body:before,
.panel-body:after,
.modal-header:before,
.modal-header:after,
.modal-footer:before,
.modal-footer:after,
.item_buttons:before,
.item_buttons:after {
  content: " ";
  display: table;
}
.clearfix:after,
.dl-horizontal dd:after,
.container:after,
.container-fluid:after,
.row:after,
.form-horizontal .form-group:after,
.btn-toolbar:after,
.btn-group-vertical > .btn-group:after,
.nav:after,
.navbar:after,
.navbar-header:after,
.navbar-collapse:after,
.pager:after,
.panel-body:after,
.modal-header:after,
.modal-footer:after,
.item_buttons:after {
  clear: both;
}
.center-block {
  display: block;
  margin-left: auto;
  margin-right: auto;
}
.pull-right {
  float: right !important;
}
.pull-left {
  float: left !important;
}
.hide {
  display: none !important;
}
.show {
  display: block !important;
}
.invisible {
  visibility: hidden;
}
.text-hide {
  font: 0/0 a;
  color: transparent;
  text-shadow: none;
  background-color: transparent;
  border: 0;
}
.hidden {
  display: none !important;
}
.affix {
  position: fixed;
}
@-ms-viewport {
  width: device-width;
}
.visible-xs,
.visible-sm,
.visible-md,
.visible-lg {
  display: none !important;
}
.visible-xs-block,
.visible-xs-inline,
.visible-xs-inline-block,
.visible-sm-block,
.visible-sm-inline,
.visible-sm-inline-block,
.visible-md-block,
.visible-md-inline,
.visible-md-inline-block,
.visible-lg-block,
.visible-lg-inline,
.visible-lg-inline-block {
  display: none !important;
}
@media (max-width: 767px) {
  .visible-xs {
    display: block !important;
  }
  table.visible-xs {
    display: table !important;
  }
  tr.visible-xs {
    display: table-row !important;
  }
  th.visible-xs,
  td.visible-xs {
    display: table-cell !important;
  }
}
@media (max-width: 767px) {
  .visible-xs-block {
    display: block !important;
  }
}
@media (max-width: 767px) {
  .visible-xs-inline {
    display: inline !important;
  }
}
@media (max-width: 767px) {
  .visible-xs-inline-block {
    display: inline-block !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .visible-sm {
    display: block !important;
  }
  table.visible-sm {
    display: table !important;
  }
  tr.visible-sm {
    display: table-row !important;
  }
  th.visible-sm,
  td.visible-sm {
    display: table-cell !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .visible-sm-block {
    display: block !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .visible-sm-inline {
    display: inline !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .visible-sm-inline-block {
    display: inline-block !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .visible-md {
    display: block !important;
  }
  table.visible-md {
    display: table !important;
  }
  tr.visible-md {
    display: table-row !important;
  }
  th.visible-md,
  td.visible-md {
    display: table-cell !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .visible-md-block {
    display: block !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .visible-md-inline {
    display: inline !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .visible-md-inline-block {
    display: inline-block !important;
  }
}
@media (min-width: 1200px) {
  .visible-lg {
    display: block !important;
  }
  table.visible-lg {
    display: table !important;
  }
  tr.visible-lg {
    display: table-row !important;
  }
  th.visible-lg,
  td.visible-lg {
    display: table-cell !important;
  }
}
@media (min-width: 1200px) {
  .visible-lg-block {
    display: block !important;
  }
}
@media (min-width: 1200px) {
  .visible-lg-inline {
    display: inline !important;
  }
}
@media (min-width: 1200px) {
  .visible-lg-inline-block {
    display: inline-block !important;
  }
}
@media (max-width: 767px) {
  .hidden-xs {
    display: none !important;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  .hidden-sm {
    display: none !important;
  }
}
@media (min-width: 992px) and (max-width: 1199px) {
  .hidden-md {
    display: none !important;
  }
}
@media (min-width: 1200px) {
  .hidden-lg {
    display: none !important;
  }
}
.visible-print {
  display: none !important;
}
@media print {
  .visible-print {
    display: block !important;
  }
  table.visible-print {
    display: table !important;
  }
  tr.visible-print {
    display: table-row !important;
  }
  th.visible-print,
  td.visible-print {
    display: table-cell !important;
  }
}
.visible-print-block {
  display: none !important;
}
@media print {
  .visible-print-block {
    display: block !important;
  }
}
.visible-print-inline {
  display: none !important;
}
@media print {
  .visible-print-inline {
    display: inline !important;
  }
}
.visible-print-inline-block {
  display: none !important;
}
@media print {
  .visible-print-inline-block {
    display: inline-block !important;
  }
}
@media print {
  .hidden-print {
    display: none !important;
  }
}
/*!
*
* Font Awesome
*
*/
/*!
 *  Font Awesome 4.7.0 by @davegandy - http://fontawesome.io - @fontawesome
 *  License - http://fontawesome.io/license (Font: SIL OFL 1.1, CSS: MIT License)
 */
/* FONT PATH
 * -------------------------- */
@font-face {
  font-family: 'FontAwesome';
  src: url('../components/font-awesome/fonts/fontawesome-webfont.eot?v=4.7.0');
  src: url('../components/font-awesome/fonts/fontawesome-webfont.eot?#iefix&v=4.7.0') format('embedded-opentype'), url('../components/font-awesome/fonts/fontawesome-webfont.woff2?v=4.7.0') format('woff2'), url('../components/font-awesome/fonts/fontawesome-webfont.woff?v=4.7.0') format('woff'), url('../components/font-awesome/fonts/fontawesome-webfont.ttf?v=4.7.0') format('truetype'), url('../components/font-awesome/fonts/fontawesome-webfont.svg?v=4.7.0#fontawesomeregular') format('svg');
  font-weight: normal;
  font-style: normal;
}
.fa {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
/* makes the font 33% larger relative to the icon container */
.fa-lg {
  font-size: 1.33333333em;
  line-height: 0.75em;
  vertical-align: -15%;
}
.fa-2x {
  font-size: 2em;
}
.fa-3x {
  font-size: 3em;
}
.fa-4x {
  font-size: 4em;
}
.fa-5x {
  font-size: 5em;
}
.fa-fw {
  width: 1.28571429em;
  text-align: center;
}
.fa-ul {
  padding-left: 0;
  margin-left: 2.14285714em;
  list-style-type: none;
}
.fa-ul > li {
  position: relative;
}
.fa-li {
  position: absolute;
  left: -2.14285714em;
  width: 2.14285714em;
  top: 0.14285714em;
  text-align: center;
}
.fa-li.fa-lg {
  left: -1.85714286em;
}
.fa-border {
  padding: .2em .25em .15em;
  border: solid 0.08em #eee;
  border-radius: .1em;
}
.fa-pull-left {
  float: left;
}
.fa-pull-right {
  float: right;
}
.fa.fa-pull-left {
  margin-right: .3em;
}
.fa.fa-pull-right {
  margin-left: .3em;
}
/* Deprecated as of 4.4.0 */
.pull-right {
  float: right;
}
.pull-left {
  float: left;
}
.fa.pull-left {
  margin-right: .3em;
}
.fa.pull-right {
  margin-left: .3em;
}
.fa-spin {
  -webkit-animation: fa-spin 2s infinite linear;
  animation: fa-spin 2s infinite linear;
}
.fa-pulse {
  -webkit-animation: fa-spin 1s infinite steps(8);
  animation: fa-spin 1s infinite steps(8);
}
@-webkit-keyframes fa-spin {
  0% {
    -webkit-transform: rotate(0deg);
    transform: rotate(0deg);
  }
  100% {
    -webkit-transform: rotate(359deg);
    transform: rotate(359deg);
  }
}
@keyframes fa-spin {
  0% {
    -webkit-transform: rotate(0deg);
    transform: rotate(0deg);
  }
  100% {
    -webkit-transform: rotate(359deg);
    transform: rotate(359deg);
  }
}
.fa-rotate-90 {
  -ms-filter: "progid:DXImageTransform.Microsoft.BasicImage(rotation=1)";
  -webkit-transform: rotate(90deg);
  -ms-transform: rotate(90deg);
  transform: rotate(90deg);
}
.fa-rotate-180 {
  -ms-filter: "progid:DXImageTransform.Microsoft.BasicImage(rotation=2)";
  -webkit-transform: rotate(180deg);
  -ms-transform: rotate(180deg);
  transform: rotate(180deg);
}
.fa-rotate-270 {
  -ms-filter: "progid:DXImageTransform.Microsoft.BasicImage(rotation=3)";
  -webkit-transform: rotate(270deg);
  -ms-transform: rotate(270deg);
  transform: rotate(270deg);
}
.fa-flip-horizontal {
  -ms-filter: "progid:DXImageTransform.Microsoft.BasicImage(rotation=0, mirror=1)";
  -webkit-transform: scale(-1, 1);
  -ms-transform: scale(-1, 1);
  transform: scale(-1, 1);
}
.fa-flip-vertical {
  -ms-filter: "progid:DXImageTransform.Microsoft.BasicImage(rotation=2, mirror=1)";
  -webkit-transform: scale(1, -1);
  -ms-transform: scale(1, -1);
  transform: scale(1, -1);
}
:root .fa-rotate-90,
:root .fa-rotate-180,
:root .fa-rotate-270,
:root .fa-flip-horizontal,
:root .fa-flip-vertical {
  filter: none;
}
.fa-stack {
  position: relative;
  display: inline-block;
  width: 2em;
  height: 2em;
  line-height: 2em;
  vertical-align: middle;
}
.fa-stack-1x,
.fa-stack-2x {
  position: absolute;
  left: 0;
  width: 100%;
  text-align: center;
}
.fa-stack-1x {
  line-height: inherit;
}
.fa-stack-2x {
  font-size: 2em;
}
.fa-inverse {
  color: #fff;
}
/* Font Awesome uses the Unicode Private Use Area (PUA) to ensure screen
   readers do not read off random characters that represent icons */
.fa-glass:before {
  content: "\f000";
}
.fa-music:before {
  content: "\f001";
}
.fa-search:before {
  content: "\f002";
}
.fa-envelope-o:before {
  content: "\f003";
}
.fa-heart:before {
  content: "\f004";
}
.fa-star:before {
  content: "\f005";
}
.fa-star-o:before {
  content: "\f006";
}
.fa-user:before {
  content: "\f007";
}
.fa-film:before {
  content: "\f008";
}
.fa-th-large:before {
  content: "\f009";
}
.fa-th:before {
  content: "\f00a";
}
.fa-th-list:before {
  content: "\f00b";
}
.fa-check:before {
  content: "\f00c";
}
.fa-remove:before,
.fa-close:before,
.fa-times:before {
  content: "\f00d";
}
.fa-search-plus:before {
  content: "\f00e";
}
.fa-search-minus:before {
  content: "\f010";
}
.fa-power-off:before {
  content: "\f011";
}
.fa-signal:before {
  content: "\f012";
}
.fa-gear:before,
.fa-cog:before {
  content: "\f013";
}
.fa-trash-o:before {
  content: "\f014";
}
.fa-home:before {
  content: "\f015";
}
.fa-file-o:before {
  content: "\f016";
}
.fa-clock-o:before {
  content: "\f017";
}
.fa-road:before {
  content: "\f018";
}
.fa-download:before {
  content: "\f019";
}
.fa-arrow-circle-o-down:before {
  content: "\f01a";
}
.fa-arrow-circle-o-up:before {
  content: "\f01b";
}
.fa-inbox:before {
  content: "\f01c";
}
.fa-play-circle-o:before {
  content: "\f01d";
}
.fa-rotate-right:before,
.fa-repeat:before {
  content: "\f01e";
}
.fa-refresh:before {
  content: "\f021";
}
.fa-list-alt:before {
  content: "\f022";
}
.fa-lock:before {
  content: "\f023";
}
.fa-flag:before {
  content: "\f024";
}
.fa-headphones:before {
  content: "\f025";
}
.fa-volume-off:before {
  content: "\f026";
}
.fa-volume-down:before {
  content: "\f027";
}
.fa-volume-up:before {
  content: "\f028";
}
.fa-qrcode:before {
  content: "\f029";
}
.fa-barcode:before {
  content: "\f02a";
}
.fa-tag:before {
  content: "\f02b";
}
.fa-tags:before {
  content: "\f02c";
}
.fa-book:before {
  content: "\f02d";
}
.fa-bookmark:before {
  content: "\f02e";
}
.fa-print:before {
  content: "\f02f";
}
.fa-camera:before {
  content: "\f030";
}
.fa-font:before {
  content: "\f031";
}
.fa-bold:before {
  content: "\f032";
}
.fa-italic:before {
  content: "\f033";
}
.fa-text-height:before {
  content: "\f034";
}
.fa-text-width:before {
  content: "\f035";
}
.fa-align-left:before {
  content: "\f036";
}
.fa-align-center:before {
  content: "\f037";
}
.fa-align-right:before {
  content: "\f038";
}
.fa-align-justify:before {
  content: "\f039";
}
.fa-list:before {
  content: "\f03a";
}
.fa-dedent:before,
.fa-outdent:before {
  content: "\f03b";
}
.fa-indent:before {
  content: "\f03c";
}
.fa-video-camera:before {
  content: "\f03d";
}
.fa-photo:before,
.fa-image:before,
.fa-picture-o:before {
  content: "\f03e";
}
.fa-pencil:before {
  content: "\f040";
}
.fa-map-marker:before {
  content: "\f041";
}
.fa-adjust:before {
  content: "\f042";
}
.fa-tint:before {
  content: "\f043";
}
.fa-edit:before,
.fa-pencil-square-o:before {
  content: "\f044";
}
.fa-share-square-o:before {
  content: "\f045";
}
.fa-check-square-o:before {
  content: "\f046";
}
.fa-arrows:before {
  content: "\f047";
}
.fa-step-backward:before {
  content: "\f048";
}
.fa-fast-backward:before {
  content: "\f049";
}
.fa-backward:before {
  content: "\f04a";
}
.fa-play:before {
  content: "\f04b";
}
.fa-pause:before {
  content: "\f04c";
}
.fa-stop:before {
  content: "\f04d";
}
.fa-forward:before {
  content: "\f04e";
}
.fa-fast-forward:before {
  content: "\f050";
}
.fa-step-forward:before {
  content: "\f051";
}
.fa-eject:before {
  content: "\f052";
}
.fa-chevron-left:before {
  content: "\f053";
}
.fa-chevron-right:before {
  content: "\f054";
}
.fa-plus-circle:before {
  content: "\f055";
}
.fa-minus-circle:before {
  content: "\f056";
}
.fa-times-circle:before {
  content: "\f057";
}
.fa-check-circle:before {
  content: "\f058";
}
.fa-question-circle:before {
  content: "\f059";
}
.fa-info-circle:before {
  content: "\f05a";
}
.fa-crosshairs:before {
  content: "\f05b";
}
.fa-times-circle-o:before {
  content: "\f05c";
}
.fa-check-circle-o:before {
  content: "\f05d";
}
.fa-ban:before {
  content: "\f05e";
}
.fa-arrow-left:before {
  content: "\f060";
}
.fa-arrow-right:before {
  content: "\f061";
}
.fa-arrow-up:before {
  content: "\f062";
}
.fa-arrow-down:before {
  content: "\f063";
}
.fa-mail-forward:before,
.fa-share:before {
  content: "\f064";
}
.fa-expand:before {
  content: "\f065";
}
.fa-compress:before {
  content: "\f066";
}
.fa-plus:before {
  content: "\f067";
}
.fa-minus:before {
  content: "\f068";
}
.fa-asterisk:before {
  content: "\f069";
}
.fa-exclamation-circle:before {
  content: "\f06a";
}
.fa-gift:before {
  content: "\f06b";
}
.fa-leaf:before {
  content: "\f06c";
}
.fa-fire:before {
  content: "\f06d";
}
.fa-eye:before {
  content: "\f06e";
}
.fa-eye-slash:before {
  content: "\f070";
}
.fa-warning:before,
.fa-exclamation-triangle:before {
  content: "\f071";
}
.fa-plane:before {
  content: "\f072";
}
.fa-calendar:before {
  content: "\f073";
}
.fa-random:before {
  content: "\f074";
}
.fa-comment:before {
  content: "\f075";
}
.fa-magnet:before {
  content: "\f076";
}
.fa-chevron-up:before {
  content: "\f077";
}
.fa-chevron-down:before {
  content: "\f078";
}
.fa-retweet:before {
  content: "\f079";
}
.fa-shopping-cart:before {
  content: "\f07a";
}
.fa-folder:before {
  content: "\f07b";
}
.fa-folder-open:before {
  content: "\f07c";
}
.fa-arrows-v:before {
  content: "\f07d";
}
.fa-arrows-h:before {
  content: "\f07e";
}
.fa-bar-chart-o:before,
.fa-bar-chart:before {
  content: "\f080";
}
.fa-twitter-square:before {
  content: "\f081";
}
.fa-facebook-square:before {
  content: "\f082";
}
.fa-camera-retro:before {
  content: "\f083";
}
.fa-key:before {
  content: "\f084";
}
.fa-gears:before,
.fa-cogs:before {
  content: "\f085";
}
.fa-comments:before {
  content: "\f086";
}
.fa-thumbs-o-up:before {
  content: "\f087";
}
.fa-thumbs-o-down:before {
  content: "\f088";
}
.fa-star-half:before {
  content: "\f089";
}
.fa-heart-o:before {
  content: "\f08a";
}
.fa-sign-out:before {
  content: "\f08b";
}
.fa-linkedin-square:before {
  content: "\f08c";
}
.fa-thumb-tack:before {
  content: "\f08d";
}
.fa-external-link:before {
  content: "\f08e";
}
.fa-sign-in:before {
  content: "\f090";
}
.fa-trophy:before {
  content: "\f091";
}
.fa-github-square:before {
  content: "\f092";
}
.fa-upload:before {
  content: "\f093";
}
.fa-lemon-o:before {
  content: "\f094";
}
.fa-phone:before {
  content: "\f095";
}
.fa-square-o:before {
  content: "\f096";
}
.fa-bookmark-o:before {
  content: "\f097";
}
.fa-phone-square:before {
  content: "\f098";
}
.fa-twitter:before {
  content: "\f099";
}
.fa-facebook-f:before,
.fa-facebook:before {
  content: "\f09a";
}
.fa-github:before {
  content: "\f09b";
}
.fa-unlock:before {
  content: "\f09c";
}
.fa-credit-card:before {
  content: "\f09d";
}
.fa-feed:before,
.fa-rss:before {
  content: "\f09e";
}
.fa-hdd-o:before {
  content: "\f0a0";
}
.fa-bullhorn:before {
  content: "\f0a1";
}
.fa-bell:before {
  content: "\f0f3";
}
.fa-certificate:before {
  content: "\f0a3";
}
.fa-hand-o-right:before {
  content: "\f0a4";
}
.fa-hand-o-left:before {
  content: "\f0a5";
}
.fa-hand-o-up:before {
  content: "\f0a6";
}
.fa-hand-o-down:before {
  content: "\f0a7";
}
.fa-arrow-circle-left:before {
  content: "\f0a8";
}
.fa-arrow-circle-right:before {
  content: "\f0a9";
}
.fa-arrow-circle-up:before {
  content: "\f0aa";
}
.fa-arrow-circle-down:before {
  content: "\f0ab";
}
.fa-globe:before {
  content: "\f0ac";
}
.fa-wrench:before {
  content: "\f0ad";
}
.fa-tasks:before {
  content: "\f0ae";
}
.fa-filter:before {
  content: "\f0b0";
}
.fa-briefcase:before {
  content: "\f0b1";
}
.fa-arrows-alt:before {
  content: "\f0b2";
}
.fa-group:before,
.fa-users:before {
  content: "\f0c0";
}
.fa-chain:before,
.fa-link:before {
  content: "\f0c1";
}
.fa-cloud:before {
  content: "\f0c2";
}
.fa-flask:before {
  content: "\f0c3";
}
.fa-cut:before,
.fa-scissors:before {
  content: "\f0c4";
}
.fa-copy:before,
.fa-files-o:before {
  content: "\f0c5";
}
.fa-paperclip:before {
  content: "\f0c6";
}
.fa-save:before,
.fa-floppy-o:before {
  content: "\f0c7";
}
.fa-square:before {
  content: "\f0c8";
}
.fa-navicon:before,
.fa-reorder:before,
.fa-bars:before {
  content: "\f0c9";
}
.fa-list-ul:before {
  content: "\f0ca";
}
.fa-list-ol:before {
  content: "\f0cb";
}
.fa-strikethrough:before {
  content: "\f0cc";
}
.fa-underline:before {
  content: "\f0cd";
}
.fa-table:before {
  content: "\f0ce";
}
.fa-magic:before {
  content: "\f0d0";
}
.fa-truck:before {
  content: "\f0d1";
}
.fa-pinterest:before {
  content: "\f0d2";
}
.fa-pinterest-square:before {
  content: "\f0d3";
}
.fa-google-plus-square:before {
  content: "\f0d4";
}
.fa-google-plus:before {
  content: "\f0d5";
}
.fa-money:before {
  content: "\f0d6";
}
.fa-caret-down:before {
  content: "\f0d7";
}
.fa-caret-up:before {
  content: "\f0d8";
}
.fa-caret-left:before {
  content: "\f0d9";
}
.fa-caret-right:before {
  content: "\f0da";
}
.fa-columns:before {
  content: "\f0db";
}
.fa-unsorted:before,
.fa-sort:before {
  content: "\f0dc";
}
.fa-sort-down:before,
.fa-sort-desc:before {
  content: "\f0dd";
}
.fa-sort-up:before,
.fa-sort-asc:before {
  content: "\f0de";
}
.fa-envelope:before {
  content: "\f0e0";
}
.fa-linkedin:before {
  content: "\f0e1";
}
.fa-rotate-left:before,
.fa-undo:before {
  content: "\f0e2";
}
.fa-legal:before,
.fa-gavel:before {
  content: "\f0e3";
}
.fa-dashboard:before,
.fa-tachometer:before {
  content: "\f0e4";
}
.fa-comment-o:before {
  content: "\f0e5";
}
.fa-comments-o:before {
  content: "\f0e6";
}
.fa-flash:before,
.fa-bolt:before {
  content: "\f0e7";
}
.fa-sitemap:before {
  content: "\f0e8";
}
.fa-umbrella:before {
  content: "\f0e9";
}
.fa-paste:before,
.fa-clipboard:before {
  content: "\f0ea";
}
.fa-lightbulb-o:before {
  content: "\f0eb";
}
.fa-exchange:before {
  content: "\f0ec";
}
.fa-cloud-download:before {
  content: "\f0ed";
}
.fa-cloud-upload:before {
  content: "\f0ee";
}
.fa-user-md:before {
  content: "\f0f0";
}
.fa-stethoscope:before {
  content: "\f0f1";
}
.fa-suitcase:before {
  content: "\f0f2";
}
.fa-bell-o:before {
  content: "\f0a2";
}
.fa-coffee:before {
  content: "\f0f4";
}
.fa-cutlery:before {
  content: "\f0f5";
}
.fa-file-text-o:before {
  content: "\f0f6";
}
.fa-building-o:before {
  content: "\f0f7";
}
.fa-hospital-o:before {
  content: "\f0f8";
}
.fa-ambulance:before {
  content: "\f0f9";
}
.fa-medkit:before {
  content: "\f0fa";
}
.fa-fighter-jet:before {
  content: "\f0fb";
}
.fa-beer:before {
  content: "\f0fc";
}
.fa-h-square:before {
  content: "\f0fd";
}
.fa-plus-square:before {
  content: "\f0fe";
}
.fa-angle-double-left:before {
  content: "\f100";
}
.fa-angle-double-right:before {
  content: "\f101";
}
.fa-angle-double-up:before {
  content: "\f102";
}
.fa-angle-double-down:before {
  content: "\f103";
}
.fa-angle-left:before {
  content: "\f104";
}
.fa-angle-right:before {
  content: "\f105";
}
.fa-angle-up:before {
  content: "\f106";
}
.fa-angle-down:before {
  content: "\f107";
}
.fa-desktop:before {
  content: "\f108";
}
.fa-laptop:before {
  content: "\f109";
}
.fa-tablet:before {
  content: "\f10a";
}
.fa-mobile-phone:before,
.fa-mobile:before {
  content: "\f10b";
}
.fa-circle-o:before {
  content: "\f10c";
}
.fa-quote-left:before {
  content: "\f10d";
}
.fa-quote-right:before {
  content: "\f10e";
}
.fa-spinner:before {
  content: "\f110";
}
.fa-circle:before {
  content: "\f111";
}
.fa-mail-reply:before,
.fa-reply:before {
  content: "\f112";
}
.fa-github-alt:before {
  content: "\f113";
}
.fa-folder-o:before {
  content: "\f114";
}
.fa-folder-open-o:before {
  content: "\f115";
}
.fa-smile-o:before {
  content: "\f118";
}
.fa-frown-o:before {
  content: "\f119";
}
.fa-meh-o:before {
  content: "\f11a";
}
.fa-gamepad:before {
  content: "\f11b";
}
.fa-keyboard-o:before {
  content: "\f11c";
}
.fa-flag-o:before {
  content: "\f11d";
}
.fa-flag-checkered:before {
  content: "\f11e";
}
.fa-terminal:before {
  content: "\f120";
}
.fa-code:before {
  content: "\f121";
}
.fa-mail-reply-all:before,
.fa-reply-all:before {
  content: "\f122";
}
.fa-star-half-empty:before,
.fa-star-half-full:before,
.fa-star-half-o:before {
  content: "\f123";
}
.fa-location-arrow:before {
  content: "\f124";
}
.fa-crop:before {
  content: "\f125";
}
.fa-code-fork:before {
  content: "\f126";
}
.fa-unlink:before,
.fa-chain-broken:before {
  content: "\f127";
}
.fa-question:before {
  content: "\f128";
}
.fa-info:before {
  content: "\f129";
}
.fa-exclamation:before {
  content: "\f12a";
}
.fa-superscript:before {
  content: "\f12b";
}
.fa-subscript:before {
  content: "\f12c";
}
.fa-eraser:before {
  content: "\f12d";
}
.fa-puzzle-piece:before {
  content: "\f12e";
}
.fa-microphone:before {
  content: "\f130";
}
.fa-microphone-slash:before {
  content: "\f131";
}
.fa-shield:before {
  content: "\f132";
}
.fa-calendar-o:before {
  content: "\f133";
}
.fa-fire-extinguisher:before {
  content: "\f134";
}
.fa-rocket:before {
  content: "\f135";
}
.fa-maxcdn:before {
  content: "\f136";
}
.fa-chevron-circle-left:before {
  content: "\f137";
}
.fa-chevron-circle-right:before {
  content: "\f138";
}
.fa-chevron-circle-up:before {
  content: "\f139";
}
.fa-chevron-circle-down:before {
  content: "\f13a";
}
.fa-html5:before {
  content: "\f13b";
}
.fa-css3:before {
  content: "\f13c";
}
.fa-anchor:before {
  content: "\f13d";
}
.fa-unlock-alt:before {
  content: "\f13e";
}
.fa-bullseye:before {
  content: "\f140";
}
.fa-ellipsis-h:before {
  content: "\f141";
}
.fa-ellipsis-v:before {
  content: "\f142";
}
.fa-rss-square:before {
  content: "\f143";
}
.fa-play-circle:before {
  content: "\f144";
}
.fa-ticket:before {
  content: "\f145";
}
.fa-minus-square:before {
  content: "\f146";
}
.fa-minus-square-o:before {
  content: "\f147";
}
.fa-level-up:before {
  content: "\f148";
}
.fa-level-down:before {
  content: "\f149";
}
.fa-check-square:before {
  content: "\f14a";
}
.fa-pencil-square:before {
  content: "\f14b";
}
.fa-external-link-square:before {
  content: "\f14c";
}
.fa-share-square:before {
  content: "\f14d";
}
.fa-compass:before {
  content: "\f14e";
}
.fa-toggle-down:before,
.fa-caret-square-o-down:before {
  content: "\f150";
}
.fa-toggle-up:before,
.fa-caret-square-o-up:before {
  content: "\f151";
}
.fa-toggle-right:before,
.fa-caret-square-o-right:before {
  content: "\f152";
}
.fa-euro:before,
.fa-eur:before {
  content: "\f153";
}
.fa-gbp:before {
  content: "\f154";
}
.fa-dollar:before,
.fa-usd:before {
  content: "\f155";
}
.fa-rupee:before,
.fa-inr:before {
  content: "\f156";
}
.fa-cny:before,
.fa-rmb:before,
.fa-yen:before,
.fa-jpy:before {
  content: "\f157";
}
.fa-ruble:before,
.fa-rouble:before,
.fa-rub:before {
  content: "\f158";
}
.fa-won:before,
.fa-krw:before {
  content: "\f159";
}
.fa-bitcoin:before,
.fa-btc:before {
  content: "\f15a";
}
.fa-file:before {
  content: "\f15b";
}
.fa-file-text:before {
  content: "\f15c";
}
.fa-sort-alpha-asc:before {
  content: "\f15d";
}
.fa-sort-alpha-desc:before {
  content: "\f15e";
}
.fa-sort-amount-asc:before {
  content: "\f160";
}
.fa-sort-amount-desc:before {
  content: "\f161";
}
.fa-sort-numeric-asc:before {
  content: "\f162";
}
.fa-sort-numeric-desc:before {
  content: "\f163";
}
.fa-thumbs-up:before {
  content: "\f164";
}
.fa-thumbs-down:before {
  content: "\f165";
}
.fa-youtube-square:before {
  content: "\f166";
}
.fa-youtube:before {
  content: "\f167";
}
.fa-xing:before {
  content: "\f168";
}
.fa-xing-square:before {
  content: "\f169";
}
.fa-youtube-play:before {
  content: "\f16a";
}
.fa-dropbox:before {
  content: "\f16b";
}
.fa-stack-overflow:before {
  content: "\f16c";
}
.fa-instagram:before {
  content: "\f16d";
}
.fa-flickr:before {
  content: "\f16e";
}
.fa-adn:before {
  content: "\f170";
}
.fa-bitbucket:before {
  content: "\f171";
}
.fa-bitbucket-square:before {
  content: "\f172";
}
.fa-tumblr:before {
  content: "\f173";
}
.fa-tumblr-square:before {
  content: "\f174";
}
.fa-long-arrow-down:before {
  content: "\f175";
}
.fa-long-arrow-up:before {
  content: "\f176";
}
.fa-long-arrow-left:before {
  content: "\f177";
}
.fa-long-arrow-right:before {
  content: "\f178";
}
.fa-apple:before {
  content: "\f179";
}
.fa-windows:before {
  content: "\f17a";
}
.fa-android:before {
  content: "\f17b";
}
.fa-linux:before {
  content: "\f17c";
}
.fa-dribbble:before {
  content: "\f17d";
}
.fa-skype:before {
  content: "\f17e";
}
.fa-foursquare:before {
  content: "\f180";
}
.fa-trello:before {
  content: "\f181";
}
.fa-female:before {
  content: "\f182";
}
.fa-male:before {
  content: "\f183";
}
.fa-gittip:before,
.fa-gratipay:before {
  content: "\f184";
}
.fa-sun-o:before {
  content: "\f185";
}
.fa-moon-o:before {
  content: "\f186";
}
.fa-archive:before {
  content: "\f187";
}
.fa-bug:before {
  content: "\f188";
}
.fa-vk:before {
  content: "\f189";
}
.fa-weibo:before {
  content: "\f18a";
}
.fa-renren:before {
  content: "\f18b";
}
.fa-pagelines:before {
  content: "\f18c";
}
.fa-stack-exchange:before {
  content: "\f18d";
}
.fa-arrow-circle-o-right:before {
  content: "\f18e";
}
.fa-arrow-circle-o-left:before {
  content: "\f190";
}
.fa-toggle-left:before,
.fa-caret-square-o-left:before {
  content: "\f191";
}
.fa-dot-circle-o:before {
  content: "\f192";
}
.fa-wheelchair:before {
  content: "\f193";
}
.fa-vimeo-square:before {
  content: "\f194";
}
.fa-turkish-lira:before,
.fa-try:before {
  content: "\f195";
}
.fa-plus-square-o:before {
  content: "\f196";
}
.fa-space-shuttle:before {
  content: "\f197";
}
.fa-slack:before {
  content: "\f198";
}
.fa-envelope-square:before {
  content: "\f199";
}
.fa-wordpress:before {
  content: "\f19a";
}
.fa-openid:before {
  content: "\f19b";
}
.fa-institution:before,
.fa-bank:before,
.fa-university:before {
  content: "\f19c";
}
.fa-mortar-board:before,
.fa-graduation-cap:before {
  content: "\f19d";
}
.fa-yahoo:before {
  content: "\f19e";
}
.fa-google:before {
  content: "\f1a0";
}
.fa-reddit:before {
  content: "\f1a1";
}
.fa-reddit-square:before {
  content: "\f1a2";
}
.fa-stumbleupon-circle:before {
  content: "\f1a3";
}
.fa-stumbleupon:before {
  content: "\f1a4";
}
.fa-delicious:before {
  content: "\f1a5";
}
.fa-digg:before {
  content: "\f1a6";
}
.fa-pied-piper-pp:before {
  content: "\f1a7";
}
.fa-pied-piper-alt:before {
  content: "\f1a8";
}
.fa-drupal:before {
  content: "\f1a9";
}
.fa-joomla:before {
  content: "\f1aa";
}
.fa-language:before {
  content: "\f1ab";
}
.fa-fax:before {
  content: "\f1ac";
}
.fa-building:before {
  content: "\f1ad";
}
.fa-child:before {
  content: "\f1ae";
}
.fa-paw:before {
  content: "\f1b0";
}
.fa-spoon:before {
  content: "\f1b1";
}
.fa-cube:before {
  content: "\f1b2";
}
.fa-cubes:before {
  content: "\f1b3";
}
.fa-behance:before {
  content: "\f1b4";
}
.fa-behance-square:before {
  content: "\f1b5";
}
.fa-steam:before {
  content: "\f1b6";
}
.fa-steam-square:before {
  content: "\f1b7";
}
.fa-recycle:before {
  content: "\f1b8";
}
.fa-automobile:before,
.fa-car:before {
  content: "\f1b9";
}
.fa-cab:before,
.fa-taxi:before {
  content: "\f1ba";
}
.fa-tree:before {
  content: "\f1bb";
}
.fa-spotify:before {
  content: "\f1bc";
}
.fa-deviantart:before {
  content: "\f1bd";
}
.fa-soundcloud:before {
  content: "\f1be";
}
.fa-database:before {
  content: "\f1c0";
}
.fa-file-pdf-o:before {
  content: "\f1c1";
}
.fa-file-word-o:before {
  content: "\f1c2";
}
.fa-file-excel-o:before {
  content: "\f1c3";
}
.fa-file-powerpoint-o:before {
  content: "\f1c4";
}
.fa-file-photo-o:before,
.fa-file-picture-o:before,
.fa-file-image-o:before {
  content: "\f1c5";
}
.fa-file-zip-o:before,
.fa-file-archive-o:before {
  content: "\f1c6";
}
.fa-file-sound-o:before,
.fa-file-audio-o:before {
  content: "\f1c7";
}
.fa-file-movie-o:before,
.fa-file-video-o:before {
  content: "\f1c8";
}
.fa-file-code-o:before {
  content: "\f1c9";
}
.fa-vine:before {
  content: "\f1ca";
}
.fa-codepen:before {
  content: "\f1cb";
}
.fa-jsfiddle:before {
  content: "\f1cc";
}
.fa-life-bouy:before,
.fa-life-buoy:before,
.fa-life-saver:before,
.fa-support:before,
.fa-life-ring:before {
  content: "\f1cd";
}
.fa-circle-o-notch:before {
  content: "\f1ce";
}
.fa-ra:before,
.fa-resistance:before,
.fa-rebel:before {
  content: "\f1d0";
}
.fa-ge:before,
.fa-empire:before {
  content: "\f1d1";
}
.fa-git-square:before {
  content: "\f1d2";
}
.fa-git:before {
  content: "\f1d3";
}
.fa-y-combinator-square:before,
.fa-yc-square:before,
.fa-hacker-news:before {
  content: "\f1d4";
}
.fa-tencent-weibo:before {
  content: "\f1d5";
}
.fa-qq:before {
  content: "\f1d6";
}
.fa-wechat:before,
.fa-weixin:before {
  content: "\f1d7";
}
.fa-send:before,
.fa-paper-plane:before {
  content: "\f1d8";
}
.fa-send-o:before,
.fa-paper-plane-o:before {
  content: "\f1d9";
}
.fa-history:before {
  content: "\f1da";
}
.fa-circle-thin:before {
  content: "\f1db";
}
.fa-header:before {
  content: "\f1dc";
}
.fa-paragraph:before {
  content: "\f1dd";
}
.fa-sliders:before {
  content: "\f1de";
}
.fa-share-alt:before {
  content: "\f1e0";
}
.fa-share-alt-square:before {
  content: "\f1e1";
}
.fa-bomb:before {
  content: "\f1e2";
}
.fa-soccer-ball-o:before,
.fa-futbol-o:before {
  content: "\f1e3";
}
.fa-tty:before {
  content: "\f1e4";
}
.fa-binoculars:before {
  content: "\f1e5";
}
.fa-plug:before {
  content: "\f1e6";
}
.fa-slideshare:before {
  content: "\f1e7";
}
.fa-twitch:before {
  content: "\f1e8";
}
.fa-yelp:before {
  content: "\f1e9";
}
.fa-newspaper-o:before {
  content: "\f1ea";
}
.fa-wifi:before {
  content: "\f1eb";
}
.fa-calculator:before {
  content: "\f1ec";
}
.fa-paypal:before {
  content: "\f1ed";
}
.fa-google-wallet:before {
  content: "\f1ee";
}
.fa-cc-visa:before {
  content: "\f1f0";
}
.fa-cc-mastercard:before {
  content: "\f1f1";
}
.fa-cc-discover:before {
  content: "\f1f2";
}
.fa-cc-amex:before {
  content: "\f1f3";
}
.fa-cc-paypal:before {
  content: "\f1f4";
}
.fa-cc-stripe:before {
  content: "\f1f5";
}
.fa-bell-slash:before {
  content: "\f1f6";
}
.fa-bell-slash-o:before {
  content: "\f1f7";
}
.fa-trash:before {
  content: "\f1f8";
}
.fa-copyright:before {
  content: "\f1f9";
}
.fa-at:before {
  content: "\f1fa";
}
.fa-eyedropper:before {
  content: "\f1fb";
}
.fa-paint-brush:before {
  content: "\f1fc";
}
.fa-birthday-cake:before {
  content: "\f1fd";
}
.fa-area-chart:before {
  content: "\f1fe";
}
.fa-pie-chart:before {
  content: "\f200";
}
.fa-line-chart:before {
  content: "\f201";
}
.fa-lastfm:before {
  content: "\f202";
}
.fa-lastfm-square:before {
  content: "\f203";
}
.fa-toggle-off:before {
  content: "\f204";
}
.fa-toggle-on:before {
  content: "\f205";
}
.fa-bicycle:before {
  content: "\f206";
}
.fa-bus:before {
  content: "\f207";
}
.fa-ioxhost:before {
  content: "\f208";
}
.fa-angellist:before {
  content: "\f209";
}
.fa-cc:before {
  content: "\f20a";
}
.fa-shekel:before,
.fa-sheqel:before,
.fa-ils:before {
  content: "\f20b";
}
.fa-meanpath:before {
  content: "\f20c";
}
.fa-buysellads:before {
  content: "\f20d";
}
.fa-connectdevelop:before {
  content: "\f20e";
}
.fa-dashcube:before {
  content: "\f210";
}
.fa-forumbee:before {
  content: "\f211";
}
.fa-leanpub:before {
  content: "\f212";
}
.fa-sellsy:before {
  content: "\f213";
}
.fa-shirtsinbulk:before {
  content: "\f214";
}
.fa-simplybuilt:before {
  content: "\f215";
}
.fa-skyatlas:before {
  content: "\f216";
}
.fa-cart-plus:before {
  content: "\f217";
}
.fa-cart-arrow-down:before {
  content: "\f218";
}
.fa-diamond:before {
  content: "\f219";
}
.fa-ship:before {
  content: "\f21a";
}
.fa-user-secret:before {
  content: "\f21b";
}
.fa-motorcycle:before {
  content: "\f21c";
}
.fa-street-view:before {
  content: "\f21d";
}
.fa-heartbeat:before {
  content: "\f21e";
}
.fa-venus:before {
  content: "\f221";
}
.fa-mars:before {
  content: "\f222";
}
.fa-mercury:before {
  content: "\f223";
}
.fa-intersex:before,
.fa-transgender:before {
  content: "\f224";
}
.fa-transgender-alt:before {
  content: "\f225";
}
.fa-venus-double:before {
  content: "\f226";
}
.fa-mars-double:before {
  content: "\f227";
}
.fa-venus-mars:before {
  content: "\f228";
}
.fa-mars-stroke:before {
  content: "\f229";
}
.fa-mars-stroke-v:before {
  content: "\f22a";
}
.fa-mars-stroke-h:before {
  content: "\f22b";
}
.fa-neuter:before {
  content: "\f22c";
}
.fa-genderless:before {
  content: "\f22d";
}
.fa-facebook-official:before {
  content: "\f230";
}
.fa-pinterest-p:before {
  content: "\f231";
}
.fa-whatsapp:before {
  content: "\f232";
}
.fa-server:before {
  content: "\f233";
}
.fa-user-plus:before {
  content: "\f234";
}
.fa-user-times:before {
  content: "\f235";
}
.fa-hotel:before,
.fa-bed:before {
  content: "\f236";
}
.fa-viacoin:before {
  content: "\f237";
}
.fa-train:before {
  content: "\f238";
}
.fa-subway:before {
  content: "\f239";
}
.fa-medium:before {
  content: "\f23a";
}
.fa-yc:before,
.fa-y-combinator:before {
  content: "\f23b";
}
.fa-optin-monster:before {
  content: "\f23c";
}
.fa-opencart:before {
  content: "\f23d";
}
.fa-expeditedssl:before {
  content: "\f23e";
}
.fa-battery-4:before,
.fa-battery:before,
.fa-battery-full:before {
  content: "\f240";
}
.fa-battery-3:before,
.fa-battery-three-quarters:before {
  content: "\f241";
}
.fa-battery-2:before,
.fa-battery-half:before {
  content: "\f242";
}
.fa-battery-1:before,
.fa-battery-quarter:before {
  content: "\f243";
}
.fa-battery-0:before,
.fa-battery-empty:before {
  content: "\f244";
}
.fa-mouse-pointer:before {
  content: "\f245";
}
.fa-i-cursor:before {
  content: "\f246";
}
.fa-object-group:before {
  content: "\f247";
}
.fa-object-ungroup:before {
  content: "\f248";
}
.fa-sticky-note:before {
  content: "\f249";
}
.fa-sticky-note-o:before {
  content: "\f24a";
}
.fa-cc-jcb:before {
  content: "\f24b";
}
.fa-cc-diners-club:before {
  content: "\f24c";
}
.fa-clone:before {
  content: "\f24d";
}
.fa-balance-scale:before {
  content: "\f24e";
}
.fa-hourglass-o:before {
  content: "\f250";
}
.fa-hourglass-1:before,
.fa-hourglass-start:before {
  content: "\f251";
}
.fa-hourglass-2:before,
.fa-hourglass-half:before {
  content: "\f252";
}
.fa-hourglass-3:before,
.fa-hourglass-end:before {
  content: "\f253";
}
.fa-hourglass:before {
  content: "\f254";
}
.fa-hand-grab-o:before,
.fa-hand-rock-o:before {
  content: "\f255";
}
.fa-hand-stop-o:before,
.fa-hand-paper-o:before {
  content: "\f256";
}
.fa-hand-scissors-o:before {
  content: "\f257";
}
.fa-hand-lizard-o:before {
  content: "\f258";
}
.fa-hand-spock-o:before {
  content: "\f259";
}
.fa-hand-pointer-o:before {
  content: "\f25a";
}
.fa-hand-peace-o:before {
  content: "\f25b";
}
.fa-trademark:before {
  content: "\f25c";
}
.fa-registered:before {
  content: "\f25d";
}
.fa-creative-commons:before {
  content: "\f25e";
}
.fa-gg:before {
  content: "\f260";
}
.fa-gg-circle:before {
  content: "\f261";
}
.fa-tripadvisor:before {
  content: "\f262";
}
.fa-odnoklassniki:before {
  content: "\f263";
}
.fa-odnoklassniki-square:before {
  content: "\f264";
}
.fa-get-pocket:before {
  content: "\f265";
}
.fa-wikipedia-w:before {
  content: "\f266";
}
.fa-safari:before {
  content: "\f267";
}
.fa-chrome:before {
  content: "\f268";
}
.fa-firefox:before {
  content: "\f269";
}
.fa-opera:before {
  content: "\f26a";
}
.fa-internet-explorer:before {
  content: "\f26b";
}
.fa-tv:before,
.fa-television:before {
  content: "\f26c";
}
.fa-contao:before {
  content: "\f26d";
}
.fa-500px:before {
  content: "\f26e";
}
.fa-amazon:before {
  content: "\f270";
}
.fa-calendar-plus-o:before {
  content: "\f271";
}
.fa-calendar-minus-o:before {
  content: "\f272";
}
.fa-calendar-times-o:before {
  content: "\f273";
}
.fa-calendar-check-o:before {
  content: "\f274";
}
.fa-industry:before {
  content: "\f275";
}
.fa-map-pin:before {
  content: "\f276";
}
.fa-map-signs:before {
  content: "\f277";
}
.fa-map-o:before {
  content: "\f278";
}
.fa-map:before {
  content: "\f279";
}
.fa-commenting:before {
  content: "\f27a";
}
.fa-commenting-o:before {
  content: "\f27b";
}
.fa-houzz:before {
  content: "\f27c";
}
.fa-vimeo:before {
  content: "\f27d";
}
.fa-black-tie:before {
  content: "\f27e";
}
.fa-fonticons:before {
  content: "\f280";
}
.fa-reddit-alien:before {
  content: "\f281";
}
.fa-edge:before {
  content: "\f282";
}
.fa-credit-card-alt:before {
  content: "\f283";
}
.fa-codiepie:before {
  content: "\f284";
}
.fa-modx:before {
  content: "\f285";
}
.fa-fort-awesome:before {
  content: "\f286";
}
.fa-usb:before {
  content: "\f287";
}
.fa-product-hunt:before {
  content: "\f288";
}
.fa-mixcloud:before {
  content: "\f289";
}
.fa-scribd:before {
  content: "\f28a";
}
.fa-pause-circle:before {
  content: "\f28b";
}
.fa-pause-circle-o:before {
  content: "\f28c";
}
.fa-stop-circle:before {
  content: "\f28d";
}
.fa-stop-circle-o:before {
  content: "\f28e";
}
.fa-shopping-bag:before {
  content: "\f290";
}
.fa-shopping-basket:before {
  content: "\f291";
}
.fa-hashtag:before {
  content: "\f292";
}
.fa-bluetooth:before {
  content: "\f293";
}
.fa-bluetooth-b:before {
  content: "\f294";
}
.fa-percent:before {
  content: "\f295";
}
.fa-gitlab:before {
  content: "\f296";
}
.fa-wpbeginner:before {
  content: "\f297";
}
.fa-wpforms:before {
  content: "\f298";
}
.fa-envira:before {
  content: "\f299";
}
.fa-universal-access:before {
  content: "\f29a";
}
.fa-wheelchair-alt:before {
  content: "\f29b";
}
.fa-question-circle-o:before {
  content: "\f29c";
}
.fa-blind:before {
  content: "\f29d";
}
.fa-audio-description:before {
  content: "\f29e";
}
.fa-volume-control-phone:before {
  content: "\f2a0";
}
.fa-braille:before {
  content: "\f2a1";
}
.fa-assistive-listening-systems:before {
  content: "\f2a2";
}
.fa-asl-interpreting:before,
.fa-american-sign-language-interpreting:before {
  content: "\f2a3";
}
.fa-deafness:before,
.fa-hard-of-hearing:before,
.fa-deaf:before {
  content: "\f2a4";
}
.fa-glide:before {
  content: "\f2a5";
}
.fa-glide-g:before {
  content: "\f2a6";
}
.fa-signing:before,
.fa-sign-language:before {
  content: "\f2a7";
}
.fa-low-vision:before {
  content: "\f2a8";
}
.fa-viadeo:before {
  content: "\f2a9";
}
.fa-viadeo-square:before {
  content: "\f2aa";
}
.fa-snapchat:before {
  content: "\f2ab";
}
.fa-snapchat-ghost:before {
  content: "\f2ac";
}
.fa-snapchat-square:before {
  content: "\f2ad";
}
.fa-pied-piper:before {
  content: "\f2ae";
}
.fa-first-order:before {
  content: "\f2b0";
}
.fa-yoast:before {
  content: "\f2b1";
}
.fa-themeisle:before {
  content: "\f2b2";
}
.fa-google-plus-circle:before,
.fa-google-plus-official:before {
  content: "\f2b3";
}
.fa-fa:before,
.fa-font-awesome:before {
  content: "\f2b4";
}
.fa-handshake-o:before {
  content: "\f2b5";
}
.fa-envelope-open:before {
  content: "\f2b6";
}
.fa-envelope-open-o:before {
  content: "\f2b7";
}
.fa-linode:before {
  content: "\f2b8";
}
.fa-address-book:before {
  content: "\f2b9";
}
.fa-address-book-o:before {
  content: "\f2ba";
}
.fa-vcard:before,
.fa-address-card:before {
  content: "\f2bb";
}
.fa-vcard-o:before,
.fa-address-card-o:before {
  content: "\f2bc";
}
.fa-user-circle:before {
  content: "\f2bd";
}
.fa-user-circle-o:before {
  content: "\f2be";
}
.fa-user-o:before {
  content: "\f2c0";
}
.fa-id-badge:before {
  content: "\f2c1";
}
.fa-drivers-license:before,
.fa-id-card:before {
  content: "\f2c2";
}
.fa-drivers-license-o:before,
.fa-id-card-o:before {
  content: "\f2c3";
}
.fa-quora:before {
  content: "\f2c4";
}
.fa-free-code-camp:before {
  content: "\f2c5";
}
.fa-telegram:before {
  content: "\f2c6";
}
.fa-thermometer-4:before,
.fa-thermometer:before,
.fa-thermometer-full:before {
  content: "\f2c7";
}
.fa-thermometer-3:before,
.fa-thermometer-three-quarters:before {
  content: "\f2c8";
}
.fa-thermometer-2:before,
.fa-thermometer-half:before {
  content: "\f2c9";
}
.fa-thermometer-1:before,
.fa-thermometer-quarter:before {
  content: "\f2ca";
}
.fa-thermometer-0:before,
.fa-thermometer-empty:before {
  content: "\f2cb";
}
.fa-shower:before {
  content: "\f2cc";
}
.fa-bathtub:before,
.fa-s15:before,
.fa-bath:before {
  content: "\f2cd";
}
.fa-podcast:before {
  content: "\f2ce";
}
.fa-window-maximize:before {
  content: "\f2d0";
}
.fa-window-minimize:before {
  content: "\f2d1";
}
.fa-window-restore:before {
  content: "\f2d2";
}
.fa-times-rectangle:before,
.fa-window-close:before {
  content: "\f2d3";
}
.fa-times-rectangle-o:before,
.fa-window-close-o:before {
  content: "\f2d4";
}
.fa-bandcamp:before {
  content: "\f2d5";
}
.fa-grav:before {
  content: "\f2d6";
}
.fa-etsy:before {
  content: "\f2d7";
}
.fa-imdb:before {
  content: "\f2d8";
}
.fa-ravelry:before {
  content: "\f2d9";
}
.fa-eercast:before {
  content: "\f2da";
}
.fa-microchip:before {
  content: "\f2db";
}
.fa-snowflake-o:before {
  content: "\f2dc";
}
.fa-superpowers:before {
  content: "\f2dd";
}
.fa-wpexplorer:before {
  content: "\f2de";
}
.fa-meetup:before {
  content: "\f2e0";
}
.sr-only {
  position: absolute;
  width: 1px;
  height: 1px;
  padding: 0;
  margin: -1px;
  overflow: hidden;
  clip: rect(0, 0, 0, 0);
  border: 0;
}
.sr-only-focusable:active,
.sr-only-focusable:focus {
  position: static;
  width: auto;
  height: auto;
  margin: 0;
  overflow: visible;
  clip: auto;
}
.sr-only-focusable:active,
.sr-only-focusable:focus {
  position: static;
  width: auto;
  height: auto;
  margin: 0;
  overflow: visible;
  clip: auto;
}
/*!
*
* IPython base
*
*/
.modal.fade .modal-dialog {
  -webkit-transform: translate(0, 0);
  -ms-transform: translate(0, 0);
  -o-transform: translate(0, 0);
  transform: translate(0, 0);
}
code {
  color: #000;
}
pre {
  font-size: inherit;
  line-height: inherit;
}
label {
  font-weight: normal;
}
/* Make the page background atleast 100% the height of the view port */
/* Make the page itself atleast 70% the height of the view port */
.border-box-sizing {
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
.corner-all {
  border-radius: 2px;
}
.no-padding {
  padding: 0px;
}
/* Flexible box model classes */
/* Taken from Alex Russell http://infrequently.org/2009/08/css-3-progress/ */
/* This file is a compatability layer.  It allows the usage of flexible box
model layouts accross multiple browsers, including older browsers.  The newest,
universal implementation of the flexible box model is used when available (see
`Modern browsers` comments below).  Browsers that are known to implement this
new spec completely include:

    Firefox 28.0+
    Chrome 29.0+
    Internet Explorer 11+
    Opera 17.0+

Browsers not listed, including Safari, are supported via the styling under the
`Old browsers` comments below.
*/
.hbox {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
.hbox > * {
  /* Old browsers */
  -webkit-box-flex: 0;
  -moz-box-flex: 0;
  box-flex: 0;
  /* Modern browsers */
  flex: none;
}
.vbox {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
}
.vbox > * {
  /* Old browsers */
  -webkit-box-flex: 0;
  -moz-box-flex: 0;
  box-flex: 0;
  /* Modern browsers */
  flex: none;
}
.hbox.reverse,
.vbox.reverse,
.reverse {
  /* Old browsers */
  -webkit-box-direction: reverse;
  -moz-box-direction: reverse;
  box-direction: reverse;
  /* Modern browsers */
  flex-direction: row-reverse;
}
.hbox.box-flex0,
.vbox.box-flex0,
.box-flex0 {
  /* Old browsers */
  -webkit-box-flex: 0;
  -moz-box-flex: 0;
  box-flex: 0;
  /* Modern browsers */
  flex: none;
  width: auto;
}
.hbox.box-flex1,
.vbox.box-flex1,
.box-flex1 {
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
}
.hbox.box-flex,
.vbox.box-flex,
.box-flex {
  /* Old browsers */
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
}
.hbox.box-flex2,
.vbox.box-flex2,
.box-flex2 {
  /* Old browsers */
  -webkit-box-flex: 2;
  -moz-box-flex: 2;
  box-flex: 2;
  /* Modern browsers */
  flex: 2;
}
.box-group1 {
  /*  Deprecated */
  -webkit-box-flex-group: 1;
  -moz-box-flex-group: 1;
  box-flex-group: 1;
}
.box-group2 {
  /* Deprecated */
  -webkit-box-flex-group: 2;
  -moz-box-flex-group: 2;
  box-flex-group: 2;
}
.hbox.start,
.vbox.start,
.start {
  /* Old browsers */
  -webkit-box-pack: start;
  -moz-box-pack: start;
  box-pack: start;
  /* Modern browsers */
  justify-content: flex-start;
}
.hbox.end,
.vbox.end,
.end {
  /* Old browsers */
  -webkit-box-pack: end;
  -moz-box-pack: end;
  box-pack: end;
  /* Modern browsers */
  justify-content: flex-end;
}
.hbox.center,
.vbox.center,
.center {
  /* Old browsers */
  -webkit-box-pack: center;
  -moz-box-pack: center;
  box-pack: center;
  /* Modern browsers */
  justify-content: center;
}
.hbox.baseline,
.vbox.baseline,
.baseline {
  /* Old browsers */
  -webkit-box-pack: baseline;
  -moz-box-pack: baseline;
  box-pack: baseline;
  /* Modern browsers */
  justify-content: baseline;
}
.hbox.stretch,
.vbox.stretch,
.stretch {
  /* Old browsers */
  -webkit-box-pack: stretch;
  -moz-box-pack: stretch;
  box-pack: stretch;
  /* Modern browsers */
  justify-content: stretch;
}
.hbox.align-start,
.vbox.align-start,
.align-start {
  /* Old browsers */
  -webkit-box-align: start;
  -moz-box-align: start;
  box-align: start;
  /* Modern browsers */
  align-items: flex-start;
}
.hbox.align-end,
.vbox.align-end,
.align-end {
  /* Old browsers */
  -webkit-box-align: end;
  -moz-box-align: end;
  box-align: end;
  /* Modern browsers */
  align-items: flex-end;
}
.hbox.align-center,
.vbox.align-center,
.align-center {
  /* Old browsers */
  -webkit-box-align: center;
  -moz-box-align: center;
  box-align: center;
  /* Modern browsers */
  align-items: center;
}
.hbox.align-baseline,
.vbox.align-baseline,
.align-baseline {
  /* Old browsers */
  -webkit-box-align: baseline;
  -moz-box-align: baseline;
  box-align: baseline;
  /* Modern browsers */
  align-items: baseline;
}
.hbox.align-stretch,
.vbox.align-stretch,
.align-stretch {
  /* Old browsers */
  -webkit-box-align: stretch;
  -moz-box-align: stretch;
  box-align: stretch;
  /* Modern browsers */
  align-items: stretch;
}
div.error {
  margin: 2em;
  text-align: center;
}
div.error > h1 {
  font-size: 500%;
  line-height: normal;
}
div.error > p {
  font-size: 200%;
  line-height: normal;
}
div.traceback-wrapper {
  text-align: left;
  max-width: 800px;
  margin: auto;
}
div.traceback-wrapper pre.traceback {
  max-height: 600px;
  overflow: auto;
}
/**
 * Primary styles
 *
 * Author: Jupyter Development Team
 */
body {
  background-color: #fff;
  /* This makes sure that the body covers the entire window and needs to
       be in a different element than the display: box in wrapper below */
  position: absolute;
  left: 0px;
  right: 0px;
  top: 0px;
  bottom: 0px;
  overflow: visible;
}
body > #header {
  /* Initially hidden to prevent FLOUC */
  display: none;
  background-color: #fff;
  /* Display over codemirror */
  position: relative;
  z-index: 100;
}
body > #header #header-container {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  padding: 5px;
  padding-bottom: 5px;
  padding-top: 5px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
body > #header .header-bar {
  width: 100%;
  height: 1px;
  background: #e7e7e7;
  margin-bottom: -1px;
}
@media print {
  body > #header {
    display: none !important;
  }
}
#header-spacer {
  width: 100%;
  visibility: hidden;
}
@media print {
  #header-spacer {
    display: none;
  }
}
#ipython_notebook {
  padding-left: 0px;
  padding-top: 1px;
  padding-bottom: 1px;
}
[dir="rtl"] #ipython_notebook {
  margin-right: 10px;
  margin-left: 0;
}
[dir="rtl"] #ipython_notebook.pull-left {
  float: right !important;
  float: right;
}
.flex-spacer {
  flex: 1;
}
#noscript {
  width: auto;
  padding-top: 16px;
  padding-bottom: 16px;
  text-align: center;
  font-size: 22px;
  color: red;
  font-weight: bold;
}
#ipython_notebook img {
  height: 28px;
}
#site {
  width: 100%;
  display: none;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  overflow: auto;
}
@media print {
  #site {
    height: auto !important;
  }
}
/* Smaller buttons */
.ui-button .ui-button-text {
  padding: 0.2em 0.8em;
  font-size: 77%;
}
input.ui-button {
  padding: 0.3em 0.9em;
}
span#kernel_logo_widget {
  margin: 0 10px;
}
span#login_widget {
  float: right;
}
[dir="rtl"] span#login_widget {
  float: left;
}
span#login_widget > .button,
#logout {
  color: #333;
  background-color: #fff;
  border-color: #ccc;
}
span#login_widget > .button:focus,
#logout:focus,
span#login_widget > .button.focus,
#logout.focus {
  color: #333;
  background-color: #e6e6e6;
  border-color: #8c8c8c;
}
span#login_widget > .button:hover,
#logout:hover {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
span#login_widget > .button:active,
#logout:active,
span#login_widget > .button.active,
#logout.active,
.open > .dropdown-togglespan#login_widget > .button,
.open > .dropdown-toggle#logout {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
span#login_widget > .button:active:hover,
#logout:active:hover,
span#login_widget > .button.active:hover,
#logout.active:hover,
.open > .dropdown-togglespan#login_widget > .button:hover,
.open > .dropdown-toggle#logout:hover,
span#login_widget > .button:active:focus,
#logout:active:focus,
span#login_widget > .button.active:focus,
#logout.active:focus,
.open > .dropdown-togglespan#login_widget > .button:focus,
.open > .dropdown-toggle#logout:focus,
span#login_widget > .button:active.focus,
#logout:active.focus,
span#login_widget > .button.active.focus,
#logout.active.focus,
.open > .dropdown-togglespan#login_widget > .button.focus,
.open > .dropdown-toggle#logout.focus {
  color: #333;
  background-color: #d4d4d4;
  border-color: #8c8c8c;
}
span#login_widget > .button:active,
#logout:active,
span#login_widget > .button.active,
#logout.active,
.open > .dropdown-togglespan#login_widget > .button,
.open > .dropdown-toggle#logout {
  background-image: none;
}
span#login_widget > .button.disabled:hover,
#logout.disabled:hover,
span#login_widget > .button[disabled]:hover,
#logout[disabled]:hover,
fieldset[disabled] span#login_widget > .button:hover,
fieldset[disabled] #logout:hover,
span#login_widget > .button.disabled:focus,
#logout.disabled:focus,
span#login_widget > .button[disabled]:focus,
#logout[disabled]:focus,
fieldset[disabled] span#login_widget > .button:focus,
fieldset[disabled] #logout:focus,
span#login_widget > .button.disabled.focus,
#logout.disabled.focus,
span#login_widget > .button[disabled].focus,
#logout[disabled].focus,
fieldset[disabled] span#login_widget > .button.focus,
fieldset[disabled] #logout.focus {
  background-color: #fff;
  border-color: #ccc;
}
span#login_widget > .button .badge,
#logout .badge {
  color: #fff;
  background-color: #333;
}
.nav-header {
  text-transform: none;
}
#header > span {
  margin-top: 10px;
}
.modal_stretch .modal-dialog {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
  min-height: 80vh;
}
.modal_stretch .modal-dialog .modal-body {
  max-height: calc(100vh - 200px);
  overflow: auto;
  flex: 1;
}
.modal-header {
  cursor: move;
}
@media (min-width: 768px) {
  .modal .modal-dialog {
    width: 700px;
  }
}
@media (min-width: 768px) {
  select.form-control {
    margin-left: 12px;
    margin-right: 12px;
  }
}
/*!
*
* IPython auth
*
*/
.center-nav {
  display: inline-block;
  margin-bottom: -4px;
}
[dir="rtl"] .center-nav form.pull-left {
  float: right !important;
  float: right;
}
[dir="rtl"] .center-nav .navbar-text {
  float: right;
}
[dir="rtl"] .navbar-inner {
  text-align: right;
}
[dir="rtl"] div.text-left {
  text-align: right;
}
/*!
*
* IPython tree view
*
*/
/* We need an invisible input field on top of the sentense*/
/* "Drag file onto the list ..." */
.alternate_upload {
  background-color: none;
  display: inline;
}
.alternate_upload.form {
  padding: 0;
  margin: 0;
}
.alternate_upload input.fileinput {
  position: absolute;
  display: block;
  width: 100%;
  height: 100%;
  overflow: hidden;
  cursor: pointer;
  opacity: 0;
  z-index: 2;
}
.alternate_upload .btn-xs > input.fileinput {
  margin: -1px -5px;
}
.alternate_upload .btn-upload {
  position: relative;
  height: 22px;
}
::-webkit-file-upload-button {
  cursor: pointer;
}
/**
 * Primary styles
 *
 * Author: Jupyter Development Team
 */
ul#tabs {
  margin-bottom: 4px;
}
ul#tabs a {
  padding-top: 6px;
  padding-bottom: 4px;
}
[dir="rtl"] ul#tabs.nav-tabs > li {
  float: right;
}
[dir="rtl"] ul#tabs.nav.nav-tabs {
  padding-right: 0;
}
ul.breadcrumb a:focus,
ul.breadcrumb a:hover {
  text-decoration: none;
}
ul.breadcrumb i.icon-home {
  font-size: 16px;
  margin-right: 4px;
}
ul.breadcrumb span {
  color: #5e5e5e;
}
.list_toolbar {
  padding: 4px 0 4px 0;
  vertical-align: middle;
}
.list_toolbar .tree-buttons {
  padding-top: 1px;
}
[dir="rtl"] .list_toolbar .tree-buttons .pull-right {
  float: left !important;
  float: left;
}
[dir="rtl"] .list_toolbar .col-sm-4,
[dir="rtl"] .list_toolbar .col-sm-8 {
  float: right;
}
.dynamic-buttons {
  padding-top: 3px;
  display: inline-block;
}
.list_toolbar [class*="span"] {
  min-height: 24px;
}
.list_header {
  font-weight: bold;
  background-color: #EEE;
}
.list_placeholder {
  font-weight: bold;
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 7px;
  padding-right: 7px;
}
.list_container {
  margin-top: 4px;
  margin-bottom: 20px;
  border: 1px solid #ddd;
  border-radius: 2px;
}
.list_container > div {
  border-bottom: 1px solid #ddd;
}
.list_container > div:hover .list-item {
  background-color: red;
}
.list_container > div:last-child {
  border: none;
}
.list_item:hover .list_item {
  background-color: #ddd;
}
.list_item a {
  text-decoration: none;
}
.list_item:hover {
  background-color: #fafafa;
}
.list_header > div,
.list_item > div {
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 7px;
  padding-right: 7px;
  line-height: 22px;
}
.list_header > div input,
.list_item > div input {
  margin-right: 7px;
  margin-left: 14px;
  vertical-align: text-bottom;
  line-height: 22px;
  position: relative;
  top: -1px;
}
.list_header > div .item_link,
.list_item > div .item_link {
  margin-left: -1px;
  vertical-align: baseline;
  line-height: 22px;
}
[dir="rtl"] .list_item > div input {
  margin-right: 0;
}
.new-file input[type=checkbox] {
  visibility: hidden;
}
.item_name {
  line-height: 22px;
  height: 24px;
}
.item_icon {
  font-size: 14px;
  color: #5e5e5e;
  margin-right: 7px;
  margin-left: 7px;
  line-height: 22px;
  vertical-align: baseline;
}
.item_modified {
  margin-right: 7px;
  margin-left: 7px;
}
[dir="rtl"] .item_modified.pull-right {
  float: left !important;
  float: left;
}
.item_buttons {
  line-height: 1em;
  margin-left: -5px;
}
.item_buttons .btn,
.item_buttons .btn-group,
.item_buttons .input-group {
  float: left;
}
.item_buttons > .btn,
.item_buttons > .btn-group,
.item_buttons > .input-group {
  margin-left: 5px;
}
.item_buttons .btn {
  min-width: 13ex;
}
.item_buttons .running-indicator {
  padding-top: 4px;
  color: #5cb85c;
}
.item_buttons .kernel-name {
  padding-top: 4px;
  color: #5bc0de;
  margin-right: 7px;
  float: left;
}
[dir="rtl"] .item_buttons.pull-right {
  float: left !important;
  float: left;
}
[dir="rtl"] .item_buttons .kernel-name {
  margin-left: 7px;
  float: right;
}
.toolbar_info {
  height: 24px;
  line-height: 24px;
}
.list_item input:not([type=checkbox]) {
  padding-top: 3px;
  padding-bottom: 3px;
  height: 22px;
  line-height: 14px;
  margin: 0px;
}
.highlight_text {
  color: blue;
}
#project_name {
  display: inline-block;
  padding-left: 7px;
  margin-left: -2px;
}
#project_name > .breadcrumb {
  padding: 0px;
  margin-bottom: 0px;
  background-color: transparent;
  font-weight: bold;
}
.sort_button {
  display: inline-block;
  padding-left: 7px;
}
[dir="rtl"] .sort_button.pull-right {
  float: left !important;
  float: left;
}
#tree-selector {
  padding-right: 0px;
}
#button-select-all {
  min-width: 50px;
}
[dir="rtl"] #button-select-all.btn {
  float: right ;
}
#select-all {
  margin-left: 7px;
  margin-right: 2px;
  margin-top: 2px;
  height: 16px;
}
[dir="rtl"] #select-all.pull-left {
  float: right !important;
  float: right;
}
.menu_icon {
  margin-right: 2px;
}
.tab-content .row {
  margin-left: 0px;
  margin-right: 0px;
}
.folder_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f114";
}
.folder_icon:before.fa-pull-left {
  margin-right: .3em;
}
.folder_icon:before.fa-pull-right {
  margin-left: .3em;
}
.folder_icon:before.pull-left {
  margin-right: .3em;
}
.folder_icon:before.pull-right {
  margin-left: .3em;
}
.notebook_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f02d";
  position: relative;
  top: -1px;
}
.notebook_icon:before.fa-pull-left {
  margin-right: .3em;
}
.notebook_icon:before.fa-pull-right {
  margin-left: .3em;
}
.notebook_icon:before.pull-left {
  margin-right: .3em;
}
.notebook_icon:before.pull-right {
  margin-left: .3em;
}
.running_notebook_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f02d";
  position: relative;
  top: -1px;
  color: #5cb85c;
}
.running_notebook_icon:before.fa-pull-left {
  margin-right: .3em;
}
.running_notebook_icon:before.fa-pull-right {
  margin-left: .3em;
}
.running_notebook_icon:before.pull-left {
  margin-right: .3em;
}
.running_notebook_icon:before.pull-right {
  margin-left: .3em;
}
.file_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f016";
  position: relative;
  top: -2px;
}
.file_icon:before.fa-pull-left {
  margin-right: .3em;
}
.file_icon:before.fa-pull-right {
  margin-left: .3em;
}
.file_icon:before.pull-left {
  margin-right: .3em;
}
.file_icon:before.pull-right {
  margin-left: .3em;
}
#notebook_toolbar .pull-right {
  padding-top: 0px;
  margin-right: -1px;
}
ul#new-menu {
  left: auto;
  right: 0;
}
#new-menu .dropdown-header {
  font-size: 10px;
  border-bottom: 1px solid #e5e5e5;
  padding: 0 0 3px;
  margin: -3px 20px 0;
}
.kernel-menu-icon {
  padding-right: 12px;
  width: 24px;
  content: "\f096";
}
.kernel-menu-icon:before {
  content: "\f096";
}
.kernel-menu-icon-current:before {
  content: "\f00c";
}
#tab_content {
  padding-top: 20px;
}
#running .panel-group .panel {
  margin-top: 3px;
  margin-bottom: 1em;
}
#running .panel-group .panel .panel-heading {
  background-color: #EEE;
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 7px;
  padding-right: 7px;
  line-height: 22px;
}
#running .panel-group .panel .panel-heading a:focus,
#running .panel-group .panel .panel-heading a:hover {
  text-decoration: none;
}
#running .panel-group .panel .panel-body {
  padding: 0px;
}
#running .panel-group .panel .panel-body .list_container {
  margin-top: 0px;
  margin-bottom: 0px;
  border: 0px;
  border-radius: 0px;
}
#running .panel-group .panel .panel-body .list_container .list_item {
  border-bottom: 1px solid #ddd;
}
#running .panel-group .panel .panel-body .list_container .list_item:last-child {
  border-bottom: 0px;
}
.delete-button {
  display: none;
}
.duplicate-button {
  display: none;
}
.rename-button {
  display: none;
}
.move-button {
  display: none;
}
.download-button {
  display: none;
}
.shutdown-button {
  display: none;
}
.dynamic-instructions {
  display: inline-block;
  padding-top: 4px;
}
/*!
*
* IPython text editor webapp
*
*/
.selected-keymap i.fa {
  padding: 0px 5px;
}
.selected-keymap i.fa:before {
  content: "\f00c";
}
#mode-menu {
  overflow: auto;
  max-height: 20em;
}
.edit_app #header {
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
}
.edit_app #menubar .navbar {
  /* Use a negative 1 bottom margin, so the border overlaps the border of the
    header */
  margin-bottom: -1px;
}
.dirty-indicator {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  width: 20px;
}
.dirty-indicator.fa-pull-left {
  margin-right: .3em;
}
.dirty-indicator.fa-pull-right {
  margin-left: .3em;
}
.dirty-indicator.pull-left {
  margin-right: .3em;
}
.dirty-indicator.pull-right {
  margin-left: .3em;
}
.dirty-indicator-dirty {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  width: 20px;
}
.dirty-indicator-dirty.fa-pull-left {
  margin-right: .3em;
}
.dirty-indicator-dirty.fa-pull-right {
  margin-left: .3em;
}
.dirty-indicator-dirty.pull-left {
  margin-right: .3em;
}
.dirty-indicator-dirty.pull-right {
  margin-left: .3em;
}
.dirty-indicator-clean {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  width: 20px;
}
.dirty-indicator-clean.fa-pull-left {
  margin-right: .3em;
}
.dirty-indicator-clean.fa-pull-right {
  margin-left: .3em;
}
.dirty-indicator-clean.pull-left {
  margin-right: .3em;
}
.dirty-indicator-clean.pull-right {
  margin-left: .3em;
}
.dirty-indicator-clean:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f00c";
}
.dirty-indicator-clean:before.fa-pull-left {
  margin-right: .3em;
}
.dirty-indicator-clean:before.fa-pull-right {
  margin-left: .3em;
}
.dirty-indicator-clean:before.pull-left {
  margin-right: .3em;
}
.dirty-indicator-clean:before.pull-right {
  margin-left: .3em;
}
#filename {
  font-size: 16pt;
  display: table;
  padding: 0px 5px;
}
#current-mode {
  padding-left: 5px;
  padding-right: 5px;
}
#texteditor-backdrop {
  padding-top: 20px;
  padding-bottom: 20px;
}
@media not print {
  #texteditor-backdrop {
    background-color: #EEE;
  }
}
@media print {
  #texteditor-backdrop #texteditor-container .CodeMirror-gutter,
  #texteditor-backdrop #texteditor-container .CodeMirror-gutters {
    background-color: #fff;
  }
}
@media not print {
  #texteditor-backdrop #texteditor-container .CodeMirror-gutter,
  #texteditor-backdrop #texteditor-container .CodeMirror-gutters {
    background-color: #fff;
  }
}
@media not print {
  #texteditor-backdrop #texteditor-container {
    padding: 0px;
    background-color: #fff;
    -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
    box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  }
}
.CodeMirror-dialog {
  background-color: #fff;
}
/*!
*
* IPython notebook
*
*/
/* CSS font colors for translated ANSI escape sequences */
/* The color values are a mix of
   http://www.xcolors.net/dl/baskerville-ivorylight and
   http://www.xcolors.net/dl/euphrasia */
.ansi-black-fg {
  color: #3E424D;
}
.ansi-black-bg {
  background-color: #3E424D;
}
.ansi-black-intense-fg {
  color: #282C36;
}
.ansi-black-intense-bg {
  background-color: #282C36;
}
.ansi-red-fg {
  color: #E75C58;
}
.ansi-red-bg {
  background-color: #E75C58;
}
.ansi-red-intense-fg {
  color: #B22B31;
}
.ansi-red-intense-bg {
  background-color: #B22B31;
}
.ansi-green-fg {
  color: #00A250;
}
.ansi-green-bg {
  background-color: #00A250;
}
.ansi-green-intense-fg {
  color: #007427;
}
.ansi-green-intense-bg {
  background-color: #007427;
}
.ansi-yellow-fg {
  color: #DDB62B;
}
.ansi-yellow-bg {
  background-color: #DDB62B;
}
.ansi-yellow-intense-fg {
  color: #B27D12;
}
.ansi-yellow-intense-bg {
  background-color: #B27D12;
}
.ansi-blue-fg {
  color: #208FFB;
}
.ansi-blue-bg {
  background-color: #208FFB;
}
.ansi-blue-intense-fg {
  color: #0065CA;
}
.ansi-blue-intense-bg {
  background-color: #0065CA;
}
.ansi-magenta-fg {
  color: #D160C4;
}
.ansi-magenta-bg {
  background-color: #D160C4;
}
.ansi-magenta-intense-fg {
  color: #A03196;
}
.ansi-magenta-intense-bg {
  background-color: #A03196;
}
.ansi-cyan-fg {
  color: #60C6C8;
}
.ansi-cyan-bg {
  background-color: #60C6C8;
}
.ansi-cyan-intense-fg {
  color: #258F8F;
}
.ansi-cyan-intense-bg {
  background-color: #258F8F;
}
.ansi-white-fg {
  color: #C5C1B4;
}
.ansi-white-bg {
  background-color: #C5C1B4;
}
.ansi-white-intense-fg {
  color: #A1A6B2;
}
.ansi-white-intense-bg {
  background-color: #A1A6B2;
}
.ansi-default-inverse-fg {
  color: #FFFFFF;
}
.ansi-default-inverse-bg {
  background-color: #000000;
}
.ansi-bold {
  font-weight: bold;
}
.ansi-underline {
  text-decoration: underline;
}
/* The following styles are deprecated an will be removed in a future version */
.ansibold {
  font-weight: bold;
}
.ansi-inverse {
  outline: 0.5px dotted;
}
/* use dark versions for foreground, to improve visibility */
.ansiblack {
  color: black;
}
.ansired {
  color: darkred;
}
.ansigreen {
  color: darkgreen;
}
.ansiyellow {
  color: #c4a000;
}
.ansiblue {
  color: darkblue;
}
.ansipurple {
  color: darkviolet;
}
.ansicyan {
  color: steelblue;
}
.ansigray {
  color: gray;
}
/* and light for background, for the same reason */
.ansibgblack {
  background-color: black;
}
.ansibgred {
  background-color: red;
}
.ansibggreen {
  background-color: green;
}
.ansibgyellow {
  background-color: yellow;
}
.ansibgblue {
  background-color: blue;
}
.ansibgpurple {
  background-color: magenta;
}
.ansibgcyan {
  background-color: cyan;
}
.ansibggray {
  background-color: gray;
}
div.cell {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
  border-radius: 2px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  border-width: 1px;
  border-style: solid;
  border-color: transparent;
  width: 100%;
  padding: 5px;
  /* This acts as a spacer between cells, that is outside the border */
  margin: 0px;
  outline: none;
  position: relative;
  overflow: visible;
}
div.cell:before {
  position: absolute;
  display: block;
  top: -1px;
  left: -1px;
  width: 5px;
  height: calc(100% +  2px);
  content: '';
  background: transparent;
}
div.cell.jupyter-soft-selected {
  border-left-color: #E3F2FD;
  border-left-width: 1px;
  padding-left: 5px;
  border-right-color: #E3F2FD;
  border-right-width: 1px;
  background: #E3F2FD;
}
@media print {
  div.cell.jupyter-soft-selected {
    border-color: transparent;
  }
}
div.cell.selected,
div.cell.selected.jupyter-soft-selected {
  border-color: #ababab;
}
div.cell.selected:before,
div.cell.selected.jupyter-soft-selected:before {
  position: absolute;
  display: block;
  top: -1px;
  left: -1px;
  width: 5px;
  height: calc(100% +  2px);
  content: '';
  background: #42A5F5;
}
@media print {
  div.cell.selected,
  div.cell.selected.jupyter-soft-selected {
    border-color: transparent;
  }
}
.edit_mode div.cell.selected {
  border-color: #66BB6A;
}
.edit_mode div.cell.selected:before {
  position: absolute;
  display: block;
  top: -1px;
  left: -1px;
  width: 5px;
  height: calc(100% +  2px);
  content: '';
  background: #66BB6A;
}
@media print {
  .edit_mode div.cell.selected {
    border-color: transparent;
  }
}
.prompt {
  /* This needs to be wide enough for 3 digit prompt numbers: In[100]: */
  min-width: 14ex;
  /* This padding is tuned to match the padding on the CodeMirror editor. */
  padding: 0.4em;
  margin: 0px;
  font-family: monospace;
  text-align: right;
  /* This has to match that of the the CodeMirror class line-height below */
  line-height: 1.21429em;
  /* Don't highlight prompt number selection */
  -webkit-touch-callout: none;
  -webkit-user-select: none;
  -khtml-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
  /* Use default cursor */
  cursor: default;
}
@media (max-width: 540px) {
  .prompt {
    text-align: left;
  }
}
div.inner_cell {
  min-width: 0;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
}
/* input_area and input_prompt must match in top border and margin for alignment */
div.input_area {
  border: 1px solid #cfcfcf;
  border-radius: 2px;
  background: #f7f7f7;
  line-height: 1.21429em;
}
/* This is needed so that empty prompt areas can collapse to zero height when there
   is no content in the output_subarea and the prompt. The main purpose of this is
   to make sure that empty JavaScript output_subareas have no height. */
div.prompt:empty {
  padding-top: 0;
  padding-bottom: 0;
}
div.unrecognized_cell {
  padding: 5px 5px 5px 0px;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
div.unrecognized_cell .inner_cell {
  border-radius: 2px;
  padding: 5px;
  font-weight: bold;
  color: red;
  border: 1px solid #cfcfcf;
  background: #eaeaea;
}
div.unrecognized_cell .inner_cell a {
  color: inherit;
  text-decoration: none;
}
div.unrecognized_cell .inner_cell a:hover {
  color: inherit;
  text-decoration: none;
}
@media (max-width: 540px) {
  div.unrecognized_cell > div.prompt {
    display: none;
  }
}
div.code_cell {
  /* avoid page breaking on code cells when printing */
}
@media print {
  div.code_cell {
    page-break-inside: avoid;
  }
}
/* any special styling for code cells that are currently running goes here */
div.input {
  page-break-inside: avoid;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
@media (max-width: 540px) {
  div.input {
    /* Old browsers */
    display: -webkit-box;
    -webkit-box-orient: vertical;
    -webkit-box-align: stretch;
    display: -moz-box;
    -moz-box-orient: vertical;
    -moz-box-align: stretch;
    display: box;
    box-orient: vertical;
    box-align: stretch;
    /* Modern browsers */
    display: flex;
    flex-direction: column;
    align-items: stretch;
  }
}
/* input_area and input_prompt must match in top border and margin for alignment */
div.input_prompt {
  color: #303F9F;
  border-top: 1px solid transparent;
}
div.input_area > div.highlight {
  margin: 0.4em;
  border: none;
  padding: 0px;
  background-color: transparent;
}
div.input_area > div.highlight > pre {
  margin: 0px;
  border: none;
  padding: 0px;
  background-color: transparent;
}
/* The following gets added to the <head> if it is detected that the user has a
 * monospace font with inconsistent normal/bold/italic height.  See
 * notebookmain.js.  Such fonts will have keywords vertically offset with
 * respect to the rest of the text.  The user should select a better font.
 * See: https://github.com/ipython/ipython/issues/1503
 *
 * .CodeMirror span {
 *      vertical-align: bottom;
 * }
 */
.CodeMirror {
  line-height: 1.21429em;
  /* Changed from 1em to our global default */
  font-size: 14px;
  height: auto;
  /* Changed to auto to autogrow */
  background: none;
  /* Changed from white to allow our bg to show through */
}
.CodeMirror-scroll {
  /*  The CodeMirror docs are a bit fuzzy on if overflow-y should be hidden or visible.*/
  /*  We have found that if it is visible, vertical scrollbars appear with font size changes.*/
  overflow-y: hidden;
  overflow-x: auto;
}
.CodeMirror-lines {
  /* In CM2, this used to be 0.4em, but in CM3 it went to 4px. We need the em value because */
  /* we have set a different line-height and want this to scale with that. */
  /* Note that this should set vertical padding only, since CodeMirror assumes
       that horizontal padding will be set on CodeMirror pre */
  padding: 0.4em 0;
}
.CodeMirror-linenumber {
  padding: 0 8px 0 4px;
}
.CodeMirror-gutters {
  border-bottom-left-radius: 2px;
  border-top-left-radius: 2px;
}
.CodeMirror pre {
  /* In CM3 this went to 4px from 0 in CM2. This sets horizontal padding only,
    use .CodeMirror-lines for vertical */
  padding: 0 0.4em;
  border: 0;
  border-radius: 0;
}
.CodeMirror-cursor {
  border-left: 1.4px solid black;
}
@media screen and (min-width: 2138px) and (max-width: 4319px) {
  .CodeMirror-cursor {
    border-left: 2px solid black;
  }
}
@media screen and (min-width: 4320px) {
  .CodeMirror-cursor {
    border-left: 4px solid black;
  }
}
/*

Original style from softwaremaniacs.org (c) Ivan Sagalaev <Maniac@SoftwareManiacs.Org>
Adapted from GitHub theme

*/
.highlight-base {
  color: #000;
}
.highlight-variable {
  color: #000;
}
.highlight-variable-2 {
  color: #1a1a1a;
}
.highlight-variable-3 {
  color: #333333;
}
.highlight-string {
  color: #BA2121;
}
.highlight-comment {
  color: #408080;
  font-style: italic;
}
.highlight-number {
  color: #080;
}
.highlight-atom {
  color: #88F;
}
.highlight-keyword {
  color: #008000;
  font-weight: bold;
}
.highlight-builtin {
  color: #008000;
}
.highlight-error {
  color: #f00;
}
.highlight-operator {
  color: #AA22FF;
  font-weight: bold;
}
.highlight-meta {
  color: #AA22FF;
}
/* previously not defined, copying from default codemirror */
.highlight-def {
  color: #00f;
}
.highlight-string-2 {
  color: #f50;
}
.highlight-qualifier {
  color: #555;
}
.highlight-bracket {
  color: #997;
}
.highlight-tag {
  color: #170;
}
.highlight-attribute {
  color: #00c;
}
.highlight-header {
  color: blue;
}
.highlight-quote {
  color: #090;
}
.highlight-link {
  color: #00c;
}
/* apply the same style to codemirror */
.cm-s-ipython span.cm-keyword {
  color: #008000;
  font-weight: bold;
}
.cm-s-ipython span.cm-atom {
  color: #88F;
}
.cm-s-ipython span.cm-number {
  color: #080;
}
.cm-s-ipython span.cm-def {
  color: #00f;
}
.cm-s-ipython span.cm-variable {
  color: #000;
}
.cm-s-ipython span.cm-operator {
  color: #AA22FF;
  font-weight: bold;
}
.cm-s-ipython span.cm-variable-2 {
  color: #1a1a1a;
}
.cm-s-ipython span.cm-variable-3 {
  color: #333333;
}
.cm-s-ipython span.cm-comment {
  color: #408080;
  font-style: italic;
}
.cm-s-ipython span.cm-string {
  color: #BA2121;
}
.cm-s-ipython span.cm-string-2 {
  color: #f50;
}
.cm-s-ipython span.cm-meta {
  color: #AA22FF;
}
.cm-s-ipython span.cm-qualifier {
  color: #555;
}
.cm-s-ipython span.cm-builtin {
  color: #008000;
}
.cm-s-ipython span.cm-bracket {
  color: #997;
}
.cm-s-ipython span.cm-tag {
  color: #170;
}
.cm-s-ipython span.cm-attribute {
  color: #00c;
}
.cm-s-ipython span.cm-header {
  color: blue;
}
.cm-s-ipython span.cm-quote {
  color: #090;
}
.cm-s-ipython span.cm-link {
  color: #00c;
}
.cm-s-ipython span.cm-error {
  color: #f00;
}
.cm-s-ipython span.cm-tab {
  background: url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAADAAAAAMCAYAAAAkuj5RAAAAAXNSR0IArs4c6QAAAGFJREFUSMft1LsRQFAQheHPowAKoACx3IgEKtaEHujDjORSgWTH/ZOdnZOcM/sgk/kFFWY0qV8foQwS4MKBCS3qR6ixBJvElOobYAtivseIE120FaowJPN75GMu8j/LfMwNjh4HUpwg4LUAAAAASUVORK5CYII=);
  background-position: right;
  background-repeat: no-repeat;
}
div.output_wrapper {
  /* this position must be relative to enable descendents to be absolute within it */
  position: relative;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
  z-index: 1;
}
/* class for the output area when it should be height-limited */
div.output_scroll {
  /* ideally, this would be max-height, but FF barfs all over that */
  height: 24em;
  /* FF needs this *and the wrapper* to specify full width, or it will shrinkwrap */
  width: 100%;
  overflow: auto;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 2px 8px rgba(0, 0, 0, 0.8);
  box-shadow: inset 0 2px 8px rgba(0, 0, 0, 0.8);
  display: block;
}
/* output div while it is collapsed */
div.output_collapsed {
  margin: 0px;
  padding: 0px;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
}
div.out_prompt_overlay {
  height: 100%;
  padding: 0px 0.4em;
  position: absolute;
  border-radius: 2px;
}
div.out_prompt_overlay:hover {
  /* use inner shadow to get border that is computed the same on WebKit/FF */
  -webkit-box-shadow: inset 0 0 1px #000;
  box-shadow: inset 0 0 1px #000;
  background: rgba(240, 240, 240, 0.5);
}
div.output_prompt {
  color: #D84315;
}
/* This class is the outer container of all output sections. */
div.output_area {
  padding: 0px;
  page-break-inside: avoid;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
div.output_area .MathJax_Display {
  text-align: left !important;
}
div.output_area .rendered_html table {
  margin-left: 0;
  margin-right: 0;
}
div.output_area .rendered_html img {
  margin-left: 0;
  margin-right: 0;
}
div.output_area img,
div.output_area svg {
  max-width: 100%;
  height: auto;
}
div.output_area img.unconfined,
div.output_area svg.unconfined {
  max-width: none;
}
div.output_area .mglyph > img {
  max-width: none;
}
/* This is needed to protect the pre formating from global settings such
   as that of bootstrap */
.output {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: vertical;
  -moz-box-align: stretch;
  display: box;
  box-orient: vertical;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: column;
  align-items: stretch;
}
@media (max-width: 540px) {
  div.output_area {
    /* Old browsers */
    display: -webkit-box;
    -webkit-box-orient: vertical;
    -webkit-box-align: stretch;
    display: -moz-box;
    -moz-box-orient: vertical;
    -moz-box-align: stretch;
    display: box;
    box-orient: vertical;
    box-align: stretch;
    /* Modern browsers */
    display: flex;
    flex-direction: column;
    align-items: stretch;
  }
}
div.output_area pre {
  margin: 0;
  padding: 1px 0 1px 0;
  border: 0;
  vertical-align: baseline;
  color: black;
  background-color: transparent;
  border-radius: 0;
}
/* This class is for the output subarea inside the output_area and after
   the prompt div. */
div.output_subarea {
  overflow-x: auto;
  padding: 0.4em;
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
  max-width: calc(100% - 14ex);
}
div.output_scroll div.output_subarea {
  overflow-x: visible;
}
/* The rest of the output_* classes are for special styling of the different
   output types */
/* all text output has this class: */
div.output_text {
  text-align: left;
  color: #000;
  /* This has to match that of the the CodeMirror class line-height below */
  line-height: 1.21429em;
}
/* stdout/stderr are 'text' as well as 'stream', but execute_result/error are *not* streams */
div.output_stderr {
  background: #fdd;
  /* very light red background for stderr */
}
div.output_latex {
  text-align: left;
}
/* Empty output_javascript divs should have no height */
div.output_javascript:empty {
  padding: 0;
}
.js-error {
  color: darkred;
}
/* raw_input styles */
div.raw_input_container {
  line-height: 1.21429em;
  padding-top: 5px;
}
pre.raw_input_prompt {
  /* nothing needed here. */
}
input.raw_input {
  font-family: monospace;
  font-size: inherit;
  color: inherit;
  width: auto;
  /* make sure input baseline aligns with prompt */
  vertical-align: baseline;
  /* padding + margin = 0.5em between prompt and cursor */
  padding: 0em 0.25em;
  margin: 0em 0.25em;
}
input.raw_input:focus {
  box-shadow: none;
}
p.p-space {
  margin-bottom: 10px;
}
div.output_unrecognized {
  padding: 5px;
  font-weight: bold;
  color: red;
}
div.output_unrecognized a {
  color: inherit;
  text-decoration: none;
}
div.output_unrecognized a:hover {
  color: inherit;
  text-decoration: none;
}
.rendered_html {
  color: #000;
  /* any extras will just be numbers: */
}
.rendered_html em {
  font-style: italic;
}
.rendered_html strong {
  font-weight: bold;
}
.rendered_html u {
  text-decoration: underline;
}
.rendered_html :link {
  text-decoration: underline;
}
.rendered_html :visited {
  text-decoration: underline;
}
.rendered_html h1 {
  font-size: 185.7%;
  margin: 1.08em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
}
.rendered_html h2 {
  font-size: 157.1%;
  margin: 1.27em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
}
.rendered_html h3 {
  font-size: 128.6%;
  margin: 1.55em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
}
.rendered_html h4 {
  font-size: 100%;
  margin: 2em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
}
.rendered_html h5 {
  font-size: 100%;
  margin: 2em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
  font-style: italic;
}
.rendered_html h6 {
  font-size: 100%;
  margin: 2em 0 0 0;
  font-weight: bold;
  line-height: 1.0;
  font-style: italic;
}
.rendered_html h1:first-child {
  margin-top: 0.538em;
}
.rendered_html h2:first-child {
  margin-top: 0.636em;
}
.rendered_html h3:first-child {
  margin-top: 0.777em;
}
.rendered_html h4:first-child {
  margin-top: 1em;
}
.rendered_html h5:first-child {
  margin-top: 1em;
}
.rendered_html h6:first-child {
  margin-top: 1em;
}
.rendered_html ul:not(.list-inline),
.rendered_html ol:not(.list-inline) {
  padding-left: 2em;
}
.rendered_html ul {
  list-style: disc;
}
.rendered_html ul ul {
  list-style: square;
  margin-top: 0;
}
.rendered_html ul ul ul {
  list-style: circle;
}
.rendered_html ol {
  list-style: decimal;
}
.rendered_html ol ol {
  list-style: upper-alpha;
  margin-top: 0;
}
.rendered_html ol ol ol {
  list-style: lower-alpha;
}
.rendered_html ol ol ol ol {
  list-style: lower-roman;
}
.rendered_html ol ol ol ol ol {
  list-style: decimal;
}
.rendered_html * + ul {
  margin-top: 1em;
}
.rendered_html * + ol {
  margin-top: 1em;
}
.rendered_html hr {
  color: black;
  background-color: black;
}
.rendered_html pre {
  margin: 1em 2em;
  padding: 0px;
  background-color: #fff;
}
.rendered_html code {
  background-color: #eff0f1;
}
.rendered_html p code {
  padding: 1px 5px;
}
.rendered_html pre code {
  background-color: #fff;
}
.rendered_html pre,
.rendered_html code {
  border: 0;
  color: #000;
  font-size: 100%;
}
.rendered_html blockquote {
  margin: 1em 2em;
}
.rendered_html table {
  margin-left: auto;
  margin-right: auto;
  border: none;
  border-collapse: collapse;
  border-spacing: 0;
  color: black;
  font-size: 12px;
  table-layout: fixed;
}
.rendered_html thead {
  border-bottom: 1px solid black;
  vertical-align: bottom;
}
.rendered_html tr,
.rendered_html th,
.rendered_html td {
  text-align: right;
  vertical-align: middle;
  padding: 0.5em 0.5em;
  line-height: normal;
  white-space: normal;
  max-width: none;
  border: none;
}
.rendered_html th {
  font-weight: bold;
}
.rendered_html tbody tr:nth-child(odd) {
  background: #f5f5f5;
}
.rendered_html tbody tr:hover {
  background: rgba(66, 165, 245, 0.2);
}
.rendered_html * + table {
  margin-top: 1em;
}
.rendered_html p {
  text-align: left;
}
.rendered_html * + p {
  margin-top: 1em;
}
.rendered_html img {
  display: block;
  margin-left: auto;
  margin-right: auto;
}
.rendered_html * + img {
  margin-top: 1em;
}
.rendered_html img,
.rendered_html svg {
  max-width: 100%;
  height: auto;
}
.rendered_html img.unconfined,
.rendered_html svg.unconfined {
  max-width: none;
}
.rendered_html .alert {
  margin-bottom: initial;
}
.rendered_html * + .alert {
  margin-top: 1em;
}
[dir="rtl"] .rendered_html p {
  text-align: right;
}
div.text_cell {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
}
@media (max-width: 540px) {
  div.text_cell > div.prompt {
    display: none;
  }
}
div.text_cell_render {
  /*font-family: "Helvetica Neue", Arial, Helvetica, Geneva, sans-serif;*/
  outline: none;
  resize: none;
  width: inherit;
  border-style: none;
  padding: 0.5em 0.5em 0.5em 0.4em;
  color: #000;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
a.anchor-link:link {
  text-decoration: none;
  padding: 0px 20px;
  visibility: hidden;
}
h1:hover .anchor-link,
h2:hover .anchor-link,
h3:hover .anchor-link,
h4:hover .anchor-link,
h5:hover .anchor-link,
h6:hover .anchor-link {
  visibility: visible;
}
.text_cell.rendered .input_area {
  display: none;
}
.text_cell.rendered .rendered_html {
  overflow-x: auto;
  overflow-y: hidden;
}
.text_cell.rendered .rendered_html tr,
.text_cell.rendered .rendered_html th,
.text_cell.rendered .rendered_html td {
  max-width: none;
}
.text_cell.unrendered .text_cell_render {
  display: none;
}
.text_cell .dropzone .input_area {
  border: 2px dashed #bababa;
  margin: -1px;
}
.cm-header-1,
.cm-header-2,
.cm-header-3,
.cm-header-4,
.cm-header-5,
.cm-header-6 {
  font-weight: bold;
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
}
.cm-header-1 {
  font-size: 185.7%;
}
.cm-header-2 {
  font-size: 157.1%;
}
.cm-header-3 {
  font-size: 128.6%;
}
.cm-header-4 {
  font-size: 110%;
}
.cm-header-5 {
  font-size: 100%;
  font-style: italic;
}
.cm-header-6 {
  font-size: 100%;
  font-style: italic;
}
/*!
*
* IPython notebook webapp
*
*/
@media (max-width: 767px) {
  .notebook_app {
    padding-left: 0px;
    padding-right: 0px;
  }
}
#ipython-main-app {
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  height: 100%;
}
div#notebook_panel {
  margin: 0px;
  padding: 0px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  height: 100%;
}
div#notebook {
  font-size: 14px;
  line-height: 20px;
  overflow-y: hidden;
  overflow-x: auto;
  width: 100%;
  /* This spaces the page away from the edge of the notebook area */
  padding-top: 20px;
  margin: 0px;
  outline: none;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  min-height: 100%;
}
@media not print {
  #notebook-container {
    padding: 15px;
    background-color: #fff;
    min-height: 0;
    -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
    box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  }
}
@media print {
  #notebook-container {
    width: 100%;
  }
}
div.ui-widget-content {
  border: 1px solid #ababab;
  outline: none;
}
pre.dialog {
  background-color: #f7f7f7;
  border: 1px solid #ddd;
  border-radius: 2px;
  padding: 0.4em;
  padding-left: 2em;
}
p.dialog {
  padding: 0.2em;
}
/* Word-wrap output correctly.  This is the CSS3 spelling, though Firefox seems
   to not honor it correctly.  Webkit browsers (Chrome, rekonq, Safari) do.
 */
pre,
code,
kbd,
samp {
  white-space: pre-wrap;
}
#fonttest {
  font-family: monospace;
}
p {
  margin-bottom: 0;
}
.end_space {
  min-height: 100px;
  transition: height .2s ease;
}
.notebook_app > #header {
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
}
@media not print {
  .notebook_app {
    background-color: #EEE;
  }
}
kbd {
  border-style: solid;
  border-width: 1px;
  box-shadow: none;
  margin: 2px;
  padding-left: 2px;
  padding-right: 2px;
  padding-top: 1px;
  padding-bottom: 1px;
}
.jupyter-keybindings {
  padding: 1px;
  line-height: 24px;
  border-bottom: 1px solid gray;
}
.jupyter-keybindings input {
  margin: 0;
  padding: 0;
  border: none;
}
.jupyter-keybindings i {
  padding: 6px;
}
.well code {
  background-color: #ffffff;
  border-color: #ababab;
  border-width: 1px;
  border-style: solid;
  padding: 2px;
  padding-top: 1px;
  padding-bottom: 1px;
}
/* CSS for the cell toolbar */
.celltoolbar {
  border: thin solid #CFCFCF;
  border-bottom: none;
  background: #EEE;
  border-radius: 2px 2px 0px 0px;
  width: 100%;
  height: 29px;
  padding-right: 4px;
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
  /* Old browsers */
  -webkit-box-pack: end;
  -moz-box-pack: end;
  box-pack: end;
  /* Modern browsers */
  justify-content: flex-end;
  display: -webkit-flex;
}
@media print {
  .celltoolbar {
    display: none;
  }
}
.ctb_hideshow {
  display: none;
  vertical-align: bottom;
}
/* ctb_show is added to the ctb_hideshow div to show the cell toolbar.
   Cell toolbars are only shown when the ctb_global_show class is also set.
*/
.ctb_global_show .ctb_show.ctb_hideshow {
  display: block;
}
.ctb_global_show .ctb_show + .input_area,
.ctb_global_show .ctb_show + div.text_cell_input,
.ctb_global_show .ctb_show ~ div.text_cell_render {
  border-top-right-radius: 0px;
  border-top-left-radius: 0px;
}
.ctb_global_show .ctb_show ~ div.text_cell_render {
  border: 1px solid #cfcfcf;
}
.celltoolbar {
  font-size: 87%;
  padding-top: 3px;
}
.celltoolbar select {
  display: block;
  width: 100%;
  height: 32px;
  padding: 6px 12px;
  font-size: 13px;
  line-height: 1.42857143;
  color: #555555;
  background-color: #fff;
  background-image: none;
  border: 1px solid #ccc;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  -webkit-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  -o-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  height: 30px;
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
  width: inherit;
  font-size: inherit;
  height: 22px;
  padding: 0px;
  display: inline-block;
}
.celltoolbar select:focus {
  border-color: #66afe9;
  outline: 0;
  -webkit-box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
  box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
}
.celltoolbar select::-moz-placeholder {
  color: #999;
  opacity: 1;
}
.celltoolbar select:-ms-input-placeholder {
  color: #999;
}
.celltoolbar select::-webkit-input-placeholder {
  color: #999;
}
.celltoolbar select::-ms-expand {
  border: 0;
  background-color: transparent;
}
.celltoolbar select[disabled],
.celltoolbar select[readonly],
fieldset[disabled] .celltoolbar select {
  background-color: #eeeeee;
  opacity: 1;
}
.celltoolbar select[disabled],
fieldset[disabled] .celltoolbar select {
  cursor: not-allowed;
}
textarea.celltoolbar select {
  height: auto;
}
select.celltoolbar select {
  height: 30px;
  line-height: 30px;
}
textarea.celltoolbar select,
select[multiple].celltoolbar select {
  height: auto;
}
.celltoolbar label {
  margin-left: 5px;
  margin-right: 5px;
}
.tags_button_container {
  width: 100%;
  display: flex;
}
.tag-container {
  display: flex;
  flex-direction: row;
  flex-grow: 1;
  overflow: hidden;
  position: relative;
}
.tag-container > * {
  margin: 0 4px;
}
.remove-tag-btn {
  margin-left: 4px;
}
.tags-input {
  display: flex;
}
.cell-tag:last-child:after {
  content: "";
  position: absolute;
  right: 0;
  width: 40px;
  height: 100%;
  /* Fade to background color of cell toolbar */
  background: linear-gradient(to right, rgba(0, 0, 0, 0), #EEE);
}
.tags-input > * {
  margin-left: 4px;
}
.cell-tag,
.tags-input input,
.tags-input button {
  display: block;
  width: 100%;
  height: 32px;
  padding: 6px 12px;
  font-size: 13px;
  line-height: 1.42857143;
  color: #555555;
  background-color: #fff;
  background-image: none;
  border: 1px solid #ccc;
  border-radius: 2px;
  -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.075);
  -webkit-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  -o-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
  height: 30px;
  padding: 5px 10px;
  font-size: 12px;
  line-height: 1.5;
  border-radius: 1px;
  box-shadow: none;
  width: inherit;
  font-size: inherit;
  height: 22px;
  line-height: 22px;
  padding: 0px 4px;
  display: inline-block;
}
.cell-tag:focus,
.tags-input input:focus,
.tags-input button:focus {
  border-color: #66afe9;
  outline: 0;
  -webkit-box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
  box-shadow: inset 0 1px 1px rgba(0,0,0,.075), 0 0 8px rgba(102, 175, 233, 0.6);
}
.cell-tag::-moz-placeholder,
.tags-input input::-moz-placeholder,
.tags-input button::-moz-placeholder {
  color: #999;
  opacity: 1;
}
.cell-tag:-ms-input-placeholder,
.tags-input input:-ms-input-placeholder,
.tags-input button:-ms-input-placeholder {
  color: #999;
}
.cell-tag::-webkit-input-placeholder,
.tags-input input::-webkit-input-placeholder,
.tags-input button::-webkit-input-placeholder {
  color: #999;
}
.cell-tag::-ms-expand,
.tags-input input::-ms-expand,
.tags-input button::-ms-expand {
  border: 0;
  background-color: transparent;
}
.cell-tag[disabled],
.tags-input input[disabled],
.tags-input button[disabled],
.cell-tag[readonly],
.tags-input input[readonly],
.tags-input button[readonly],
fieldset[disabled] .cell-tag,
fieldset[disabled] .tags-input input,
fieldset[disabled] .tags-input button {
  background-color: #eeeeee;
  opacity: 1;
}
.cell-tag[disabled],
.tags-input input[disabled],
.tags-input button[disabled],
fieldset[disabled] .cell-tag,
fieldset[disabled] .tags-input input,
fieldset[disabled] .tags-input button {
  cursor: not-allowed;
}
textarea.cell-tag,
textarea.tags-input input,
textarea.tags-input button {
  height: auto;
}
select.cell-tag,
select.tags-input input,
select.tags-input button {
  height: 30px;
  line-height: 30px;
}
textarea.cell-tag,
textarea.tags-input input,
textarea.tags-input button,
select[multiple].cell-tag,
select[multiple].tags-input input,
select[multiple].tags-input button {
  height: auto;
}
.cell-tag,
.tags-input button {
  padding: 0px 4px;
}
.cell-tag {
  background-color: #fff;
  white-space: nowrap;
}
.tags-input input[type=text]:focus {
  outline: none;
  box-shadow: none;
  border-color: #ccc;
}
.completions {
  position: absolute;
  z-index: 110;
  overflow: hidden;
  border: 1px solid #ababab;
  border-radius: 2px;
  -webkit-box-shadow: 0px 6px 10px -1px #adadad;
  box-shadow: 0px 6px 10px -1px #adadad;
  line-height: 1;
}
.completions select {
  background: white;
  outline: none;
  border: none;
  padding: 0px;
  margin: 0px;
  overflow: auto;
  font-family: monospace;
  font-size: 110%;
  color: #000;
  width: auto;
}
.completions select option.context {
  color: #286090;
}
#kernel_logo_widget .current_kernel_logo {
  display: none;
  margin-top: -1px;
  margin-bottom: -1px;
  width: 32px;
  height: 32px;
}
[dir="rtl"] #kernel_logo_widget {
  float: left !important;
  float: left;
}
.modal .modal-body .move-path {
  display: flex;
  flex-direction: row;
  justify-content: space;
  align-items: center;
}
.modal .modal-body .move-path .server-root {
  padding-right: 20px;
}
.modal .modal-body .move-path .path-input {
  flex: 1;
}
#menubar {
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
  margin-top: 1px;
}
#menubar .navbar {
  border-top: 1px;
  border-radius: 0px 0px 2px 2px;
  margin-bottom: 0px;
}
#menubar .navbar-toggle {
  float: left;
  padding-top: 7px;
  padding-bottom: 7px;
  border: none;
}
#menubar .navbar-collapse {
  clear: left;
}
[dir="rtl"] #menubar .navbar-toggle {
  float: right;
}
[dir="rtl"] #menubar .navbar-collapse {
  clear: right;
}
[dir="rtl"] #menubar .navbar-nav {
  float: right;
}
[dir="rtl"] #menubar .nav {
  padding-right: 0px;
}
[dir="rtl"] #menubar .navbar-nav > li {
  float: right;
}
[dir="rtl"] #menubar .navbar-right {
  float: left !important;
}
[dir="rtl"] ul.dropdown-menu {
  text-align: right;
  left: auto;
}
[dir="rtl"] ul#new-menu.dropdown-menu {
  right: auto;
  left: 0;
}
.nav-wrapper {
  border-bottom: 1px solid #e7e7e7;
}
i.menu-icon {
  padding-top: 4px;
}
[dir="rtl"] i.menu-icon.pull-right {
  float: left !important;
  float: left;
}
ul#help_menu li a {
  overflow: hidden;
  padding-right: 2.2em;
}
ul#help_menu li a i {
  margin-right: -1.2em;
}
[dir="rtl"] ul#help_menu li a {
  padding-left: 2.2em;
}
[dir="rtl"] ul#help_menu li a i {
  margin-right: 0;
  margin-left: -1.2em;
}
[dir="rtl"] ul#help_menu li a i.pull-right {
  float: left !important;
  float: left;
}
.dropdown-submenu {
  position: relative;
}
.dropdown-submenu > .dropdown-menu {
  top: 0;
  left: 100%;
  margin-top: -6px;
  margin-left: -1px;
}
[dir="rtl"] .dropdown-submenu > .dropdown-menu {
  right: 100%;
  margin-right: -1px;
}
.dropdown-submenu:hover > .dropdown-menu {
  display: block;
}
.dropdown-submenu > a:after {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  display: block;
  content: "\f0da";
  float: right;
  color: #333333;
  margin-top: 2px;
  margin-right: -10px;
}
.dropdown-submenu > a:after.fa-pull-left {
  margin-right: .3em;
}
.dropdown-submenu > a:after.fa-pull-right {
  margin-left: .3em;
}
.dropdown-submenu > a:after.pull-left {
  margin-right: .3em;
}
.dropdown-submenu > a:after.pull-right {
  margin-left: .3em;
}
[dir="rtl"] .dropdown-submenu > a:after {
  float: left;
  content: "\f0d9";
  margin-right: 0;
  margin-left: -10px;
}
.dropdown-submenu:hover > a:after {
  color: #262626;
}
.dropdown-submenu.pull-left {
  float: none;
}
.dropdown-submenu.pull-left > .dropdown-menu {
  left: -100%;
  margin-left: 10px;
}
#notification_area {
  float: right !important;
  float: right;
  z-index: 10;
}
[dir="rtl"] #notification_area {
  float: left !important;
  float: left;
}
.indicator_area {
  float: right !important;
  float: right;
  color: #777;
  margin-left: 5px;
  margin-right: 5px;
  width: 11px;
  z-index: 10;
  text-align: center;
  width: auto;
}
[dir="rtl"] .indicator_area {
  float: left !important;
  float: left;
}
#kernel_indicator {
  float: right !important;
  float: right;
  color: #777;
  margin-left: 5px;
  margin-right: 5px;
  width: 11px;
  z-index: 10;
  text-align: center;
  width: auto;
  border-left: 1px solid;
}
#kernel_indicator .kernel_indicator_name {
  padding-left: 5px;
  padding-right: 5px;
}
[dir="rtl"] #kernel_indicator {
  float: left !important;
  float: left;
  border-left: 0;
  border-right: 1px solid;
}
#modal_indicator {
  float: right !important;
  float: right;
  color: #777;
  margin-left: 5px;
  margin-right: 5px;
  width: 11px;
  z-index: 10;
  text-align: center;
  width: auto;
}
[dir="rtl"] #modal_indicator {
  float: left !important;
  float: left;
}
#readonly-indicator {
  float: right !important;
  float: right;
  color: #777;
  margin-left: 5px;
  margin-right: 5px;
  width: 11px;
  z-index: 10;
  text-align: center;
  width: auto;
  margin-top: 2px;
  margin-bottom: 0px;
  margin-left: 0px;
  margin-right: 0px;
  display: none;
}
.modal_indicator:before {
  width: 1.28571429em;
  text-align: center;
}
.edit_mode .modal_indicator:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f040";
}
.edit_mode .modal_indicator:before.fa-pull-left {
  margin-right: .3em;
}
.edit_mode .modal_indicator:before.fa-pull-right {
  margin-left: .3em;
}
.edit_mode .modal_indicator:before.pull-left {
  margin-right: .3em;
}
.edit_mode .modal_indicator:before.pull-right {
  margin-left: .3em;
}
.command_mode .modal_indicator:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: ' ';
}
.command_mode .modal_indicator:before.fa-pull-left {
  margin-right: .3em;
}
.command_mode .modal_indicator:before.fa-pull-right {
  margin-left: .3em;
}
.command_mode .modal_indicator:before.pull-left {
  margin-right: .3em;
}
.command_mode .modal_indicator:before.pull-right {
  margin-left: .3em;
}
.kernel_idle_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f10c";
}
.kernel_idle_icon:before.fa-pull-left {
  margin-right: .3em;
}
.kernel_idle_icon:before.fa-pull-right {
  margin-left: .3em;
}
.kernel_idle_icon:before.pull-left {
  margin-right: .3em;
}
.kernel_idle_icon:before.pull-right {
  margin-left: .3em;
}
.kernel_busy_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f111";
}
.kernel_busy_icon:before.fa-pull-left {
  margin-right: .3em;
}
.kernel_busy_icon:before.fa-pull-right {
  margin-left: .3em;
}
.kernel_busy_icon:before.pull-left {
  margin-right: .3em;
}
.kernel_busy_icon:before.pull-right {
  margin-left: .3em;
}
.kernel_dead_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f1e2";
}
.kernel_dead_icon:before.fa-pull-left {
  margin-right: .3em;
}
.kernel_dead_icon:before.fa-pull-right {
  margin-left: .3em;
}
.kernel_dead_icon:before.pull-left {
  margin-right: .3em;
}
.kernel_dead_icon:before.pull-right {
  margin-left: .3em;
}
.kernel_disconnected_icon:before {
  display: inline-block;
  font: normal normal normal 14px/1 FontAwesome;
  font-size: inherit;
  text-rendering: auto;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  content: "\f127";
}
.kernel_disconnected_icon:before.fa-pull-left {
  margin-right: .3em;
}
.kernel_disconnected_icon:before.fa-pull-right {
  margin-left: .3em;
}
.kernel_disconnected_icon:before.pull-left {
  margin-right: .3em;
}
.kernel_disconnected_icon:before.pull-right {
  margin-left: .3em;
}
.notification_widget {
  color: #777;
  z-index: 10;
  background: rgba(240, 240, 240, 0.5);
  margin-right: 4px;
  color: #333;
  background-color: #fff;
  border-color: #ccc;
}
.notification_widget:focus,
.notification_widget.focus {
  color: #333;
  background-color: #e6e6e6;
  border-color: #8c8c8c;
}
.notification_widget:hover {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
.notification_widget:active,
.notification_widget.active,
.open > .dropdown-toggle.notification_widget {
  color: #333;
  background-color: #e6e6e6;
  border-color: #adadad;
}
.notification_widget:active:hover,
.notification_widget.active:hover,
.open > .dropdown-toggle.notification_widget:hover,
.notification_widget:active:focus,
.notification_widget.active:focus,
.open > .dropdown-toggle.notification_widget:focus,
.notification_widget:active.focus,
.notification_widget.active.focus,
.open > .dropdown-toggle.notification_widget.focus {
  color: #333;
  background-color: #d4d4d4;
  border-color: #8c8c8c;
}
.notification_widget:active,
.notification_widget.active,
.open > .dropdown-toggle.notification_widget {
  background-image: none;
}
.notification_widget.disabled:hover,
.notification_widget[disabled]:hover,
fieldset[disabled] .notification_widget:hover,
.notification_widget.disabled:focus,
.notification_widget[disabled]:focus,
fieldset[disabled] .notification_widget:focus,
.notification_widget.disabled.focus,
.notification_widget[disabled].focus,
fieldset[disabled] .notification_widget.focus {
  background-color: #fff;
  border-color: #ccc;
}
.notification_widget .badge {
  color: #fff;
  background-color: #333;
}
.notification_widget.warning {
  color: #fff;
  background-color: #f0ad4e;
  border-color: #eea236;
}
.notification_widget.warning:focus,
.notification_widget.warning.focus {
  color: #fff;
  background-color: #ec971f;
  border-color: #985f0d;
}
.notification_widget.warning:hover {
  color: #fff;
  background-color: #ec971f;
  border-color: #d58512;
}
.notification_widget.warning:active,
.notification_widget.warning.active,
.open > .dropdown-toggle.notification_widget.warning {
  color: #fff;
  background-color: #ec971f;
  border-color: #d58512;
}
.notification_widget.warning:active:hover,
.notification_widget.warning.active:hover,
.open > .dropdown-toggle.notification_widget.warning:hover,
.notification_widget.warning:active:focus,
.notification_widget.warning.active:focus,
.open > .dropdown-toggle.notification_widget.warning:focus,
.notification_widget.warning:active.focus,
.notification_widget.warning.active.focus,
.open > .dropdown-toggle.notification_widget.warning.focus {
  color: #fff;
  background-color: #d58512;
  border-color: #985f0d;
}
.notification_widget.warning:active,
.notification_widget.warning.active,
.open > .dropdown-toggle.notification_widget.warning {
  background-image: none;
}
.notification_widget.warning.disabled:hover,
.notification_widget.warning[disabled]:hover,
fieldset[disabled] .notification_widget.warning:hover,
.notification_widget.warning.disabled:focus,
.notification_widget.warning[disabled]:focus,
fieldset[disabled] .notification_widget.warning:focus,
.notification_widget.warning.disabled.focus,
.notification_widget.warning[disabled].focus,
fieldset[disabled] .notification_widget.warning.focus {
  background-color: #f0ad4e;
  border-color: #eea236;
}
.notification_widget.warning .badge {
  color: #f0ad4e;
  background-color: #fff;
}
.notification_widget.success {
  color: #fff;
  background-color: #5cb85c;
  border-color: #4cae4c;
}
.notification_widget.success:focus,
.notification_widget.success.focus {
  color: #fff;
  background-color: #449d44;
  border-color: #255625;
}
.notification_widget.success:hover {
  color: #fff;
  background-color: #449d44;
  border-color: #398439;
}
.notification_widget.success:active,
.notification_widget.success.active,
.open > .dropdown-toggle.notification_widget.success {
  color: #fff;
  background-color: #449d44;
  border-color: #398439;
}
.notification_widget.success:active:hover,
.notification_widget.success.active:hover,
.open > .dropdown-toggle.notification_widget.success:hover,
.notification_widget.success:active:focus,
.notification_widget.success.active:focus,
.open > .dropdown-toggle.notification_widget.success:focus,
.notification_widget.success:active.focus,
.notification_widget.success.active.focus,
.open > .dropdown-toggle.notification_widget.success.focus {
  color: #fff;
  background-color: #398439;
  border-color: #255625;
}
.notification_widget.success:active,
.notification_widget.success.active,
.open > .dropdown-toggle.notification_widget.success {
  background-image: none;
}
.notification_widget.success.disabled:hover,
.notification_widget.success[disabled]:hover,
fieldset[disabled] .notification_widget.success:hover,
.notification_widget.success.disabled:focus,
.notification_widget.success[disabled]:focus,
fieldset[disabled] .notification_widget.success:focus,
.notification_widget.success.disabled.focus,
.notification_widget.success[disabled].focus,
fieldset[disabled] .notification_widget.success.focus {
  background-color: #5cb85c;
  border-color: #4cae4c;
}
.notification_widget.success .badge {
  color: #5cb85c;
  background-color: #fff;
}
.notification_widget.info {
  color: #fff;
  background-color: #5bc0de;
  border-color: #46b8da;
}
.notification_widget.info:focus,
.notification_widget.info.focus {
  color: #fff;
  background-color: #31b0d5;
  border-color: #1b6d85;
}
.notification_widget.info:hover {
  color: #fff;
  background-color: #31b0d5;
  border-color: #269abc;
}
.notification_widget.info:active,
.notification_widget.info.active,
.open > .dropdown-toggle.notification_widget.info {
  color: #fff;
  background-color: #31b0d5;
  border-color: #269abc;
}
.notification_widget.info:active:hover,
.notification_widget.info.active:hover,
.open > .dropdown-toggle.notification_widget.info:hover,
.notification_widget.info:active:focus,
.notification_widget.info.active:focus,
.open > .dropdown-toggle.notification_widget.info:focus,
.notification_widget.info:active.focus,
.notification_widget.info.active.focus,
.open > .dropdown-toggle.notification_widget.info.focus {
  color: #fff;
  background-color: #269abc;
  border-color: #1b6d85;
}
.notification_widget.info:active,
.notification_widget.info.active,
.open > .dropdown-toggle.notification_widget.info {
  background-image: none;
}
.notification_widget.info.disabled:hover,
.notification_widget.info[disabled]:hover,
fieldset[disabled] .notification_widget.info:hover,
.notification_widget.info.disabled:focus,
.notification_widget.info[disabled]:focus,
fieldset[disabled] .notification_widget.info:focus,
.notification_widget.info.disabled.focus,
.notification_widget.info[disabled].focus,
fieldset[disabled] .notification_widget.info.focus {
  background-color: #5bc0de;
  border-color: #46b8da;
}
.notification_widget.info .badge {
  color: #5bc0de;
  background-color: #fff;
}
.notification_widget.danger {
  color: #fff;
  background-color: #d9534f;
  border-color: #d43f3a;
}
.notification_widget.danger:focus,
.notification_widget.danger.focus {
  color: #fff;
  background-color: #c9302c;
  border-color: #761c19;
}
.notification_widget.danger:hover {
  color: #fff;
  background-color: #c9302c;
  border-color: #ac2925;
}
.notification_widget.danger:active,
.notification_widget.danger.active,
.open > .dropdown-toggle.notification_widget.danger {
  color: #fff;
  background-color: #c9302c;
  border-color: #ac2925;
}
.notification_widget.danger:active:hover,
.notification_widget.danger.active:hover,
.open > .dropdown-toggle.notification_widget.danger:hover,
.notification_widget.danger:active:focus,
.notification_widget.danger.active:focus,
.open > .dropdown-toggle.notification_widget.danger:focus,
.notification_widget.danger:active.focus,
.notification_widget.danger.active.focus,
.open > .dropdown-toggle.notification_widget.danger.focus {
  color: #fff;
  background-color: #ac2925;
  border-color: #761c19;
}
.notification_widget.danger:active,
.notification_widget.danger.active,
.open > .dropdown-toggle.notification_widget.danger {
  background-image: none;
}
.notification_widget.danger.disabled:hover,
.notification_widget.danger[disabled]:hover,
fieldset[disabled] .notification_widget.danger:hover,
.notification_widget.danger.disabled:focus,
.notification_widget.danger[disabled]:focus,
fieldset[disabled] .notification_widget.danger:focus,
.notification_widget.danger.disabled.focus,
.notification_widget.danger[disabled].focus,
fieldset[disabled] .notification_widget.danger.focus {
  background-color: #d9534f;
  border-color: #d43f3a;
}
.notification_widget.danger .badge {
  color: #d9534f;
  background-color: #fff;
}
div#pager {
  background-color: #fff;
  font-size: 14px;
  line-height: 20px;
  overflow: hidden;
  display: none;
  position: fixed;
  bottom: 0px;
  width: 100%;
  max-height: 50%;
  padding-top: 8px;
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  /* Display over codemirror */
  z-index: 100;
  /* Hack which prevents jquery ui resizable from changing top. */
  top: auto !important;
}
div#pager pre {
  line-height: 1.21429em;
  color: #000;
  background-color: #f7f7f7;
  padding: 0.4em;
}
div#pager #pager-button-area {
  position: absolute;
  top: 8px;
  right: 20px;
}
div#pager #pager-contents {
  position: relative;
  overflow: auto;
  width: 100%;
  height: 100%;
}
div#pager #pager-contents #pager-container {
  position: relative;
  padding: 15px 0px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
div#pager .ui-resizable-handle {
  top: 0px;
  height: 8px;
  background: #f7f7f7;
  border-top: 1px solid #cfcfcf;
  border-bottom: 1px solid #cfcfcf;
  /* This injects handle bars (a short, wide = symbol) for
        the resize handle. */
}
div#pager .ui-resizable-handle::after {
  content: '';
  top: 2px;
  left: 50%;
  height: 3px;
  width: 30px;
  margin-left: -15px;
  position: absolute;
  border-top: 1px solid #cfcfcf;
}
.quickhelp {
  /* Old browsers */
  display: -webkit-box;
  -webkit-box-orient: horizontal;
  -webkit-box-align: stretch;
  display: -moz-box;
  -moz-box-orient: horizontal;
  -moz-box-align: stretch;
  display: box;
  box-orient: horizontal;
  box-align: stretch;
  /* Modern browsers */
  display: flex;
  flex-direction: row;
  align-items: stretch;
  line-height: 1.8em;
}
.shortcut_key {
  display: inline-block;
  width: 21ex;
  text-align: right;
  font-family: monospace;
}
.shortcut_descr {
  display: inline-block;
  /* Old browsers */
  -webkit-box-flex: 1;
  -moz-box-flex: 1;
  box-flex: 1;
  /* Modern browsers */
  flex: 1;
}
span.save_widget {
  height: 30px;
  margin-top: 4px;
  display: flex;
  justify-content: flex-start;
  align-items: baseline;
  width: 50%;
  flex: 1;
}
span.save_widget span.filename {
  height: 100%;
  line-height: 1em;
  margin-left: 16px;
  border: none;
  font-size: 146.5%;
  text-overflow: ellipsis;
  overflow: hidden;
  white-space: nowrap;
  border-radius: 2px;
}
span.save_widget span.filename:hover {
  background-color: #e6e6e6;
}
[dir="rtl"] span.save_widget.pull-left {
  float: right !important;
  float: right;
}
[dir="rtl"] span.save_widget span.filename {
  margin-left: 0;
  margin-right: 16px;
}
span.checkpoint_status,
span.autosave_status {
  font-size: small;
  white-space: nowrap;
  padding: 0 5px;
}
@media (max-width: 767px) {
  span.save_widget {
    font-size: small;
    padding: 0 0 0 5px;
  }
  span.checkpoint_status,
  span.autosave_status {
    display: none;
  }
}
@media (min-width: 768px) and (max-width: 991px) {
  span.checkpoint_status {
    display: none;
  }
  span.autosave_status {
    font-size: x-small;
  }
}
.toolbar {
  padding: 0px;
  margin-left: -5px;
  margin-top: 2px;
  margin-bottom: 5px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
.toolbar select,
.toolbar label {
  width: auto;
  vertical-align: middle;
  margin-right: 2px;
  margin-bottom: 0px;
  display: inline;
  font-size: 92%;
  margin-left: 0.3em;
  margin-right: 0.3em;
  padding: 0px;
  padding-top: 3px;
}
.toolbar .btn {
  padding: 2px 8px;
}
.toolbar .btn-group {
  margin-top: 0px;
  margin-left: 5px;
}
.toolbar-btn-label {
  margin-left: 6px;
}
#maintoolbar {
  margin-bottom: -3px;
  margin-top: -8px;
  border: 0px;
  min-height: 27px;
  margin-left: 0px;
  padding-top: 11px;
  padding-bottom: 3px;
}
#maintoolbar .navbar-text {
  float: none;
  vertical-align: middle;
  text-align: right;
  margin-left: 5px;
  margin-right: 0px;
  margin-top: 0px;
}
.select-xs {
  height: 24px;
}
[dir="rtl"] .btn-group > .btn,
.btn-group-vertical > .btn {
  float: right;
}
.pulse,
.dropdown-menu > li > a.pulse,
li.pulse > a.dropdown-toggle,
li.pulse.open > a.dropdown-toggle {
  background-color: #F37626;
  color: white;
}
/**
 * Primary styles
 *
 * Author: Jupyter Development Team
 */
/** WARNING IF YOU ARE EDITTING THIS FILE, if this is a .css file, It has a lot
 * of chance of beeing generated from the ../less/[samename].less file, you can
 * try to get back the less file by reverting somme commit in history
 **/
/*
 * We'll try to get something pretty, so we
 * have some strange css to have the scroll bar on
 * the left with fix button on the top right of the tooltip
 */
@-moz-keyframes fadeOut {
  from {
    opacity: 1;
  }
  to {
    opacity: 0;
  }
}
@-webkit-keyframes fadeOut {
  from {
    opacity: 1;
  }
  to {
    opacity: 0;
  }
}
@-moz-keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
@-webkit-keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
/*properties of tooltip after "expand"*/
.bigtooltip {
  overflow: auto;
  height: 200px;
  -webkit-transition-property: height;
  -webkit-transition-duration: 500ms;
  -moz-transition-property: height;
  -moz-transition-duration: 500ms;
  transition-property: height;
  transition-duration: 500ms;
}
/*properties of tooltip before "expand"*/
.smalltooltip {
  -webkit-transition-property: height;
  -webkit-transition-duration: 500ms;
  -moz-transition-property: height;
  -moz-transition-duration: 500ms;
  transition-property: height;
  transition-duration: 500ms;
  text-overflow: ellipsis;
  overflow: hidden;
  height: 80px;
}
.tooltipbuttons {
  position: absolute;
  padding-right: 15px;
  top: 0px;
  right: 0px;
}
.tooltiptext {
  /*avoid the button to overlap on some docstring*/
  padding-right: 30px;
}
.ipython_tooltip {
  max-width: 700px;
  /*fade-in animation when inserted*/
  -webkit-animation: fadeOut 400ms;
  -moz-animation: fadeOut 400ms;
  animation: fadeOut 400ms;
  -webkit-animation: fadeIn 400ms;
  -moz-animation: fadeIn 400ms;
  animation: fadeIn 400ms;
  vertical-align: middle;
  background-color: #f7f7f7;
  overflow: visible;
  border: #ababab 1px solid;
  outline: none;
  padding: 3px;
  margin: 0px;
  padding-left: 7px;
  font-family: monospace;
  min-height: 50px;
  -moz-box-shadow: 0px 6px 10px -1px #adadad;
  -webkit-box-shadow: 0px 6px 10px -1px #adadad;
  box-shadow: 0px 6px 10px -1px #adadad;
  border-radius: 2px;
  position: absolute;
  z-index: 1000;
}
.ipython_tooltip a {
  float: right;
}
.ipython_tooltip .tooltiptext pre {
  border: 0;
  border-radius: 0;
  font-size: 100%;
  background-color: #f7f7f7;
}
.pretooltiparrow {
  left: 0px;
  margin: 0px;
  top: -16px;
  width: 40px;
  height: 16px;
  overflow: hidden;
  position: absolute;
}
.pretooltiparrow:before {
  background-color: #f7f7f7;
  border: 1px #ababab solid;
  z-index: 11;
  content: "";
  position: absolute;
  left: 15px;
  top: 10px;
  width: 25px;
  height: 25px;
  -webkit-transform: rotate(45deg);
  -moz-transform: rotate(45deg);
  -ms-transform: rotate(45deg);
  -o-transform: rotate(45deg);
}
ul.typeahead-list i {
  margin-left: -10px;
  width: 18px;
}
[dir="rtl"] ul.typeahead-list i {
  margin-left: 0;
  margin-right: -10px;
}
ul.typeahead-list {
  max-height: 80vh;
  overflow: auto;
}
ul.typeahead-list > li > a {
  /** Firefox bug **/
  /* see https://github.com/jupyter/notebook/issues/559 */
  white-space: normal;
}
ul.typeahead-list  > li > a.pull-right {
  float: left !important;
  float: left;
}
[dir="rtl"] .typeahead-list {
  text-align: right;
}
.cmd-palette .modal-body {
  padding: 7px;
}
.cmd-palette form {
  background: white;
}
.cmd-palette input {
  outline: none;
}
.no-shortcut {
  min-width: 20px;
  color: transparent;
}
[dir="rtl"] .no-shortcut.pull-right {
  float: left !important;
  float: left;
}
[dir="rtl"] .command-shortcut.pull-right {
  float: left !important;
  float: left;
}
.command-shortcut:before {
  content: "(command mode)";
  padding-right: 3px;
  color: #777777;
}
.edit-shortcut:before {
  content: "(edit)";
  padding-right: 3px;
  color: #777777;
}
[dir="rtl"] .edit-shortcut.pull-right {
  float: left !important;
  float: left;
}
#find-and-replace #replace-preview .match,
#find-and-replace #replace-preview .insert {
  background-color: #BBDEFB;
  border-color: #90CAF9;
  border-style: solid;
  border-width: 1px;
  border-radius: 0px;
}
[dir="ltr"] #find-and-replace .input-group-btn + .form-control {
  border-left: none;
}
[dir="rtl"] #find-and-replace .input-group-btn + .form-control {
  border-right: none;
}
#find-and-replace #replace-preview .replace .match {
  background-color: #FFCDD2;
  border-color: #EF9A9A;
  border-radius: 0px;
}
#find-and-replace #replace-preview .replace .insert {
  background-color: #C8E6C9;
  border-color: #A5D6A7;
  border-radius: 0px;
}
#find-and-replace #replace-preview {
  max-height: 60vh;
  overflow: auto;
}
#find-and-replace #replace-preview pre {
  padding: 5px 10px;
}
.terminal-app {
  background: #EEE;
}
.terminal-app #header {
  background: #fff;
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.2);
}
.terminal-app .terminal {
  width: 100%;
  float: left;
  font-family: monospace;
  color: white;
  background: black;
  padding: 0.4em;
  border-radius: 2px;
  -webkit-box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.4);
  box-shadow: 0px 0px 12px 1px rgba(87, 87, 87, 0.4);
}
.terminal-app .terminal,
.terminal-app .terminal dummy-screen {
  line-height: 1em;
  font-size: 14px;
}
.terminal-app .terminal .xterm-rows {
  padding: 10px;
}
.terminal-app .terminal-cursor {
  color: black;
  background: white;
}
.terminal-app #terminado-container {
  margin-top: 20px;
}
/*# sourceMappingURL=style.min.css.map */
    </style>
<style type="text/css">
    .highlight .hll { background-color: #ffffcc }
.highlight  { background: #f8f8f8; }
.highlight .c { color: #408080; font-style: italic } /* Comment */
.highlight .err { border: 1px solid #FF0000 } /* Error */
.highlight .k { color: #008000; font-weight: bold } /* Keyword */
.highlight .o { color: #666666 } /* Operator */
.highlight .ch { color: #408080; font-style: italic } /* Comment.Hashbang */
.highlight .cm { color: #408080; font-style: italic } /* Comment.Multiline */
.highlight .cp { color: #BC7A00 } /* Comment.Preproc */
.highlight .cpf { color: #408080; font-style: italic } /* Comment.PreprocFile */
.highlight .c1 { color: #408080; font-style: italic } /* Comment.Single */
.highlight .cs { color: #408080; font-style: italic } /* Comment.Special */
.highlight .gd { color: #A00000 } /* Generic.Deleted */
.highlight .ge { font-style: italic } /* Generic.Emph */
.highlight .gr { color: #FF0000 } /* Generic.Error */
.highlight .gh { color: #000080; font-weight: bold } /* Generic.Heading */
.highlight .gi { color: #00A000 } /* Generic.Inserted */
.highlight .go { color: #888888 } /* Generic.Output */
.highlight .gp { color: #000080; font-weight: bold } /* Generic.Prompt */
.highlight .gs { font-weight: bold } /* Generic.Strong */
.highlight .gu { color: #800080; font-weight: bold } /* Generic.Subheading */
.highlight .gt { color: #0044DD } /* Generic.Traceback */
.highlight .kc { color: #008000; font-weight: bold } /* Keyword.Constant */
.highlight .kd { color: #008000; font-weight: bold } /* Keyword.Declaration */
.highlight .kn { color: #008000; font-weight: bold } /* Keyword.Namespace */
.highlight .kp { color: #008000 } /* Keyword.Pseudo */
.highlight .kr { color: #008000; font-weight: bold } /* Keyword.Reserved */
.highlight .kt { color: #B00040 } /* Keyword.Type */
.highlight .m { color: #666666 } /* Literal.Number */
.highlight .s { color: #BA2121 } /* Literal.String */
.highlight .na { color: #7D9029 } /* Name.Attribute */
.highlight .nb { color: #008000 } /* Name.Builtin */
.highlight .nc { color: #0000FF; font-weight: bold } /* Name.Class */
.highlight .no { color: #880000 } /* Name.Constant */
.highlight .nd { color: #AA22FF } /* Name.Decorator */
.highlight .ni { color: #999999; font-weight: bold } /* Name.Entity */
.highlight .ne { color: #D2413A; font-weight: bold } /* Name.Exception */
.highlight .nf { color: #0000FF } /* Name.Function */
.highlight .nl { color: #A0A000 } /* Name.Label */
.highlight .nn { color: #0000FF; font-weight: bold } /* Name.Namespace */
.highlight .nt { color: #008000; font-weight: bold } /* Name.Tag */
.highlight .nv { color: #19177C } /* Name.Variable */
.highlight .ow { color: #AA22FF; font-weight: bold } /* Operator.Word */
.highlight .w { color: #bbbbbb } /* Text.Whitespace */
.highlight .mb { color: #666666 } /* Literal.Number.Bin */
.highlight .mf { color: #666666 } /* Literal.Number.Float */
.highlight .mh { color: #666666 } /* Literal.Number.Hex */
.highlight .mi { color: #666666 } /* Literal.Number.Integer */
.highlight .mo { color: #666666 } /* Literal.Number.Oct */
.highlight .sa { color: #BA2121 } /* Literal.String.Affix */
.highlight .sb { color: #BA2121 } /* Literal.String.Backtick */
.highlight .sc { color: #BA2121 } /* Literal.String.Char */
.highlight .dl { color: #BA2121 } /* Literal.String.Delimiter */
.highlight .sd { color: #BA2121; font-style: italic } /* Literal.String.Doc */
.highlight .s2 { color: #BA2121 } /* Literal.String.Double */
.highlight .se { color: #BB6622; font-weight: bold } /* Literal.String.Escape */
.highlight .sh { color: #BA2121 } /* Literal.String.Heredoc */
.highlight .si { color: #BB6688; font-weight: bold } /* Literal.String.Interpol */
.highlight .sx { color: #008000 } /* Literal.String.Other */
.highlight .sr { color: #BB6688 } /* Literal.String.Regex */
.highlight .s1 { color: #BA2121 } /* Literal.String.Single */
.highlight .ss { color: #19177C } /* Literal.String.Symbol */
.highlight .bp { color: #008000 } /* Name.Builtin.Pseudo */
.highlight .fm { color: #0000FF } /* Name.Function.Magic */
.highlight .vc { color: #19177C } /* Name.Variable.Class */
.highlight .vg { color: #19177C } /* Name.Variable.Global */
.highlight .vi { color: #19177C } /* Name.Variable.Instance */
.highlight .vm { color: #19177C } /* Name.Variable.Magic */
.highlight .il { color: #666666 } /* Literal.Number.Integer.Long */
    </style>


<style type="text/css">
/* Overrides of notebook CSS for static HTML export */
body {
  overflow: visible;
  padding: 8px;
}

div#notebook {
  overflow: visible;
  border-top: none;
}@media print {
  div.cell {
    display: block;
    page-break-inside: avoid;
  }
  div.output_wrapper {
    display: block;
    page-break-inside: avoid;
  }
  div.output {
    display: block;
    page-break-inside: avoid;
  }
}
</style>

<!-- Custom stylesheet, it must be in the same directory as the html file -->
<link rel="stylesheet" href="custom.css">

<!-- Loading mathjax macro -->
<!-- Load mathjax -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.5/latest.js?config=TeX-AMS_HTML"></script>
    <!-- MathJax configuration -->
    <script type="text/x-mathjax-config">
    MathJax.Hub.Config({
        tex2jax: {
            inlineMath: [ ['$','$'], ["\\(","\\)"] ],
            displayMath: [ ['$$','$$'], ["\\[","\\]"] ],
            processEscapes: true,
            processEnvironments: true
        },
        // Center justify equations in code and markdown cells. Elsewhere
        // we use CSS to left justify single line equations in code cells.
        displayAlign: 'center',
        "HTML-CSS": {
            styles: {'.MathJax_Display': {"margin": 0}},
            linebreaks: { automatic: true }
        }
    });
    </script>
    <!-- End of mathjax configuration --></head>
<body>
  <div tabindex="-1" id="notebook" class="border-box-sizing">
    <div class="container" id="notebook-container">

<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h1 id="Noise-Examples">Noise Examples<a class="anchor-link" href="#Noise-Examples">&#182;</a></h1><p>URL: <a href="https://github.com/python-acoustics/python-acoustics/blob/master/acoustics/generator.py">https://github.com/python-acoustics/python-acoustics/blob/master/acoustics/generator.py</a></p>
<table>
<thead><tr>
<th style="text-align:left">Color</th>
<th style="text-align:right">Power</th>
<th style="text-align:right">Power density</th>
</tr>
</thead>
<tbody>
<tr>
<td style="text-align:left">White</td>
<td style="text-align:right">+3 dB</td>
<td style="text-align:right">0 dB</td>
</tr>
<tr>
<td style="text-align:left">Pink</td>
<td style="text-align:right">0 dB</td>
<td style="text-align:right">-3 dB</td>
</tr>
<tr>
<td style="text-align:left">Blue</td>
<td style="text-align:right">+6 dB</td>
<td style="text-align:right">+3 dB</td>
</tr>
<tr>
<td style="text-align:left">Brown</td>
<td style="text-align:right">-3 dB</td>
<td style="text-align:right">-6 dB</td>
</tr>
<tr>
<td style="text-align:left">Violet</td>
<td style="text-align:right">+9 dB</td>
<td style="text-align:right">+6 dB</td>
</tr>
</tbody>
</table>

</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[1]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">import</span> <span class="nn">acoustics</span>
<span class="kn">import</span> <span class="nn">numpy</span> <span class="k">as</span> <span class="nn">np</span>
<span class="kn">import</span> <span class="nn">matplotlib.pyplot</span> <span class="k">as</span> <span class="nn">plt</span>
</pre></div>

    </div>
</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h3 id="White-Noise">White Noise<a class="anchor-link" href="#White-Noise">&#182;</a></h3>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[2]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">white</span> <span class="o">=</span> <span class="n">acoustics</span><span class="o">.</span><span class="n">generator</span><span class="o">.</span><span class="n">noise</span><span class="p">(</span><span class="n">N</span><span class="o">=</span><span class="mi">150</span><span class="p">,</span> <span class="n">color</span><span class="o">=</span><span class="s1">&#39;white&#39;</span><span class="p">,</span> <span class="n">state</span><span class="o">=</span><span class="kc">None</span><span class="p">)</span>
<span class="nb">print</span><span class="p">(</span><span class="n">white</span><span class="o">.</span><span class="n">shape</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">white</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">show</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>(150,)
</pre>
</div>
</div>

<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h3 id="Pink-Noise">Pink Noise<a class="anchor-link" href="#Pink-Noise">&#182;</a></h3>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[3]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">pink</span> <span class="o">=</span> <span class="n">acoustics</span><span class="o">.</span><span class="n">generator</span><span class="o">.</span><span class="n">noise</span><span class="p">(</span><span class="n">N</span><span class="o">=</span><span class="mi">150</span><span class="p">,</span> <span class="n">color</span><span class="o">=</span><span class="s1">&#39;pink&#39;</span><span class="p">,</span> <span class="n">state</span><span class="o">=</span><span class="kc">None</span><span class="p">)</span>
<span class="nb">print</span><span class="p">(</span><span class="n">pink</span><span class="o">.</span><span class="n">shape</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">pink</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">show</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>(150,)
</pre>
</div>
</div>

<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h3 id="Blue-Noise">Blue Noise<a class="anchor-link" href="#Blue-Noise">&#182;</a></h3>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[4]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">blue</span> <span class="o">=</span> <span class="n">acoustics</span><span class="o">.</span><span class="n">generator</span><span class="o">.</span><span class="n">noise</span><span class="p">(</span><span class="n">N</span><span class="o">=</span><span class="mi">150</span><span class="p">,</span> <span class="n">color</span><span class="o">=</span><span class="s1">&#39;blue&#39;</span><span class="p">,</span> <span class="n">state</span><span class="o">=</span><span class="kc">None</span><span class="p">)</span>
<span class="nb">print</span><span class="p">(</span><span class="n">blue</span><span class="o">.</span><span class="n">shape</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">blue</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">show</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>(150,)
</pre>
</div>
</div>

<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h3 id="Brown-Noise">Brown Noise<a class="anchor-link" href="#Brown-Noise">&#182;</a></h3>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[5]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">brown</span> <span class="o">=</span> <span class="n">acoustics</span><span class="o">.</span><span class="n">generator</span><span class="o">.</span><span class="n">noise</span><span class="p">(</span><span class="n">N</span><span class="o">=</span><span class="mi">150</span><span class="p">,</span> <span class="n">color</span><span class="o">=</span><span class="s1">&#39;brown&#39;</span><span class="p">,</span> <span class="n">state</span><span class="o">=</span><span class="kc">None</span><span class="p">)</span>
<span class="nb">print</span><span class="p">(</span><span class="n">brown</span><span class="o">.</span><span class="n">shape</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">brown</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">show</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>(150,)
</pre>
</div>
</div>

<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h3 id="Violet-Noise">Violet Noise<a class="anchor-link" href="#Violet-Noise">&#182;</a></h3>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[6]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">violet</span> <span class="o">=</span> <span class="n">acoustics</span><span class="o">.</span><span class="n">generator</span><span class="o">.</span><span class="n">noise</span><span class="p">(</span><span class="n">N</span><span class="o">=</span><span class="mi">150</span><span class="p">,</span> <span class="n">color</span><span class="o">=</span><span class="s1">&#39;violet&#39;</span><span class="p">,</span> <span class="n">state</span><span class="o">=</span><span class="kc">None</span><span class="p">)</span>
<span class="nb">print</span><span class="p">(</span><span class="n">violet</span><span class="o">.</span><span class="n">shape</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">violet</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">show</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>(150,)
</pre>
</div>
</div>

<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing text_cell rendered"><div class="prompt input_prompt">
</div><div class="inner_cell">
<div class="text_cell_render border-box-sizing rendered_html">
<h2 id="Apply-to-Wave-Data">Apply to Wave Data<a class="anchor-link" href="#Apply-to-Wave-Data">&#182;</a></h2>
</div>
</div>
</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[7]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">import</span> <span class="nn">source.connecter</span> <span class="k">as</span> <span class="nn">con</span>
<span class="kn">import</span> <span class="nn">source.datamanager</span> <span class="k">as</span> <span class="nn">dman</span>

<span class="n">features_use</span> <span class="o">=</span> <span class="n">con</span><span class="o">.</span><span class="n">features</span><span class="p">(</span><span class="mi">14</span><span class="p">)</span>
<span class="nb">print</span><span class="p">(</span><span class="s2">&quot;Features:&quot;</span><span class="p">,</span> <span class="n">features_use</span><span class="p">)</span>

<span class="n">dataset</span> <span class="o">=</span> <span class="n">dman</span><span class="o">.</span><span class="n">Dataset</span><span class="p">(</span><span class="nb">set</span><span class="o">=</span><span class="s2">&quot;Normal_VS_A&quot;</span><span class="p">,</span> <span class="n">features</span><span class="o">=</span><span class="n">features_use</span><span class="p">,</span> <span class="n">key</span><span class="o">=</span><span class="s2">&quot;Normal&quot;</span><span class="p">,</span> \
                       <span class="n">balance</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span> <span class="n">smoothing</span><span class="o">=</span><span class="mi">0</span><span class="p">,</span> \
                       <span class="n">cv_te</span><span class="o">=</span><span class="mi">0</span><span class="p">,</span> <span class="n">cv_tot</span><span class="o">=</span><span class="mi">10</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stderr output_text">
<pre>Using TensorFlow backend.
/Users/1004613/tensorflow-cpu/lib/python3.7/site-packages/tensorflow/python/framework/dtypes.py:516: FutureWarning: Passing (type, 1) or &#39;1type&#39; as a synonym of type is deprecated; in a future version of numpy, it will be understood as (type, (1,)) / &#39;(1,)type&#39;.
  _np_qint8 = np.dtype([(&#34;qint8&#34;, np.int8, 1)])
/Users/1004613/tensorflow-cpu/lib/python3.7/site-packages/tensorflow/python/framework/dtypes.py:517: FutureWarning: Passing (type, 1) or &#39;1type&#39; as a synonym of type is deprecated; in a future version of numpy, it will be understood as (type, (1,)) / &#39;(1,)type&#39;.
  _np_quint8 = np.dtype([(&#34;quint8&#34;, np.uint8, 1)])
/Users/1004613/tensorflow-cpu/lib/python3.7/site-packages/tensorflow/python/framework/dtypes.py:518: FutureWarning: Passing (type, 1) or &#39;1type&#39; as a synonym of type is deprecated; in a future version of numpy, it will be understood as (type, (1,)) / &#39;(1,)type&#39;.
  _np_qint16 = np.dtype([(&#34;qint16&#34;, np.int16, 1)])
/Users/1004613/tensorflow-cpu/lib/python3.7/site-packages/tensorflow/python/framework/dtypes.py:519: FutureWarning: Passing (type, 1) or &#39;1type&#39; as a synonym of type is deprecated; in a future version of numpy, it will be understood as (type, (1,)) / &#39;(1,)type&#39;.
  _np_quint16 = np.dtype([(&#34;quint16&#34;, np.uint16, 1)])
/Users/1004613/tensorflow-cpu/lib/python3.7/site-packages/tensorflow/python/framework/dtypes.py:520: FutureWarning: Passing (type, 1) or &#39;1type&#39; as a synonym of type is deprecated; in a future version of numpy, it will be understood as (type, (1,)) / &#39;(1,)type&#39;.
  _np_qint32 = np.dtype([(&#34;qint32&#34;, np.int32, 1)])
/Users/1004613/tensorflow-cpu/lib/python3.7/site-packages/tensorflow/python/framework/dtypes.py:525: FutureWarning: Passing (type, 1) or &#39;1type&#39; as a synonym of type is deprecated; in a future version of numpy, it will be understood as (type, (1,)) / &#39;(1,)type&#39;.
  np_resource = np.dtype([(&#34;resource&#34;, np.ubyte, 1)])
/Users/1004613/tensorflow-cpu/lib/python3.7/site-packages/tensorboard/compat/tensorflow_stub/dtypes.py:541: FutureWarning: Passing (type, 1) or &#39;1type&#39; as a synonym of type is deprecated; in a future version of numpy, it will be understood as (type, (1,)) / &#39;(1,)type&#39;.
  _np_qint8 = np.dtype([(&#34;qint8&#34;, np.int8, 1)])
/Users/1004613/tensorflow-cpu/lib/python3.7/site-packages/tensorboard/compat/tensorflow_stub/dtypes.py:542: FutureWarning: Passing (type, 1) or &#39;1type&#39; as a synonym of type is deprecated; in a future version of numpy, it will be understood as (type, (1,)) / &#39;(1,)type&#39;.
  _np_quint8 = np.dtype([(&#34;quint8&#34;, np.uint8, 1)])
/Users/1004613/tensorflow-cpu/lib/python3.7/site-packages/tensorboard/compat/tensorflow_stub/dtypes.py:543: FutureWarning: Passing (type, 1) or &#39;1type&#39; as a synonym of type is deprecated; in a future version of numpy, it will be understood as (type, (1,)) / &#39;(1,)type&#39;.
  _np_qint16 = np.dtype([(&#34;qint16&#34;, np.int16, 1)])
/Users/1004613/tensorflow-cpu/lib/python3.7/site-packages/tensorboard/compat/tensorflow_stub/dtypes.py:544: FutureWarning: Passing (type, 1) or &#39;1type&#39; as a synonym of type is deprecated; in a future version of numpy, it will be understood as (type, (1,)) / &#39;(1,)type&#39;.
  _np_quint16 = np.dtype([(&#34;quint16&#34;, np.uint16, 1)])
/Users/1004613/tensorflow-cpu/lib/python3.7/site-packages/tensorboard/compat/tensorflow_stub/dtypes.py:545: FutureWarning: Passing (type, 1) or &#39;1type&#39; as a synonym of type is deprecated; in a future version of numpy, it will be understood as (type, (1,)) / &#39;(1,)type&#39;.
  _np_qint32 = np.dtype([(&#34;qint32&#34;, np.int32, 1)])
/Users/1004613/tensorflow-cpu/lib/python3.7/site-packages/tensorboard/compat/tensorflow_stub/dtypes.py:550: FutureWarning: Passing (type, 1) or &#39;1type&#39; as a synonym of type is deprecated; in a future version of numpy, it will be understood as (type, (1,)) / &#39;(1,)type&#39;.
  np_resource = np.dtype([(&#34;resource&#34;, np.ubyte, 1)])
</pre>
</div>
</div>

<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>Features: [&#39;wave_time&#39;, &#39;wave_speed&#39;, &#39;wave_press&#39;, &#39;wave_position&#39;]

Initializing Dataset...
Set      : Normal_VS_A
Features :  [&#39;wave_time&#39;, &#39;wave_speed&#39;, &#39;wave_press&#39;, &#39;wave_position&#39;]
Key      : Normal
10-Fold, Test:0, Validation 1

Training   | Abnormal:    767   Normal:  12840
Validation | Abnormal:     95   Normal:   1605
Test       | Abnormal:     95   Normal:   1605
Total
Training   :   1700
Validation :   1700
Test       :  13607

Balancing the Training set
Class-0: 13039
Class-1: 12840
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[8]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">x</span><span class="p">,</span> <span class="n">y</span> <span class="o">=</span> <span class="p">[],</span> <span class="p">[]</span>
<span class="n">abnormal</span><span class="p">,</span> <span class="n">normal</span> <span class="o">=</span> <span class="kc">True</span><span class="p">,</span> <span class="kc">True</span>
<span class="k">while</span><span class="p">(</span><span class="kc">True</span><span class="p">):</span>
    <span class="n">x_tmp</span><span class="p">,</span> <span class="n">y_tmp</span><span class="p">,</span> <span class="n">t</span> <span class="o">=</span> <span class="n">dataset</span><span class="o">.</span><span class="n">next_train</span><span class="p">(</span><span class="mi">1</span><span class="p">)</span>

    <span class="k">if</span><span class="p">(</span><span class="n">np</span><span class="o">.</span><span class="n">argmax</span><span class="p">(</span><span class="n">y_tmp</span><span class="p">[</span><span class="mi">0</span><span class="p">])</span> <span class="o">==</span> <span class="mi">0</span> <span class="ow">and</span> <span class="n">abnormal</span><span class="p">):</span>
        <span class="n">x</span><span class="o">.</span><span class="n">append</span><span class="p">(</span><span class="n">x_tmp</span><span class="p">[</span><span class="mi">0</span><span class="p">])</span>
        <span class="n">y</span><span class="o">.</span><span class="n">append</span><span class="p">(</span><span class="n">y_tmp</span><span class="p">[</span><span class="mi">0</span><span class="p">])</span>
        <span class="n">abnormal</span> <span class="o">=</span> <span class="kc">False</span>
    <span class="k">elif</span><span class="p">(</span><span class="n">np</span><span class="o">.</span><span class="n">argmax</span><span class="p">(</span><span class="n">y_tmp</span><span class="p">[</span><span class="mi">0</span><span class="p">])</span> <span class="o">==</span> <span class="mi">1</span> <span class="ow">and</span> <span class="n">normal</span><span class="p">):</span>
        <span class="n">x</span><span class="o">.</span><span class="n">append</span><span class="p">(</span><span class="n">x_tmp</span><span class="p">[</span><span class="mi">0</span><span class="p">])</span>
        <span class="n">y</span><span class="o">.</span><span class="n">append</span><span class="p">(</span><span class="n">y_tmp</span><span class="p">[</span><span class="mi">0</span><span class="p">])</span>
        <span class="n">normal</span> <span class="o">=</span> <span class="kc">False</span>

    <span class="k">if</span><span class="p">(</span><span class="ow">not</span><span class="p">(</span><span class="n">abnormal</span><span class="p">)</span> <span class="ow">and</span> <span class="ow">not</span><span class="p">(</span><span class="n">normal</span><span class="p">)):</span> <span class="k">break</span>

<span class="n">x</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">asarray</span><span class="p">(</span><span class="n">x</span><span class="p">)</span>
<span class="n">y</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">asarray</span><span class="p">(</span><span class="n">y</span><span class="p">)</span>
<span class="nb">print</span><span class="p">(</span><span class="n">x</span><span class="o">.</span><span class="n">shape</span><span class="p">,</span> <span class="n">y</span><span class="o">.</span><span class="n">shape</span><span class="p">)</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>


<div class="output_subarea output_stream output_stdout output_text">
<pre>(2, 150, 4) (2, 2)
</pre>
</div>
</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[9]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">noises</span> <span class="o">=</span> <span class="p">[</span><span class="n">white</span><span class="p">,</span> <span class="n">pink</span><span class="p">,</span> <span class="n">blue</span><span class="p">,</span> <span class="n">brown</span><span class="p">,</span> <span class="n">violet</span><span class="p">]</span>
<span class="n">noisename</span> <span class="o">=</span> <span class="p">[</span><span class="s2">&quot;white&quot;</span><span class="p">,</span> <span class="s2">&quot;pink&quot;</span><span class="p">,</span> <span class="s2">&quot;blue&quot;</span><span class="p">,</span> <span class="s2">&quot;brown&quot;</span><span class="p">,</span> <span class="s2">&quot;violet&quot;</span><span class="p">]</span>

<span class="k">for</span> <span class="n">idx_n</span><span class="p">,</span> <span class="n">noise</span> <span class="ow">in</span> <span class="nb">enumerate</span><span class="p">(</span><span class="n">noises</span><span class="p">):</span>
    <span class="n">applied</span> <span class="o">=</span> <span class="n">x</span><span class="p">[</span><span class="mi">0</span><span class="p">,</span> <span class="p">:,</span> <span class="mi">0</span><span class="p">]</span> <span class="o">+</span> <span class="n">noise</span>

    <span class="n">plt</span><span class="o">.</span><span class="n">figure</span><span class="p">(</span><span class="n">facecolor</span><span class="o">=</span><span class="s1">&#39;white&#39;</span><span class="p">,</span> <span class="n">figsize</span><span class="o">=</span><span class="p">(</span><span class="mi">13</span><span class="p">,</span><span class="mi">3</span><span class="p">))</span>

    <span class="n">plt</span><span class="o">.</span><span class="n">subplot</span><span class="p">(</span><span class="mi">1</span><span class="p">,</span><span class="mi">4</span><span class="p">,</span><span class="mi">1</span><span class="p">)</span>
    <span class="n">plt</span><span class="o">.</span><span class="n">title</span><span class="p">(</span><span class="s2">&quot;origin&quot;</span><span class="p">)</span>
    <span class="n">plt</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">x</span><span class="p">[</span><span class="mi">0</span><span class="p">,</span> <span class="p">:,</span> <span class="mi">0</span><span class="p">])</span>

    <span class="n">plt</span><span class="o">.</span><span class="n">subplot</span><span class="p">(</span><span class="mi">1</span><span class="p">,</span><span class="mi">4</span><span class="p">,</span><span class="mi">2</span><span class="p">)</span>
    <span class="n">plt</span><span class="o">.</span><span class="n">title</span><span class="p">(</span><span class="s2">&quot;</span><span class="si">%s</span><span class="s2"> noise&quot;</span> <span class="o">%</span><span class="p">(</span><span class="n">noisename</span><span class="p">[</span><span class="n">idx_n</span><span class="p">]))</span>
    <span class="n">plt</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">noise</span><span class="p">)</span>

    <span class="n">plt</span><span class="o">.</span><span class="n">subplot</span><span class="p">(</span><span class="mi">1</span><span class="p">,</span><span class="mi">4</span><span class="p">,</span><span class="mi">3</span><span class="p">)</span>
    <span class="n">plt</span><span class="o">.</span><span class="n">title</span><span class="p">(</span><span class="s2">&quot;mix&quot;</span><span class="p">)</span>
    <span class="n">plt</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">applied</span><span class="p">)</span>

    <span class="n">plt</span><span class="o">.</span><span class="n">subplot</span><span class="p">(</span><span class="mi">1</span><span class="p">,</span><span class="mi">4</span><span class="p">,</span><span class="mi">4</span><span class="p">)</span>
    <span class="n">plt</span><span class="o">.</span><span class="n">title</span><span class="p">(</span><span class="s2">&quot;l2-dist&quot;</span><span class="p">)</span>
    <span class="n">plt</span><span class="o">.</span><span class="n">plot</span><span class="p">((</span><span class="n">x</span><span class="p">[</span><span class="mi">0</span><span class="p">,</span> <span class="p">:,</span> <span class="mi">0</span><span class="p">]</span> <span class="o">-</span> <span class="n">applied</span><span class="p">)</span><span class="o">**</span><span class="mi">2</span><span class="p">)</span>

    <span class="n">plt</span><span class="o">.</span><span class="n">show</span><span class="p">()</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">


<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAwcAAADSCAYAAAAfQ7xOAAAABHNCSVQICAgIfAhkiAAAAAlwSFlzAAALEgAACxIB0t1+/AAAADh0RVh0U29mdHdhcmUAbWF0cGxvdGxpYiB2ZXJzaW9uMy4xLjIsIGh0dHA6Ly9tYXRwbG90bGliLm9yZy8li6FKAAAgAElEQVR4nOydd3wUZf7431vSAyShaAihGaQE6YIFUVRAFDlRDiwnKJ6c7eT0Ct5xXz1/FlDvrKenKCqcnthFEIIUERtgpCg99CQEkpDeNrsz8/sjmdnZzW56simf9+vFK8nszDOfmR2eeT7dommahiAIgiAIgiAI7R5roAUQBEEQBEEQBKFlIMqBIAiCIAiCIAiAKAeCIAiCIAiCIFQiyoEgCIIgCIIgCIAoB4IgCIIgCIIgVCLKgSAIgiAIgiAIgCgHbYa77rqLxx57rNH3FYS60rt3b9avX+/zs02bNtGjR49mlqh6Tpw4QWRkJIqiBFoUQagz8vwKrYXq3g11wfs9kpiYyKZNmxo8ruDGHmgBhMbh1VdfbZJ9BaGt07NnT4qKigIthiDUC3l+hdbG0qVLefHFF0lJSaFjx47cfPPNPPnkk9jt9VuS7tmzp8Z9jh07Rp8+fXA6nfU+T3tCPAdtALEYCYIgCILQGigpKeH5558nOzubrVu3smHDBv75z38GWizBhCgHLZh9+/Zx2WWXERUVRWJiIp9//jkAt912G3fffTdXX301ERERfPXVV9x22238/e9/N459+umniY2NpXv37rzxxhtYLBYOHTpkHK/vq7vn/vWvf9GtWzdiY2N56623mv9ihTbFjz/+yKBBg4iOjub222+nrKzM537m5xKo8hyvWrWKYcOGERUVxUUXXcTPP//s95wWi4VXX32Vfv36ERUVxb333oveAF5VVR5//HF69epFt27dmDVrFvn5+UCFRcliseByuQB4++236du3Lx06dKBPnz68++67xjnefPNNBg4cSHR0NJMmTeL48eP1v0mCUA29e/fmmWeeYciQIURERHDHHXdw+vRpJk+eTIcOHbjyyivJzc31eH5zcnLo0aMHK1euBKCoqIiEhASWLVsW4KsRBDd33303l1xyCcHBwcTFxXHLLbfw3Xff+d2/tLSU2267jejoaAYNGsSPP/7o8bk5XGnbtm2MGjWKjh07ctZZZ/Hggw8CMG7cOACioqKIjIzkhx9+aKKraxuIctBCcTqdXHvttUycOJHMzExeeuklbrnlFg4cOADA//73PxYsWEBhYSFjx471ODYpKYlnn32W9evXc+jQoRpj8U6dOkV+fj7p6eksWbKEe++9l9zc3Ka6NKEd8O6777J27VoOHz7MwYMHefzxx+s8xo4dO5gzZw6vvfYaZ86c4Xe/+x1Tp07F4XD4PWbVqlX8+OOP/Pzzz3zwwQesXbsWqFjwv/3223z11VccOXKEoqIi7rvvvirHFxcXc//997NmzRoKCwv5/vvvGTZsGAArVqzgySef5JNPPiErK4tLLrmEm266qc7XJQi15eOPP2bdunUcPHiQlStXMnnyZJ588kmysrJQVZUXX3zRY/+YmBjefPNN7rzzTjIzM3nggQcYNmwYs2bNCtAVCELNbN68mcTERL+fP/rooxw+fJjDhw+zdu1ali5d6nffefPmMW/ePAoKCjh8+DAzZswwzgGQl5dHUVERF154YeNeRBtDlIMWypYtWygqKuKhhx4iODiYyy+/nClTpvDee+8B8Ktf/YqLL74Yq9VKaGiox7EffPABt99+O4mJiYSHh/OPf/yj2nMFBQXx8MMPExQUxNVXX01kZKShhAhCfbjvvvuIj48nJiaGBQsWGM9tXVi8eDG/+93vGDNmDDabjdmzZxMSEsKWLVv8HvPQQw8RFRVFz549GT9+PDt37gQqlJUHH3yQvn37EhkZycKFC1m+fLnhLTBjtVrZvXs3paWlxMbGGi+tV199lb/+9a8MHDgQu93O3/72N3bu3CneA6HJ+P3vf89ZZ51FXFwcl1xyCWPGjGH48OGEhoYybdo0duzYUeWYiRMn8utf/5orrriC1atX89prrwVAckGoHW+++SbJycn86U9/8rvPBx98wIIFC4iJiSE+Pp7777/f775BQUEcOnSI7OxsIiMjueCCC5pC7DaPKActlJMnTxIfH4/V6v6KevXqRXp6OgDx8fE1HqtT3b4AnTt39kjQCQ8PlwQ3oUGYn7levXpx8uTJOo9x/Phx/vWvfxEVFWX8S01NrXass88+2/jd/ByfPHmSXr16ecjkcrk4ffq0x/ERERG8//77vPrqq8TGxnLNNdewf/9+Q5558+YZssTExKBpmvF/UhAam7POOsv4PSwsrMrf/ubpuXPnsnv3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
"
>
</div>

</div>

<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAwcAAADSCAYAAAAfQ7xOAAAABHNCSVQICAgIfAhkiAAAAAlwSFlzAAALEgAACxIB0t1+/AAAADh0RVh0U29mdHdhcmUAbWF0cGxvdGxpYiB2ZXJzaW9uMy4xLjIsIGh0dHA6Ly9tYXRwbG90bGliLm9yZy8li6FKAAAgAElEQVR4nOzdd3hUZfrw8e/0SW8kJCSRFlqC9KYiTUBBRBEWVFZAXdnFuvpb192XVdddFQW7a8MKq2vsokgHEQVpS1npCRBIQiC9z0ymnPePyQyTENJIMpPk/lyX10UyJc/EyZlzn7s8KkVRFIQQQgghhBDtntrbCxBCCCGEEEL4BgkOhBBCCCGEEIAEB0IIIYQQQohKEhwIIYQQQgghAAkOhBBCCCGEEJUkOBBCCCGEEEIAEhy0GX/4wx/45z//2eT3FaI2Xbp0YcOGDd5eRrOZNGkSy5Yt8/YyhLio06dPExgYiN1u9/ZShKhVU31ebN68mbi4OPfXSUlJbN68+ZKfV5yn9fYCRNN46623muW+QrRnq1ev9vYShKjVZZddRmlpqbeXIUS9LVu2jFdffZWUlBSCg4O57bbbeOaZZ9BqG3dKevDgwTrvk5aWRteuXbFarY3+Oe2JZA7aALliJFoDm83m7SUIIYTwsvLycl5++WVyc3PZsWMHGzdu5Pnnn/f2soQHCQ582OHDhxkzZgyhoaEkJSXx7bffAjBv3jwWLFjA5MmTCQgI4IcffmDevHn87W9/cz928eLFxMTE0KlTJ959911UKhWpqanux7vu60rPvfDCC0RFRRETE8MHH3zQ8i9WtFq7du0iMTGRsLAw7rjjDsxmM3D+vfXcc88RHR3NHXfcAcA777xDQkIC4eHhTJ06lTNnzgDwxBNPcP/99wNgtVoJCAjgkUceAcBkMmE0GsnPzyctLQ2VSsWyZcu47LLL6NChA08//fRF1zdv3jzuvfderr/+eoKCghg+fDjHjx93375t2zaGDh1KSEgIQ4cOZdu2be7bxowZw7vvvgtAamoqo0ePJiQkhA4dOjBr1iz3/Y4cOcKECRMIDw+nV69efPbZZ03xqxXtWJcuXViyZAn9+vUjICCAu+66i3PnzjFp0iSCgoIYP348BQUF7r8Hm81Gfn4+cXFxfPfddwCUlpaSkJDA8uXLvfxqhDhvwYIFXH311ej1emJjY5k9ezZbt2696P1NJhPz5s0jLCyMxMREdu3aVeV2z3KlnTt3MmTIEIKDg+nYsSMPP/wwAKNGjQIgNDSUwMBAfvnll2Z6dW2DBAc+ymq1csMNNzBx4kSys7N57bXXmD17NkePHgXgP//5DwsXLqSkpISRI0dWeeyaNWt48cUX2bBhA6mpqXXW4p09e5aioiIyMzN57733uPfeeykoKGiulybamI8//pi1a9dy/Phxjh07xlNPPeW+7ezZs+Tn53Pq1CmWLl3Kpk2b+Otf/8pnn31GVlYWnTt35pZbbgFg9OjR7vfqrl27iI6OZsuWLQD88ssv9OrVi/DwcPdz//zzzxw9epSNGzfyj3/8g8OHD190jcnJyTzxxBMUFBSQkJDAwoULAcjPz+f666/ngQceIC8vj4cffpjrr7+evLy8C57jscceY+LEiRQUFJCRkeEOZMrKypgwYQK33XYb2dnZJCcnc88993Do0KFL+8WKdu/LL79k/fr1HDt2jO+++45JkybxzDPPkJOTg8Ph4NVXX61y//DwcN5//33uvvtusrOzeeihhxgwYABz5szx0isQom5btmwhKSnporc/+eSTHD9+nOPHj7N27dpa+8AefPBBHnzwQYqLizl+/DgzZ850/wyAwsJCSktLueKKK5r2RbQxEhz4qO3bt1NaWspf/vIX9Ho948aNY8qUKXzyyScA3HjjjVx11VWo1WqMRmOVx3722WfccccdJCUl4e/vz9///vdaf5ZOp+Pxxx9Hp9MxefJkAgMD3UGIEHW57777iI+PJzw8nIULF7rfowBqtZonn3wSg8GAn58fH3/8MXfeeSeDBg3CYDCwaNEifvnlF9LS0rjiiitISUkhLy+PLVu2cNddd5GZmUlpaSk//vgjo0ePrvJzn3jiCfz8/Ojfvz/9+/dn//79F13jtGnTGDZsGFqtltmzZ7Nv3z4Avv/+e3r06MHtt9+OVqvl1ltvpXfv3u4rr550Oh2nTp3izJkzGI1Gd1C+cuVKunTpwh133IFWq2XgwIFMnz6dzz//vCl+vaIdu//+++nYsSOxsbFcffXVDB8+nIEDB2I0Gpk2bRp79+694DETJ07kN7/5Dddccw2rVq3i7bff9sLKhaif999/n927d/OnP/3povf57LPPWLhwIeHh4cTHx/PAAw9c9L46nY7U1FRy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
"
>
</div>

</div>

<div class="output_area">

    <div class="prompt"></div>




<div class="output_png output_subarea ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>
</div>

</div>
<div class="cell border-box-sizing code_cell rendered">
<div class="input">
<div class="prompt input_prompt">In&nbsp;[&nbsp;]:</div>
<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-ipython3"><pre><span></span>
</pre></div>

    </div>
</div>
</div>

</div>
    </div>
  </div>
</body>




</html>
