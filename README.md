# Astro Netlify CMS Example

This was designed to be an example of how to use Astro and NetlifyCMS
together. If you want a bit more explanation of the code, you can follow
through [the blog post on my website](https://prince.dev/astro-netlify-cms)

You can also go and deploy this onto Netlify already with:

[![](https://www.netlify.com/img/deploy/button.svg)](https://app.netlify.com/start/deploy?repository=https://github.com/maxcell/astro-netlifycms-example)

## Getting Started

You will want to make sure to have Node installed. I currently used v16.18.0.

```shell
# After cloning the project down
cd astro-netlifycms-example
npm install
npm run dev
```

This will boot up the project locally at [http://localhost:3000/](http://localhost:3000/).

If you want to see the first blog post you'll want to go to [http://localhost:3000/blog/2021-10-29-my-first-blog-post](http://localhost:3000/blog/2021-10-29-my-first-blog-post).

### Accessing NetlifyCMS locally

In order to access Netlify CMS locally, you will want to make sure to [run the local proxy server](https://www.netlifycms.org/docs/beta-features/#working-with-a-local-git-repository).

To doing so you can open another Terminal and write:

```shell
npx netlify-cms-proxy-server
```

This allows it so you can login locally without actually connecting to any provider. So when you go to [http://localhost:3000/admin](http://localhost:3000/admin), your admin portal, now you should be able to add, update, or delete blog posts! When you deploy your site onto Netlify,
be sure to configure your Netlify Identity so you can log in!

## Architecture

- `src/pages` takes advantage of Astro's File-based routing. So `src/pages/index.astro` maps to `http://localhost:3000/`
- `src/layouts` allows us to define reusable templates we'd want our page(s) to use (in our case the BlogPost layout)
- `public/` are static files we want our website to have such as the favicon


## Want something to add?

Please feel free to open an issue or pull request!