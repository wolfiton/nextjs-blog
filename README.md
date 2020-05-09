# Created for debugging the following error

`TypeError: Cannot read property 'map' of undefined in next 9.3.6`

This is a sample to reproduce the error and is part of the nextjs official tutorial.

## Description

Expected:

This sample should read the markdown files and generate stattic content in the nextjs powered blog from the tutorial.

What is actually happening:

I recieve an error: 

```terminal
TypeError: Cannot read property 'map' of undefined
Home
./pages/index.js:22

  19 | <section className={utilStyles.headingMd}>…</section>
  20 | <section className={`${utilStyles.headingMd} ${utilStyles.padding1px}`}>
  21 |   <h2 className={utilStyles.headingLg}>Blog</h2>
> 22 |   <ul className={utilStyles.list}>
     | ^  23 |     {allPostsData.map(({ id, date, title }) => (
  24 |       <li className={utilStyles.listItem} key={id}>
  25 |         {title}

This screen is visible only in development. It will not appear if the app crashes in production.
Open your browser’s developer console to further inspect this error.
```
