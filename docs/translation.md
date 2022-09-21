# Translation

Theme includes bunch of PO translation files for each languages so you can use standard translation tools to help translate theme output strings to your desired language.

### WordPress Language Setting

For WordPress 5 or higher, please follow below steps

1. Login to your WordPress Dashboard and navigate to `Settings > General Settings`
2. Make sure **Site Language** option is set to your desired language.

### Storing Translation Files

Theme use PO translation file which is industry standard translation method. In theme folder you will find a folder called languages. You will find each languages files store in the folder. By default storing inside theme folder. The theme language folder is `wp-content/themes/${var.theme-slug}/languages`.

`*.POT` – A template file for translation

`*.PO` – A lists of all text strings in theme. The text strings are in English and you can add translation to each of text string.

`*.MO` – This is the compiled .po file and is used by WordPress to translate the theme

If your language isn’t included in the theme language files. You have to create a new .PO file from original `${var.theme-slug}.po` located in theme’s languages folder then save the new .PO file with your language code for example `de_DE.po`

This method has one downside. Because whenevery you update the theme. The whole language folder will be replaced with original version which overwrite your translation files. So the solution is to backup your translation file before updating theme.

---

## Using Poedit Application

Poedit application is the popular application uses to edit .PO file translation and it’s free. [Click here to download Poedit application](https://poedit.net).

Now download and install Poedit application. Open language file you want to translate for example `en_US.po` You will find all English string in Source Text box. Select text string you want to translate, add your translation text to **Translation** field. Once you finish translating. Save the file and it will automatically compiled to `.mo` file.

1. Open file `wp-content/themes/${var.theme-slug}/languages/${var.theme-slug}.pot` using [POEdit](http://www.poedit.net/)
2. Click **Create new translation** button and choose the language.
3. Translate the text.
4. Hit save, a new .PO and .MO file will be created.
5. Dont't forget to backup the created .PO and .MO files.

---

## Rename/Change Words

1. Open file `wp-content/themes/${var.theme-slug}/languages/${var.theme-slug}.pot` using [POEdit](http://www.poedit.net/)
2. Click **Create new translation** button and choose the **English** language.
3. Change the words you want.
4. Hit save, a new .PO and .MO file will be created.
5. Dont't forget to backup the created .PO and .MO files.

---

## Using WPML with the Theme

[WPML](https://wpml.org/) makes it easy to run a multilingual website with a single WordPress installation. It comes with over 40 languages. You can also add your own language variants (like Canadian French or Mexican Spanish) using WPML’s languages editor. You can arrange different language contents in the same domain (in language directories), in sub-domains or in completely different domains.

You can find more information in [getting started guide on WPML website.](http://wpml.org/documentation/getting-started-guide/)

#### Important WPML Components

You can enhance your site translation process using these add-on plugins (please note: all of following add-ons are part of WPML Multilingual CMS package):

-   **Translation Management** With this component you can bring more organization into translation process of your site. You can view all types of content with translation status info in one place. Also you can manage people in your team or use translation service right from the translation dashboard. More information here: [usage guide](https://wpml.org/documentation/translating-your-contents/using-the-translation-editor/) and [feature overview](https://wpml.org/documentation/translating-your-contents/using-the-translation-editor/translation-management-features/).

-   **String Translation** This component helps you to translate anything that doesn’t fall inside posts, pages or taxonomy. This includes the site’s tagline, general texts in Admin screens, widget titles and many other texts. More information here: [module activation & first steps](https://wpml.org/documentation/getting-started-guide/string-translation/) and [slugs translation](https://wpml.org/documentation/getting-started-guide/translating-page-slugs/).

#### Need Help for WPML

If you need help with using WPML with TinySalt theme, please head over to [WPML technical forum](https://wpml.org/forums/forum/english-support/). Before posting about issues, we recommend that you review this quick checklist:

- Make sure you have the latest versions of the theme and of the WPML plugins, and that they are all activated. These include WPML Multilingual CMS, WPML String Translation and WPML Translation Management.
- Check that the problem does not appear if the WPML plugins are deactivated, and it does appear when only the core WPML plugins are activated.

> Please always remember to search and read [WPML official documentation](https://wpml.org/documentation/) for more details about how to use WPML.

---

## RTL Support

For languages that read from right-to-left unlike English which is left-to-right, ${var.theme-name} theme will automatically switch to an RTL style, as long as you it's in your language and uses the correct locale (as explained above).
