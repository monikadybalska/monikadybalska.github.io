# How I chose the tech stack that helped me build a website for a Palestinian NGO in two months

![A diagram showing the logos of the technologies discussed in the post](https://monikadybalska.github.io/images/diagram.drawio.png?raw=true)

For the past two months, I have collaborated with [Tech To the Rescue](https://www.techtotherescue.org/) a website to promote the city of Jericho for a non-governmental organisation [Mosaic Centre Jericho](https://mosaiccentrejericho.com/). With the project being both non-profit and me being a relative beginner in frontend development, I found the task of choosing the right tech stack both rewarding and fairly challenging.

We knew what it needed to be and what it needed to have:
- **Fast, performant, and SEO-optimised** to provide the best user experience
- **Headless CMS** for the best performance and flexibility
- **WordPress integration** to allow the organisation to easily update the website in their familiar WordPress environment

Keeping those goals in mind, here's what we chose to build the Visit Jericho website:

## React with Next.js for Javascript
At first, we considered hosting the entire website on the [WordPress](https://wordpress.com/), as it would give a familiar environment for future website administrator. However, since we aimed to provide a modern touch and feel, it seemed right though to use a framework that would allow for more design customisation. With that in mind, we opted for [React](https://react.dev/) paired with [Next.js](https://nextjs.org/). React makes building complex UIs a breeze and helps replicate similar components quickly, which ensured consistency across all the sections, from things to do to travel practicalities.

<br>

<div align="center">
  <img src="https://monikadybalska.github.io/images/lighthouse.png?raw=true" width=500>
  <div>
    <sub>Next.js significantly improved the website's performance and made it easy to implement good SEO practices.</sub>
  </div>
</div>

<br>

As for Next.js, we chose it for the perfect balance between maintainable and bleeding-edge. With the new [App Router](https://nextjs.org/docs/app), we were able to take advantage of the latest React features, such as Server Components and Streaming, which allowed us to optimise the performance of the website and make the user experience smooth without sacrificing reliability.

## Tailwind.CSS for CSS
Since I have used [Material UI](https://mui.com/material-ui/) in the past and appreciated how comprehensive and easy-to-use it was, my initial thought was to select it for this project as well. However, upon doing some more research and learning about the benefits of [Tailwind CSS](https://tailwindcss.com/) (particularly faster development and reduced CSS bundle size), I decided to give it a try. I was happy to discover how seamlessly it integrated with Next.js, and even more happy to see it become my magic utility belt. The pre-built classes for met all of my design needs, making styling a joy and saved tons of development time. 

<br>

<div align="center">
  <img src="https://monikadybalska.github.io/images/tailwind.png?raw=true" width=500>
  <div>
    <sub>Tailwind proved highly flexible and worked very well with component libraries, making it easy to achieve a sleek, consistent design.</sub>
  </div>
</div>

<br>

My initial worry about it not being as flexible as vanilla CSS faded away immediately, as it allowed for maximum customisability and flexibility and had the side effect of actually encouraging me to dive deeper into the CSS fundamentals. Last but not least, since it has considerably grown in popularity in the recent period, it was no trouble finding component libraries that provided sleek design and adhered to accessibility requirements.

## Netlify for deployment
In a search for the most reliable, cost-effective option, we initially considered using [Cloudflare Pages](https://pages.cloudflare.com/) for deployment. However, even though it provides exceptional security, its integration with the Next.js App Router is still in very early stages. Not wanting to lose the crucial features Next.js provided, we decided to explore [Netlify](https://www.netlify.com/). I was immediately stunned by how easy it was for me to navigate it with just an initial skim of the docs. 

<br>

<div align="center">
  <img src="https://monikadybalska.github.io/images/netlify.png?raw=true" width=500>
  <div>
    <sub>Netlify pair extremely well with Next.js, providing a seamless developer experience without sacrificing crucial new features.</sub>
  </div>
</div>

<br>

Netlify's [Next.js runtime](https://docs.netlify.com/frameworks/next-js/overview/) was unbeatable when it came to handling SSR, next/image and other crucial components. Another big advantage was the [Forms](https://docs.netlify.com/forms/setup/) feature — initially, we were hoping to tackle the forms with REST API or the WordPress GraphQL plug-in, but after a while, it started to seem like a losing battle. Netlify's automatic form detection and flexible notification settings allowed me to set up the forms in 15 minutes.

## WordPress with GraphQL for CMS
Making content updates easy for the team at Mosaic Centre Jericho was just as important to us as using modern, scalable technologies. Even though we had several CMSs on our radar and were aware that WordPress was not designed with Next.js or React in mind, we ultimately decided to retain the environment that the future website administrators already used for their existing Mosaic Centre Jericho website. 

<br>

<div align="center">
  <img src="https://monikadybalska.github.io/images/wordpress.png?raw=true" width=500>
  <div>
    <sub>The plug-ins allowed for maximum configurability and helped us translate the schemas into an easy-to-use interface.</sub>
  </div>
</div>

<br>

Using several WordPress plug-ins, namely [Advanced Custom Fields](https://www.advancedcustomfields.com/), [WPGraphQL](https://www.wpgraphql.com/) with the built-in GraphQL IDE, and [Admin Menu Editor](https://pl.wordpress.org/plugins/admin-menu-editor/), we were able to provide an intuitive, smooth experience for both the developers and content editors.

## Cloudfront with S3 Bucket for media optimisation

<br>

<div align="center">
  <img src="https://monikadybalska.github.io/images/cloudfront.png?raw=true" width=500>
  <div>
    <sub>The Offload Media plug-in allowed us to easily configure both the S3 storage and the Cloudfront delivery</sub>
  </div>
</div>

<br>

Since the website design relied heavily on high-quality photos, we were determined to find a smart, cost-effective, and fast CDN. Even though the [Netlify CDN](https://docs.netlify.com/image-cdn/overview/) paired with [Next.js Image](https://nextjs.org/docs/pages/api-reference/components/image) already made for a great performance, we wanted to optimise our media further. We ended up choosing [Amazon Cloudfront](https://aws.amazon.com/cloudfront/) with [Amazon S3](https://aws.amazon.com/s3/) for its reliability and very generous usage limits. With the help of the [WP Offload Media](https://deliciousbrains.com/wp-offload-media/) plug-in, we were able to deliver appropriately-sized, beautiful images and significantly improve page loads and payloads.

## AWS with Lightsail for hosting

<br>

<div align="center">
  <img src="https://monikadybalska.github.io/images/lightsail.png?raw=true" width=500>
  <div>
    <sub>Lightsail makes it very easy to launch an instance and connect it to a WordPress site</sub>
  </div>
</div>

<br>

Finally, we needed a reliable home for the website itself. [Amazon Lightsail](https://aws.amazon.com/lightsail/) offered a perfect balance of features and affordability. It's a virtual server solution within the vast AWS ecosystem, so it's secure and scalable, but with a simple interface that was easy for me to navigate.

## Summary

This tech stack is certainly not the only solution, but for a non-profit travel guide website with a user-friendly CMS and a small development team, it turned out to be just the right combination.

---

## Links

- [Beta version of the website](https://beta.visitjericho.com)
- [GitHub repo](https://github.com/monikadybalska/visitjericho)
