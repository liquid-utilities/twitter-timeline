# Liquid Twitter Timeline
[heading__title]:
  #liquid-twitter-timeline
  "&#x2B06; Top of ReadMe File"


Third-party _plugin_ written in Liquid for embedding Twitter Timelines within GitHub Pages Themes


## [![Byte size of twitter-timeline.html][badge__master__twitter_timeline__source_code]][twitter_timeline__master__source_code] [![Open Issues][badge__issues__twitter_timeline]][issues__twitter_timeline] [![Open Pull Requests][badge__pull_requests__twitter_timeline]][pull_requests__twitter_timeline] [![Latest commits][badge__commits__twitter_timeline__master]][commits__twitter_timeline__master] [![Twitter Timeline Demos][badge__demo__twitter_timeline]][demo__twitter_timeline]



------


#### Table of Contents


- [:arrow_up: Top of ReadMe File][heading__title]

- [:zap: Quick Start][heading__quick_start]

  - [:memo: Edit Your ReadMe File][heading__your_readme_file]
  - [&#x1F578; Utilize Twitter Timeline][heading__utilize]
  - [:floppy_disk: Commit and Push][heading__commit_and_push]

- [&#x1F5D2; Notes][notes]

- [:card_index: Attribution][heading__attribution]

- [&#x2696; License][heading__license]


------



## Quick Start
[heading__quick_start]:
  #quick-start
  "&#9889; Perhaps as easy as one, 2.0,..."


**Bash Variables**


```Bash
_module_name='twitter-timeline'
_module_https_url="https://github.com/liquid-utilities/${_module_name}.git"
_module_relative_path="_includes/modules/${_module_name}"
```


**Bash Submodule Commands**


```Bash
cd "<your-git-project-path>"

git checkout gh-pages
mkdir -vp "_includes/modules"

git submodule add\
 -b master --name "${_module_name}"\
 "${_module_https_url}" "${_module_relative_path}"
```


### Your ReadMe File
[heading__your_readme_file]:
  #your-readme-file
  "&#x1F578; Suggested additions for your ReadMe.md file so everyone has a good time with submodules"


Suggested additions for your _`ReadMe.md`_ file so everyone has a good time with submodules


```MarkDown
Clone with the following to avoid incomplete downloads


    git clone --recurse-submodules <url-for-your-project>


Update/upgrade submodules via


    git submodule update --init --merge --recursive --remote
```


### Utilize Twitter Timeline
[heading__utilize]:
  #Utilize-twitter-timeline
  "&#x1F578; How to make use of this submodule within another project"


**`_posts/2019-07-10-twitter-timeline.md`**


```MarkDown
---
twitter-timeline:
  name: TwitterDev
  width: 300
  height: 300
  chrome: nofooter noscrollbar noborders transparent
  tweet_limit: 3
  inject_js: true
---
```


**`_layouts/default.html`**


```Liquid
{% comment %} Other theme stuff above... {% endcomment %}

{% include modules/twitter-timeline/twitter-timeline.html %}

{% comment %} Other theme stuff bellow... {% endcomment %}
```


**Example `HTML` output**


```HTML
<a class="twitter-timeline"
   href="https://twitter.com/TwitterDev"
   data-width="300"
   data-height="300"
   data-chrome="nofooter noscrollbar noborders transparent"
   data-tweet-limit="3">Tweets by @TwitterDev</a>

<script>async src="https://platform.twitter.com/widgets.js"</script>
```


### Commit and Push
[heading__commit_and_push]:
  #commit-and-push
  "&#x1F4BE; It may be just this easy..."


```Bash
git add .gitmodules
git add _includes/content-filters/twitter-timeline


## Add any changed files too


git commit -F- <<'EOF'
:heavy_plus_sign: `liquid-utilities/twitter-timeline`



Embeds Twitter Timelines within GitHub Pages via FrontMatter configuration
Must include within `.html` files as `.md` files are exuberantly sanitized
EOF


git push origin gh-pages
```


**:tada: Excellent :tada:** your site is now ready to begin unitizing code from this repository!

___


## Notes
[notes]:
  #notes
  "&#x1F5D2; Additional notes and links that may be worth clicking in the future"


Including code from this repository within MarkDown will result in mangled output, because filters that _`content`_ is pushed through by default. Instead include within `HTML` files from the `_layouts` directory and caution should be used when including within another `_includes` file.


___


## Attribution
[heading__attribution]:
  #attribution
  "&#x1F4C7; Resources that where helpful in building this project so far."


- [Parameter Reference from `developer.twitter.com`](https://developer.twitter.com/en/docs/twitter-for-websites/timelines/guides/parameter-reference)


___


## License
[heading__license]:
  #license
  "&#x2696; Legal bits of Open Source software"


```
Twitter Timeline ReadMe documenting how things like this could be utilized
Copyright (C) 2019  S0AndS0

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU Affero General Public License as published
by the Free Software Foundation; version 3 of the License.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU Affero General Public License for more details.

You should have received a copy of the GNU Affero General Public License
along with this program.  If not, see <https://www.gnu.org/licenses/>.
```



[badge__commits__twitter_timeline__master]:
  https://img.shields.io/github/last-commit/liquid-utilities/twitter-timeline/master.svg

[commits__twitter_timeline__master]:
  https://github.com/liquid-utilities/twitter-timeline/commits/master
  "&#x1F4DD; History of changes on this branch"


[twitter_timeline__community]:
  https://github.com/liquid-utilities/twitter-timeline/community
  "&#x1F331; Dedicated to functioning code"


[twitter_timeline__gh_pages]:
  https://github.com/liquid-utilities/twitter-timeline/tree/gh-pages
  "Source code examples hosted thanks to GitHub Pages!"



[badge__demo__twitter_timeline]:
  https://img.shields.io/website/https/liquid-utilities.github.io/twitter-timeline/index.html.svg?down_color=darkorange&down_message=Offline&label=Demo&logo=Demo%20Site&up_color=success&up_message=Online

[demo__twitter_timeline]:
  https://liquid-utilities.github.io/twitter-timeline/index.html
  "&#x1F52C; Check the posts list for various Timeline tests"


[badge__issues__twitter_timeline]:
  https://img.shields.io/github/issues/liquid-utilities/twitter-timeline.svg

[issues__twitter_timeline]:
  https://github.com/liquid-utilities/twitter-timeline/issues
  "&#x2622; Search for and _bump_ existing issues or open new issues for project maintainer to address."


[badge__pull_requests__twitter_timeline]:
  https://img.shields.io/github/issues-pr/liquid-utilities/twitter-timeline.svg

[pull_requests__twitter_timeline]:
  https://github.com/liquid-utilities/twitter-timeline/pulls
  "&#x1F3D7; Pull Request friendly, though please check the Community guidelines"


[badge__master__twitter_timeline__source_code]:
  https://img.shields.io/github/size/liquid-utilities/twitter-timeline/twitter-timeline.html.svg?label=twitter-timeline.html

[twitter_timeline__master__source_code]:
  https://github.com/liquid-utilities/twitter-timeline/blob/master/twitter-timeline.html
  "&#x2328; Project source, one JavaScript file with ~142 lines of actionable code!"
