# sveltekit-design-system

This sveltekit design system is a collection of reusable design patterns, rules, and UX guidelines that define a central design language and can be assembled together to build any number of applications.

> In order to quickly iterate with confidence, design teams need access to a single source of truth that allows for a scalable UI language and streamlined UX guidelines. -[Jess Thomas](https://www.invisionapp.com/inside-design/scale-design-systems/)

## Why use a design system?

A comprehensive guide to design systems [InvisionApp](https://www.invisionapp.com/inside-design/guide-to-design-systems/)

1. **Consistency**
2. **Efficiency**
3. **Scale**


- **Create a single source of truth**<br>One place to manage brand and UX components,  coded elements, detailed documentation, and more so teams can stay in sync

- **Design with ease**<br>Update: ~~Integration with Sketch Libraries lets you upload files to DSM in a single click, sync changes, and push and pull design system assets~~

- **Iterate with confidence**<br>Update: ~~Changes sync to the whole team, and users can switch to the latest version or roll back changes at any time~~

- **Manage updates collaboratively**<br>Update: ~~Roles and permissions provide complete control over who can view or edit the design system~~

- **Share with external teams**<br>An automatically generated and customizable documentation site lets any stakeholder preview and use design and code

- **Keep code in sync**<br>Update: ~~Spot existing components and styles with InVision Inspect. And get your production-ready code with a built-in Storybook integration~~

- **Protect your company’s most strategic assets**<br>Confidently create new versions knowing visual assets are safe and secure Update:~~, with role-specific controls and design system-level permissions~~

> Your technical approach doesn’t matter as much as creating a living, breathing system that’s flexible, maintainable, stable, scalable, and successful in the long-term.<br>- **Katie Sylor-Miller**, *senior software engineer, design systems team at Etsy*

## Building a Design System

1. **Conduct a Visual Audit**<br>
The first step in building a design system is to do a visual audit of your current design, whether that’s the design of an app, a website, or some other digital product. Taking inventory of the CSS you’re using and the visual qualities of the elements can help you gauge how much of an undertaking this process might be.

    - Design Audit Example [Eleken](https://www.eleken.co/blog-posts/design-audit-example-insights-to-improve-conversion-rates)
    - How to Conduct a Design Audit of Your Website [Elegant Themes](https://www.elegantthemes.com/blog/tips-tricks/how-to-conduct-a-design-audit-of-your-website)
    - How to Conduct a Design Audit in 2023 [DesignLab](https://designlab.com/blog/how-to-conduct-a-design-audit/)
    - Visual Audit Tools  [CSS Stats](https://cssstats.com)

2. **Create a visual design language**<br>
The visual design language is the core of a design system. It’s made up of the discernible components that you’ll use to construct your digital product. Your visual design language is made up of four main categories, and you should consider the role each of these design elements plays in every component on the screen.
    - **Color**<br>
      Common colors in a design system include 1–3 primaries that represent your brand. You may want to include a range of tints—a color mixed with white—and shades—a color mixed with black—to give your designers a few more options.  

    - **Typography**<br>
      Most design systems include just 2 fonts: 1 font for both headings and body copy, and a monospace font for code. Keep it simple to avoid overloading and confusing your user. Keep the number of fonts low; it’s not only a best practice of typographic design, and it also prevents performance issues caused by excessive use of web fonts. 

    - **Sizing and Spacing**<br>
      The system you use for spacing and sizing looks best when you have rhythm and balance. A 4-based scale is growing in popularity as the recommended scale due to its use in iOS and Android standards, ICO size formats, and even the standard browser font size.

    - **Imagery**<br>
      The key to success with imagery in your visual design language is having a plan and sticking to it. Set guidelines for illustrations and icons, and use the best image format for the situation.

3. **Create a UI/pattern library**<br>
Unlike the visual audit you’ve already conducted (which looked at the visual qualities of your design elements), this step in the process looks at the actual components of your UI. Collect all of the parts and pieces of your UI currently in production. That means every button, form, modal, and image. Merge and remove what you don’t need.

4. **Document what each component is and when/how to use it**<br>
This step is important. Documentation and standards are what separate a pattern library from a true design system.

> Before beginning work on your design system, take a moment to think about the team you’ll need to bring it to life. Who needs to be involved? Spoiler alert! You’re going to need more than just designers.<br>**- Jina Anne**, *design systems advocate and former lead designer at Salesforce*

<hr>

## create-svelte

Everything you need to build a Svelte project, powered by [`create-svelte`](https://github.com/sveltejs/kit/tree/master/packages/create-svelte).

## Creating a project

If you're seeing this, you've probably already done this step. Congrats!

```bash
# create a new project in the current directory
npm create svelte@latest

# create a new project in my-app
npm create svelte@latest my-app
```

## Developing

Once you've created a project and installed dependencies with `npm install` (or `pnpm install` or `yarn`), start a development server:

```bash
npm run dev

# or start the server and open the app in a new browser tab
npm run dev -- --open
```

## Building

To create a production version of your app:

```bash
npm run build
```

You can preview the production build with `npm run preview`.

> To deploy your app, you may need to install an [adapter](https://kit.svelte.dev/docs/adapters) for your target environment.
