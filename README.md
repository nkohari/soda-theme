# Soda Theme

Dark and light custom UI themes for Sublime Text 2 and Sublime Text 3.

Project site: [http://buymeasoda.github.com/soda-theme/](http://buymeasoda.github.com/soda-theme/)

## Workaround to display sidebar Icons properly

This fork is a workaround related to the issue [#188](https://github.com/buymeasoda/soda-theme/issues/188) to support the new sidebar feature recently added to [ST3 BUILD 3065](http://www.sublimetext.com/3).

As far as I know at the moment of writing this, the new feature of ST3 looks for sidebar icons within the path `icons`. So that means if you are using a Soda Light or Dark Theme the sidebar icons won't display as expected, as you can see in this [screenshot](https://github.com/buymeasoda/soda-theme/issues/188#issue-41501621).

## Sidebar icons configuration
ST3 sidebar feature looks for icons named accordingly its file type within the folder `icons`. So the easiest way I found to get this done was to create a new folder `icons` within this repo and place those icons named as ST3 looks for its file types e.g:  
`file_type_binary.png`,  `file_type_image.png`, `file_type_markup.png` and so on. 

Then a little [hack](https://github.com/adrianorsouza/soda-theme/commit/5430e6a5212a0e11dead6fd841f9db87b0f5848f) was needed to make Soda Theme point to `icons` folder, that way there is no need of hardcoded `tmPreferences`.

## Sidebar icons for Dark Theme

As you can see the changes made in [Soda Dark 3.sublime-theme](https://github.com/adrianorsouza/soda-theme/commit/5430e6a5212a0e11dead6fd841f9db87b0f5848f#diff-7a250dbdfa5e9c254d01b150ecaf51e3) and [Soda Light 3.sublime-theme](https://github.com/adrianorsouza/soda-theme/commit/5430e6a5212a0e11dead6fd841f9db87b0f5848f#diff-d723ca3ee0c360d1c587973fc802fd48L736) point to the same folder, this because ST3 only looks for `icons` folder if you intend to use Dark Theme so you need manually rename `icons_dark` folder to `icons`.


| Sidebar Dark Theme | Sidebar Light Theme
|------------|------------
|![image][1] |![image][2] |

[1]: https://cloud.githubusercontent.com/assets/5430240/4097645/b4260d26-2fdc-11e4-9f09-760dc7bbba06.png

[2]: https://cloud.githubusercontent.com/assets/5430240/4294404/30634d4e-3ddf-11e4-9e92-1d3058e37e3c.png

---
Further reading about Soda Theme please visite https://github.com/buymeasoda/soda-theme

## License

See the original repo.
