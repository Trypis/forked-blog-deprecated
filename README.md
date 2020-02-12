# blog.trypis.ca

A static, serverless personal blog. Forked from [matthewninja](https://github.com/matthewninja/blog.matthewninja.com)

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

### Prerequisites

hugo is used for the template. install it using brew:

```
$ brew install hugo
```

### Installing

Clone the repo

```
$ git clone https://github.com/Trypis/blog.trypis.ca.git
```

### Running locally

From the base dir, run a dev server using hugo:

```
$ hugo server -D
```

### Building

You can build the static site using hugo:

```
$ hugo
```
The static site will be generated in the `public` dir.

### Adding a new blog post

Create a new post:
```
$ hugo new posts/hello-world.md
```
A new file will be created. Add your content! **Remember** to edit draft mode `draft:false` for it to be published!

## Deployment

Personally, I'm using [circleci](https://circleci.com/) for continuous deployment. It uses `.circleci/config.yml` to build the site and deploy it to S3. A cloudfront distribution picks up the static site. 

[Here's the tutorial I used to setup my CD.](https://circleci.com/blog/automate-your-static-site-deployment-with-circleci/)

**note** that the latest hugo docker image is not compatible with this theme. I'm using v0.58, as per `.circleci/config.yml`

## Built With

* [hugo](https://gohugo.io/) - The static web framework used
* [noteworthy](https://github.com/kimcc/hugo-theme-noteworthy) - The hugo theme, published by [kimcc](https://github.com/kimcc)
* [circleci](https://circleci.com/) - Tool for continuous development

## Authors

* **Matthew Ham** - *Original Dev* - [matthewninja](https://github.com/matthewninja)
* **kimcc** - *Theme Author* - [kimcc](https://github.com/kimcc)

## License

This project is licensed under the GNU General Public License v3.0 - see the [LICENSE](LICENSE) file for details
