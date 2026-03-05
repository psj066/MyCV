# Astrofy | Personal Portfolio Website Template

![Astrofy | Personal Porfolio Website Template](public/social_img.webp)

Astrofy is a free and open-source template for your Personal Portfolio Website built with Astro and TailwindCSS. Create in minutes a website with a Blog, CV, Project Section, Store, and RSS Feed.

## Demo

View a live demo of [Astrofy](https://astrofy-template.netlify.app/)

## Installation

Run the following command in your terminal

```bash
pnpm install
```

Once the packages are installed you are ready to run astro. Astro comes with a built-in development server that has everything you need for project development. The astro dev command will start the local development server so that you can see your new website in action for the very first time.

```bash
pnpm run dev
```

## Tech Stack

- [Astro](https://astro.build)
- [tailwindcss](https://tailwindcss.com/)
- [DaisyUI](https://daisyui.com/)

## Project Structure

```php
├── src/
│   ├── components/
│   │   ├── cv/
│   │   │   ├── TimeLine
│   │   ├── BaseHead.astro
│   │   ├── Card.astro
│   │   ├── Footer.astro
│   │   ├── Header.astro
│   │   └── HorizontalCard.astro
│   │   └── SideBar.astro
│   │   └── SideBarMenu.astro
│   │   └── SideBarFooter.astro
│   ├── content/
│   │   ├── blog/
│   │   │   ├── post1.md
│   │   │   ├── post2.md
│   │   │   └── post3.md
│   │   ├── store/
│   │   │   ├── item1.md
│   │   │   ├── item2.md
│   ├── layouts/
│   │   └── BaseLayout.astro
│   │   └── PostLayout.astro
│   └── pages/
│   │   ├── blog/
│   │   │   ├── [...page].astro
│   │   │   ├── [slug].astro
│   │   └── cv.astro
│   │   └── index.astro
│   │   └── projects.astro
│   │   └── rss.xml.js
│   ├── styles/
│   │   └── global.css
│   └── config.ts
├── public/
│   ├── favicon.svg
│   └── profile.webp
│   └── social_img.webp
├── astro.config.mjs
├── tailwind.config.cjs
├── package.json
└── tsconfig.json
```

### Site config

You can change global site configuration on '/src/config.ts' file:

- **SITE_TITLE**: Default pages title.
- **SITE_DESCRIPTION**: Default pages title.
- **GENERATE_SLUG_FROM_TITLE**: By default Astrofy will generate the blog slug pages base on the article name. Set this var to false if you want to use the Astro file base (Compatible with Astrofy older versions).
- **TRANSITION_API**: Enable and disable transition API

### Components usage

#### Layout Components

The `BaseHead`, `Footer`, `Header`, and `SideBar` components are already included in the layout system. To change the website content you can edit the content of these components.

##### SideBar

In the Sidebar you can change your profilePicture, links to all your website pages, and your social icons.

You can change your avatar shape using [mask classes](https://daisyui.com/components/mask/).

The used social-icons are SVG form [BoxIcons](https://boxicons.com/) pack. You can replace the icons in the `SideBarFooter` component

To add a new page in the sidebar go to the `SideBarMenu` component.

```
<li><a class="py-3 text-base" id="home" href="/">Home</a></li>

```

**Note**: In order to change the sidebar menu's active item, you need to setup the prop `sideBarActiveItemID` in the `BaseLayout` component of your new page and add that id to the link in the `SideBarMenu`

#### TimeLine

The timeline components are used to confirm the CV.

```html
<div class="time-line-container">
  <TimeLineElement title="Element Title" subtitle="Subtitle">
    Content that can contain
    <div>divs</div>
    and <span>anything else you want</span>.
  </TimeLineElement>
  ...
</div>
```

#### Card & HorizontalCard

The cards are primarly used for the Project and the Blog components. They include a picture, a title, and a description. 

```html
<HorizontalCard title="Card Title" img="imge_url" desc="Description" url="Link
URL" target="Optional link target (_blank default)" badge="Optional badge"
tags={['Array','of','tags']} />
```

#### HorizontalCard Shop Item


This component is already included in the Store layout of the template. In case you want to use it in another place these are the props.

```html
<HorizontalShopItem
  title="Item Title"
  img="imge_url"
  desc="Item description"
  pricing="current_price"
  oldPricing="old_price"
  checkoutUrl="external store checkout url"
  badge="Optional badge"
  url="item details url"
  custom_link="Custom link url"
  custom_link_label="Cutom link btn label"
  target="Optional link target (_self default)"
/>
```

#### Adding a Custom Component

To add a custom component, you can create a .astro file in the components folder under the source folder. 

Components must follow this template. The ```---``` represents the code fence and uses Javascript and can be used for imports. 

The HTML component is the actual style of your new component. 

```html
---
// Component Script (JavaScript)
---
<!-- Component Template (HTML + JS Expressions) -->
```

For more details, see the [astro components](https://docs.astro.build/en/core-concepts/astro-components/) documentation here. 

### Layouts

Include `BaseLayout` in each page you add and `PostLayout` to your post pages.

The BaseLayout defines a general template for each new webpage you want to add. It imports constants SITE_TITLE and SITE_DESCRIPTION which can be modified in the ```../config``` folder. Data placed there can be imported anywhere using import. 

### Content

You can add a [content collection](https://docs.astro.build/en/guides/content-collections/) in `/content/' folder, you will need add it at config.ts.

#### config.ts

Where you need to define your content collections, we define our content schemas too.

#### Blog

Add your `md` blog post in the `/content/blog/` folder.

##### Post format

Add code with this format in the top of each post file.

```
---
title: "Post Title"
description: "Description"
pubDate: "Post date format(Sep 10 2022)"
heroImage: "Post Hero Image URL"
---
```

### Pages

#### Blog

Blog uses Astro's content collection to query post's `md`.

##### [page].astro

The `[page].astro` is the route to work with the paginated post list. You can change there the number of items listed for each page and the pagination button labels.

##### [slug].astro

The `[slug].astro` is the base route for every blog post, you can customize the page layout or behaviour, by default uses `content/blog` for content collection and `PostLayout` as layout.

#### Shop

Add your `md` item in the `/pages/shop/` folder.

##### [page].astro

The `[page].astro` is the route to work with the paginated item list. You can change there the number of items listed for each page and the pagination button labels. The shop will render all `.md` files you include inside this folder.

##### Item format

Add code with this format at the top of each item file.

```js
---
title: "Demo Item 1"
description: "Item description"
heroImage: "Item img url"
details: true // show or hide details btn
custom_link_label: "Custom btn link label"
custom_link: "Custom btn link"
pubDate: "Sep 15 2022"
pricing: "$15"
oldPricing: "$25.5"
badge: "Featured"
checkoutUrl: "https://checkouturl.com/"
---
```

#### Static pages

The other pages included in the template are static pages. The `index` page belongs to the root page. You can add your pages directly in the `/pages` folder and then add a link to those pages in the `sidebar` component.

Feel free to modify the content included in the pages that the template contains or add the ones you need.

### Theming

To change the template theme change the `data-theme` attribute of the `<html>` tag in `BaseLayout.astro` file.

You can choose among 30 themes available or create your custom theme. See themes available [here](https://daisyui.com/docs/themes/).

## Sitemap

The Sitemap is generated automatically when you build your website in the root of the domain. Please update the `robots.txt` file in the public folder with your site name URL for the Sitemap.

## Deploy

You can deploy your site on your favourite static hosting service such as Vercel, Netlify, GitHub Pages, etc.

The configuration for the deployment varies depending on the platform where you are going to do it. See the [official Astro information](https://docs.astro.build/en/guides/deploy/) to deploy your website.

> **⚠️ CAUTION** </br>
> The Blog pagination of this template is implemented using dynamic route parameters in its filename and for now this format is incompatible with SSR deploy configs, so please use the default static deploy options for your deployments.

## GitHub Pages 배포 트러블슈팅 (CSS 미적용 문제)

GitHub Pages에 배포했을 때 CSS가 적용되지 않고 스타일 없는 HTML만 표시되는 문제가 발생한 경우, 아래 원인과 해결 방법을 참고하세요.

### 문제 1: `pnpm-lock.yaml` 잔존으로 인한 패키지 매니저 충돌

**증상**: GitHub Actions 빌드 시 `"No pnpm version is specified"` 에러 발생, 빌드 실패.

**원인**: 이 프로젝트 템플릿(Astrofy)은 원래 pnpm 기반으로 만들어져 `pnpm-lock.yaml`이 포함되어 있습니다. `withastro/action@v2`는 lockfile을 감지하여 사용할 패키지 매니저를 자동 선택하는데, `pnpm-lock.yaml`이 존재하면 pnpm을 사용하려고 합니다. 하지만 `package.json`에 pnpm 버전이 지정되어 있지 않아 빌드가 실패합니다.

**해결**: 로컬에서 npm을 사용하는 경우 `pnpm-lock.yaml`을 삭제하고, `deploy.yml`에서 `package-manager: pnpm@latest` 설정을 제거합니다.

```bash
# pnpm-lock.yaml 삭제
rm pnpm-lock.yaml  # (Windows: del pnpm-lock.yaml)
```

### 문제 2: Jekyll이 `_astro/` 폴더를 무시

**증상**: 빌드는 성공하지만, 배포된 사이트에서 `_astro/` 경로의 CSS/JS 파일이 404로 로드 실패.

**원인**: GitHub Pages는 기본적으로 Jekyll을 사용하며, Jekyll은 언더스코어(`_`)로 시작하는 폴더를 무시합니다. Astro는 빌드 결과물(CSS, JS)을 `_astro/` 폴더에 출력하므로, GitHub Pages가 해당 폴더를 서빙하지 않습니다.

**해결**: `public/` 폴더에 빈 `.nojekyll` 파일을 추가합니다. Astro는 빌드 시 `public/`의 파일을 `dist/` 루트에 복사하므로, GitHub Pages가 Jekyll 처리를 건너뛰게 됩니다.

```bash
# 빈 .nojekyll 파일 생성
touch public/.nojekyll  # (Windows: type nul > public\.nojekyll)
```

### 문제 3: `@astrojs/sitemap` 버전 호환성

**증상**: 빌드 도중 `Cannot read properties of undefined (reading 'reduce')` 에러 발생, exit code 1로 빌드 실패.

**원인**: `@astrojs/sitemap`의 최신 버전(v4+)은 Astro v5에서 추가된 `astro:routes:resolved` 훅을 사용합니다. Astro v4 환경에서는 이 훅이 호출되지 않아 `_routes` 변수가 `undefined`가 되면서 에러가 발생합니다.

**해결**: Astro v4와 호환되는 `@astrojs/sitemap@3.2.1`로 다운그레이드합니다.

```bash
npm install @astrojs/sitemap@3.2.1
```

### 요약

| 문제 | 원인 | 해결 |
|------|------|------|
| 패키지 매니저 충돌 | `pnpm-lock.yaml` 잔존 → Actions가 pnpm 사용 시도 | `pnpm-lock.yaml` 삭제 |
| `_astro/` 폴더 무시 | GitHub Pages의 Jekyll이 `_` 폴더 무시 | `public/.nojekyll` 추가 |
| sitemap 빌드 에러 | `@astrojs/sitemap` 최신 버전이 Astro v5 전용 | `@3.2.1`로 다운그레이드 |

## Contributing

Suggestions and pull requests are welcomed! Feel free to open a discussion or an issue for a new feature request or bug.

One of the best ways to contribute is to grab a [bug report or feature suggestion](https://github.com/manuelernestog/astrofy/issues) that has been marked `accepted` and dig in.

Please be wary of working on issues _not_ marked as `accepted`. Just because someone has created an issue doesn't mean we'll accept a pull request for it.

## License

Astrofy is licensed under the MIT license — see the [LICENSE](https://github.com/manuelernestog/astrofy/blob/main/LICENSE) file for details.

## Contributors

<a href="https://github.com/manuelernestog/astrofy/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=manuelernestog/astrofy" />
</a>

Made with [contrib.rocks](https://contrib.rocks).
