# Mustache and Flexbox

  ## Mustache
  > Mustache is a logic-less template syntax.  It can be used for HTML, config files, source code - or anything.  It works by expanding tags in a template using values provided in a hash or object. There are no statements, else clauses, or for loops.  Instead there are only tags. 
  > {{ }} this shows in mustache syntax that this is a placeholder. When mustache compiles this, it will look for the 'name' property in the object we pass in, and replace it with. 
  > You basically have the ability to run mustache inline with Javascript.  It can pass along information and then can render to the DOM, using res.render as its argument. 

  ## Flexbox
  > Properties for the Parent(flex container):
  1. display - this defines a flex container; inline or block depending on the given value. It enables a flex context for all its direct children.
  1. flex-direction - This establishes the main-axis, thus defining the direction flex items are placed in the flex container.
    > These are the following arguments that flex direction will follow;
      1. row (default) -  left to right in ltr; right to left in rtl
      1. row-reverse - right to left in ltr; left to right in rtl
      1. column - same as row but top to bottom
      1. column-reverse - same as row-reverse but bottom to top
  1. flex-wrap - By default, flex items will all try to fit onto one line. You can change that and allow the items to wrap as needed with this property.
    > These are the following arguments that flex-wrap will follow;
      1. nowrap (default) - all flex items will be on one line
      1. wrap -  flex items will wrap onto multiple lines, from top to bottom.
      1. wrap-reverse - flex items will wrap onto multiple lines from bottom to top.
  1. flex-flow - this is a shorthand for the flex-direction and flex-wrap properties, which together define the flex container’s main and cross axes. 
    > The default value is row nowrap.
  1. justify-content - This defines the alignment along the main axis. It helps distribute extra free space leftover when either all the flex items on a line are inflexible, or are flexible but have reached their maximum size.
    > These are the following arguments that justify content will follow;
      1. flex-start (default) - items are packed toward the start of the flex-direction.
      1. flex-end - items are packed toward the end of the flex-direction.
      1. start - items are packed toward the start of the writing-mode direction.
      1. end - items are packed toward the end of the writing-mode direction.
      1. left - items are packed toward left edge of the container, unless that doesn’t make sense with the flex-direction, then it behaves like start.
      1. right - items are packed toward right edge of the container, unless that doesn’t make sense with the flex-direction, then it behaves like start.
      1. center - items are centered along the line
      1. space-between - items are evenly distributed in the line; first item is on the start line, last item on the end line
      1. space-around - items are evenly distributed in the line with equal space around them. Note that visually the spaces aren’t equal, since all the items have equal space on both sides. The first item will have one unit of space against the container edge, but two units of space between the next item because that next item has its own spacing that applies.
      1. space-evenly - items are distributed so that the spacing between any two items (and the space to the edges) is equal.
  1. align-items - This defines the default behavior for how flex items are laid out along the cross axis on the current line. Think of it as the justify-content version for the cross-axis
    > These are the following arguments the align-items will follow;
      1. stretch (default) - stretch to fill the container (still respect min-width/max-width)
      1. flex-start / start / self-start - items are placed at the start of the cross axis. The difference between these is subtle, and is about respecting the flex-direction rules or the writing-mode rules.
      1. flex-end / end / self-end - items are placed at the end of the cross axis. The difference again is subtle and is about respecting flex-direction rules vs. writing-mode rules.
      1. center - items are centered in the cross-axis
      1. baseline - items are aligned such as their baselines align
  1. align-content - This aligns a flex container’s lines within when there is extra space in the cross-axis, similar to how justify-content aligns individual items within the main-axis.
    > These are the following arguments that align-content will follow;
      1. flex-start / start - items packed to the start of the container. The (more supported) flex-start honors the flex-direction while start honors the writing-mode direction.
      1. flex-end / end - items packed to the end of the container. The (more support) flex-end honors the flex-direction while end honors the writing-mode direction.
      1. center - items centered in the container
      1. space-between - items evenly distributed; the first line is at the start of the container while the last one is at the end
      1. space-around - items evenly distributed with equal space around each line
      1. space-evenly - items are evenly distributed with equal space around them
      1. stretch (default) - lines stretch to take up the remaining space
  >Properties for the Children - (flex items)
  1. order - By default, flex items are laid out in the source order. However, the order property controls the order in which they appear in the flex container.
  1. flex-grow - This defines the ability for a flex item to grow if necessary. It accepts a unitless value that serves as a proportion.
  1. flex-shrink - This defines the ability for a flex item to shrink if necessary.
  1. flex-basis - This defines the default size of an element before the remaining space is distributed.
  1. flex - this is the shorthand for flex-grow, flex-shrink and flex-basis combined.
  1. align-self - This allows the default alignment (or the one specified by align-items) to be overridden for individual flex items.
  1. 



