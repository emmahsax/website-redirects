# website-redirects

This repository is designed to be temporary to assist in creating solid 301 redirects from `https://emmasax4.info` and `https://www.emmasax4.info` to `https://emmasax.com`. Technically, `https://www.emmasax4.info` will actually just redirect to `https://emmasax4.info`, which will then further redirect to the `.com` domain.

This repository has one important file called `index.html`. This is the landing page when somebody navigates to `https://emmasax4.info`. Then, it loads the CSS, Bootstrap, fonts, and images from the primary site (I just copy-pasted them into the `assets/` directory... nothing too fancy) so that it has the proper "feel" of the original site and therefore looks authentic. The page has a nice message which says the site has moved (so users know what is happening), and has a button to redirect immediately. Else, there's a redirect that will apply automatically after five seconds.

The redirects are unique because they persist the path of the URL. So, if a user navigates to `https://emmasax4.info/path/to/page/`, then they'll be redirected to `https://emmasax.com/path/to/page/`. To make this work, I used Javascript functions to do the redirects, versus plain HTML, _and_ I created a symlinked file as well: `404.html`.

When a user navigates to any page at `https://emmasax4.info/` that is _not_ the base URL (so there's any path after the first `/`), then they'll be brought to the 404 page (since my static site doesn't have any other pages). And I want the 404 page to have the _exact same_ look and functionality as the primary page, hence why I created a symlink.

```bash
ln -s index.html 404.html
```

I didn't bother filling the "project" with anything more than necessary, which is why the majority of this repository is so empty.

My plan from here on out is to keep this repository and the old domain (`emmasax4.info`) alive for about six months while my SEO ratings come back. And then, I can sunset this repository and just put in plain `http` redirects in my domain name registrar going forward.

Huge thanks to Oleksii Tsvietnov for [the original idea](https://opensource.com/article/19/7/permanently-redirect-github-pages).

---

### Contributing

To submit a feature request, bug ticket, etc, please submit an official [GitHub issue](https://github.com/emmahsax/website-redirects/issues/new). To copy or make changes, please [fork this repository](https://github.com/emmahsax/website-redirects/fork). When/if you'd like to contribute back to this upstream, please create a pull request on this repository.

Please follow included Issue Template(s) and Pull Request Template(s) when creating issues or pull requests.

### Security Policy

To report any security vulnerabilities, please view this repository's [Security Policy](https://github.com/emmahsax/website-redirects/security/policy).

### Licensing

For information on licensing, please see [LICENSE.md](https://github.com/emmahsax/website-redirects/blob/main/LICENSE.md).

### Code of Conduct

When interacting with this repository, please follow [Contributor Covenant's Code of Conduct](https://contributor-covenant.org).

### Archival Notice

This repository has been archived and designated as read-only. From GitHub's documentation:

> This will make the emmahsax/website-redirects repository, issues, pull requests, labels, milestones, projects, wiki, releases, commits, tags, branches, reactions and comments read-only and disable any future comments. The repository can still be forked.

To unarchive this repository at any time, please reach out to me at https://emmasax.com/contact-me/.
