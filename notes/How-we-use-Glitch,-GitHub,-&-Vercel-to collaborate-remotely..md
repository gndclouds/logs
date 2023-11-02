---
title: How we use Glitch, GitHub, & Vercel to collaborate remotely.
publishedAt: 2020-07-29T01:00:00
updatedAt: 2020-07-29T01:00:00
type:
  - Note
published: true
---
Over the past few months, our team has been working interdependently and remotely on some web projects and I wanted to share a bit about our current indie pipeline.

---

🛠 **Glitch** for development →  
📂 **GitHub** for version control →  
🌏 **Vercel** for hosting

---



Here is an overview of how we publish content remotely with each other through using [Glitch](https://glitch.com/) for development, [Github](https://glitch.com/) for version control, and [Vercel](https://vercel/) for hosting.

1. Head to [Glitch](https://glitch.com/@tinyfactories) and make any edits to the project.![Tiny Factories Profile on Glitch](https://res.cloudinary.com/practicaldev/image/fetch/s--IF4d8Rfs--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/i/2tlxk3ehh4rkkvos2qbn.png)
2. Once edits are complete click the `tools` button and then select `Git, Import, and Export`.![Glitch.com](https://res.cloudinary.com/practicaldev/image/fetch/s--mxcpQAlk--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/i/kogj5ro2s5za1w8uqxcj.png)
3. If you see `Connect to GitHub button then click it if not select `Export to GitHub`.![Glitch.com](https://res.cloudinary.com/practicaldev/image/fetch/s--mvga0k8N--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/i/r2s4x39uijft9hah6asz.png)
4. Next, enter the GitHub-account/repo-name you would like to push to in the popup and click `ok`.![Entering repo name](https://res.cloudinary.com/practicaldev/image/fetch/s--WDi8Qcol--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/i/zid0cnt7jl7dejs219yo.png)
5. Enter a detailed description of what you are pushing for example "Updated SEO with new branding" and click `ok`.![Adding Comment](https://res.cloudinary.com/practicaldev/image/fetch/s--9PNSzHbt--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/i/jc0jngezu0z1jnqggugw.png)
6. Now head on over to your [GitHub](https://github.com/tiny-factories) repo and click Compare & pull request. If you do not see this try pushing again from Glitch.![Tiny Factories Github Repo](https://res.cloudinary.com/practicaldev/image/fetch/s--zQGUfOrm--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/i/4puvjgyfkz7m2r37gi4r.png)
7. Add additional comments and click `Create pull request`.![Making Github pull request](https://res.cloudinary.com/practicaldev/image/fetch/s--MjjRK6hZ--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/i/pvfr2xcpe3xib9xhjdw8.png)
8. Next [now.sh](http://now.sh/) will check the code and if everything looks ✅ then you can click `Merge pull request` to push the changes to now.sh and the production or live build.![Checking pull request](https://res.cloudinary.com/practicaldev/image/fetch/s--F3GEqWT3--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/i/hq97z18y7xxg3s10muwp.png)
9. You will be asked to confirm the merge.![Merging pull request](https://res.cloudinary.com/practicaldev/image/fetch/s--MDiGU_aL--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/i/n8q8esdfqm6zg7vca41d.png)
10. That's it! 🎉 Now just wait for your update to go live. If you want to check the progress head on over to your [Vercel Dashboard](https://vercel/tiny-factories/tinyfactories) and click on the project to see the status of the latest build.

[![Vercel Dashboard](https://res.cloudinary.com/practicaldev/image/fetch/s--nbCGrz6Y--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/i/wwz7lerlq3hefy4c9ahi.png)](https://res.cloudinary.com/practicaldev/image/fetch/s--nbCGrz6Y--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/i/wwz7lerlq3hefy4c9ahi.png)

---

This workflow has been great for small projects with just a few people. But in the future, we are looking at switching from [Glitch](https://glitch.com/) to [GitPod](https://www.gitpod.io/) for better react-js support.

We would love to learn more about the workflows you use for your team. Please feel free to share what works best for you and your team with us in the comments or DM us on [Twitter](https://twitter.com/tiny_factories).

---

_[Tiny Factories](https://tinyfactories.space/) is a tribe of indie makers helping each other to ship products. We are working toward a future where folks can be creatively independent by becoming — what we call — an indiepreneur._

_Every two weeks (or so), we send out an update about our project progress. If you’d like to receive this in your inbox, you can subscribe [here](https://tinyletter.com/tiny_factories)._