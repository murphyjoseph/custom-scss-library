# Custom SCSS Styles

This is a custom SCSS library I made a few years ago (pretty early in my career). I created it because, at the time, there wasn't anything like what we have today (e.g. Chakra or Tailwind). I wanted to have a blend of utility CSS classes auto generated for me and then I wanted to centralize the creation of the theming. 

I don't think I'd use this today because it generates a lot of CSS out of the box. I would likely just use something like Chakra in it's place, but it was a fun thing to make and thought I'd add it here in case anyone finds it interesting.

## How it works

The base folder is probably the most important part of this whole thing. I basically have a core theme folder called `_map-config.scss` which is where you can set whatever values you want for sizing, colors, and even component specific spacing values. Editing anything in there will then auto generate CSS classes for each of the utilities located in `ut-utilities` folder. There's also just a bunch of config files in the base folder that will control exactly how many CSS classes get made and what their names will be.

Probably the best way to understand what this is does is to just view the generated css file. 

## Notes

I'd probably just scrap all the flex box stuff or do it very differently. Creating a grid was a lot harder before we had access to the `column-gap` and `row-gap` css properties. 

If you want to see a quick demo you can just navigate to the index.html file. I didn't spend more than 5 minutes on it but does show it in use. Ideally this whole library would be complimented with feature specific CSS. This was meant to be a nice blend between doing more module related styling with utility classes. I tended to cap the number of CSS classes I'd chain to about 3 before I'd pull out the util classes and generate a single CSS class to represent those styles.