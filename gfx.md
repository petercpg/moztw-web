# May 16 Release #

來寫 bug list ...

| **Type** | **Release blocker** | **Title/description** | **Blocked by** |
|:---------|:--------------------|:----------------------|:---------------|
| Cosmetic          | Yes (tim)         | JQuery dialog 的大小在 IE6 水土不服，且有可能比小筆電的螢幕大 | 樓下(?) |
| Cosmetic          | Yes (tim)         | JQuery dialog 大小微調 |  |
| Cosmetic          | Yes (tim)         | 沒有人用的推薦頁網址要 show pretty 404 |  |
| -          | Yes               | Icon |  |
| Cosmetic          | No              | Sticker page layout | below |
| -          | Yes               | Sticker |  |
| -          | Yes               | Feature texts |  |
| Function          | No               | Custom feature texts |  |
| Cosmetic, interaction          | No               | About, feature page layout | 還沒有 idea 要怎麼做 |
| Interaction | ?               | Addon list UI | Should improve BUT currently no mock up |
| Interaction | Yes               | Bug: Groups dims when user drags addon | 樓上, 因為不知道是否要砍掉重鍊 |
| Interaction | Yes               | Bug: New addon dialog fail to receive focus after query | (fixed in latest jQuery UI trunk) |
| Interaction, Function          | No                 | Intro, Dashboard, and Login page like http://twitter.com/ , http://twitter.com/home , and http://twitter.com/login | 樓下 |

| Function          | No                 | 沒有吸引使用者回來維護推薦頁的功能 | 討論不出來可以做什麼 |

### Header behavior ###

  1. Always open 「了解本站」 at state 0 (not logged in)
    1. We would like to trick users to scroll down to see everything; the height of first block (features) almost finished at the bottom edge of visible part, users might not able to aware there are more down there.
    1. yet the block might be annoying to page builders, if so the block should always open on top page, with non-invasive speech bubble points to 「了解本站」 button after DOM load.
  1. 「更多...」 Always closed at state 1,2 (login user with or without page)
    1. something more to stuck into the block?

This behavior is due to the fact header block does not know which page it is on without loading javascript, and **show up something after DOM ready is really annoying (i think)**
  * Any behavior plan that breaks this fragment caching scheme is required to make substantial change to the caching system.

## block URLs ##

> 'about',
> 'addons',
> 'auth',
> 'badge',
> 'badges',
> 'blog',
> 'comment',
> 'comments',
> 'doc',
> 'docs',
> 'download',
> 'downloads',
> 'editor',
> 'event',
> 'events',
> 'explore',
> 'feature',
> 'features',
> 'highlight',
> 'highlights',
> 'home',
> 'homes',
> 'help',
> 'helps',
> 'list',
> 'lists',
> 'image',
> 'images',
> 'js',
> 'lobby',
> 'random',
> 'share',
> 'sticker',
> 'stickers',
> 'system',
> 'systems',
> 'user',
> 'users',
> 'useravatar',
> 'useravatars',
> 'userpage',
> 'userpages',
> 'view'

## reserved URLs ##

firefox
mozilla
moztw

# Future Ideas #

  * Add one-line-comment on add-ons one suggest (alicekey)
  * User similarity block on user pages
  * Personal page as identity
> > - user can optionally add open id meta tags
> > - but if one add it's meta tag, then the url can never be changed and will be reserved even if one delete its own account.
  * tagging game for the addons (bobchao)