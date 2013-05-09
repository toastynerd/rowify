rowify
======

Rowify is a jQuery based plugin for assisting with responsive column height problems. It works by selecting the container of the elements you would like to equalize, finding the height of its tallest child element, then setting the minimum height of all children to the tallest height. 

To rowify a group of elements, simply select the container wrapping the elements.

$(document).ready(function () {
    $('[data-same-height]').rowify();
});

Easily keep columns even sized even in liquid layouts by running rowify on window resize.

$(window).resize(function () {
    $('[data-same-height]').rowify();
});

You can specify a maximum or minimum height.

$(window).resize(function () {
    $('[data-same-height]').rowify({
      max-height: 400,
      min-height: 100
    });
});