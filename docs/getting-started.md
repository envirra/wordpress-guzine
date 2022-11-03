# Getting Started

## WordPress Installation

For WordPress Installation you can check the Famous 5-Minutes Install [here](https://wordpress.org/support/article/how-to-install-wordpress/)

---

## Theme Requirements

You must be running WordPress ${var.wp-version} or higher, PHP ${var.php-version} or higher, and MySQL 5.7 or higher. We have tested it with Mac, Windows and Linux. Below is a list of items you should ensure your host can comply with.

### Recommended PHP Configuration Limits

White screen, demo content fails when importing, empty page content and other similar issues are all related to low PHP configuration limits. The solution is to increase the PHP limits. You can do this on your own, or contact your web host and ask them to increase those limits to a minimum as follows:

-   max_input_vars = 3000
-   memory_limit = 128M
-   max_execution_time = 300
-   max_input_time = 300
-   upload_max_filesize = 64M
-   post_max_size = 64M

---

## Theme Installation

There are 3 ways to install the theme:

### Theme Installation via WordPress

0. Login to your WordPress admin.
1. In the `Appearance > Themes` menu, click the tab **"Install Themes"**
2. At the top of the page click, **"Upload"**, then click the file input to select a file.
3. Select the zipped theme file, **"${var.theme-slug}.zip"** available in **Theme files** folder from the package downloaded from ThemeForest, and click **"Install Now"**
4. After installation you will receive a success message confirming your new install.
5. Click the link **"Activate"**

##### Common Issues

-   **Are You sure you want to do this?** If you get this message. Please check with your webhost upload file size limit and ask them to increase the limitation.
-   **Theme is missing the style.css stylesheet error** This is because you have choosen an invalid theme file. Please follow instruction on [this page](https://help.market.envato.com/hc/en-us/articles/202821510).
-   **Theme install failed destination folder already exists** This is because WordPress allows you to have only 1 theme with the same name and folder. To get around this issue, please update theme using auto updater or FTP steps above.

### Theme Installation via FTP

0. Login to your FTP server and navigate to your WordPress themes directory.
1. Normally this would be "**wp-content/themes**"
2. Extract the files from the zipped theme available in the package downloaded from ThemeForest.
3. Copy the folder "**${var.theme-slug}**" to your themes directory.
4. After the files finish uploading, login to your WordPress admin.
5. In the **"Appearance"** menu, click **"Themes"**
6. Click **"Activate"** for the theme **"${var.theme-name}"**

### Theme Installation via Envato Market

0. If you already have the "**Envato Market Plugin**" installed on your site then just go to `Admin > Envato Market` and install theme from there. If not, then download the plugin by [clicking on this link](https://www.envato.com/lp/market-plugin/) and install the plugin on your site. After installation, you just need to configure it (linking with your ThemeForest account). [Click here for step-by-step tutorial](https://www.wpexplorer.com/envato-market-plugin-guide/).
1. Then just go to `Admin > Envato Market` plugin menu and install the theme. The theme would be available to install so you can easily install it.
2. **NOTE**: Plesae note that the "**${var.theme-name}**" theme is required plugin for this theme. So make sure you install that plugin after you install/activate the theme.

---

## Activate Theme

Once the theme is uploaded, activate it from `Appearance > Themes` by clicking the **"Activate"** link for **"${var.theme-name}"**.

After you have activated the theme. You need to install the plugins that are required and recommended to use with the theme.

---

## Plugins Installation

After you had activated the theme, you need to install the plugins required by the theme.

0. After you have activated your theme, you'll see a notice about required plugins for **${var.theme-name}**, to proceed click **"Begin installing plugins"**.
1. On clicking on it, you will be redirected to **Install Required Plugins** Page. Alternatively this page can be accessed from `Appearance > Install Plugins` as well.
2. You will now see a list of plugins required and recommended for use with this theme. Click on the **Select All** checkbox to select plugins.
3. Click on **Bulk Actions** dropdown menu, choose **Install** dropdown option and click the **Apply** button.
4. If all plugins are installed successfully, you will be redirected to WP Plugins page.
5. In case you encounter any problems, try installing theme one by one.
6. After you have installed all the plugins, activate them by navigating to **Plugins** page, select the required plugins, choose activate from the dropdown option and click on **Apply** button.

You have now successfully installed and activated the plugins required for ${var.theme-name} WordPress Theme.

---

# Importing Demo Content

Using the WordPress Import tool, you can import demo content into your site from an xml file. The `demo.xml` can be found in the downloaded file from ThemeForest (Please download the **All files and documentation**).

#### Before importing

If the file you’re importing is too large, your server may run out of memory when you import it. If this happens, you’ll see an error like "**Fatal error: Allowed memory size of 8388608 bytes exhausted.**"

If you have sufficient permissions on the server, you can edit the php.ini file to increase the available memory. Alternatively, you could ask your hosting provider to do this. Otherwise, you can edit your import file and save it as several smaller files, then import each one.

If your import process fails, it still may create some content. When you resolve the error and try again, you may create duplicate data. Review your site after a failed import and remove records as necessary to avoid this.

#### Start importing

To import from a WordPress export file into your website. Follow these steps .

1. Log into your site as an WordPress Administrator Panel.

2. Are You Make sure activated your new theme before proceeding.

3. Now Go to `Tools > Import`.

4. Click on“WordPress” from the list.

5. After click on WordPress you will see a popup of **WordPress Importer**. You need to install **WordPress Importer** for uploading XML file. Now click on **Install Now** Button then activate your plugin.

6. Now you can Upload the dummy content `demo.xml` file using the form provided on that page then click on **Upload file and Import** button.

7. You will be asked to map the authors in this export file to users on the blog. For each author, you may choose to map to an existing user on the blog or to create a new user. You will then have the choice to import attachments, so click on the **Download and import file attachments** check-box and click on **Submit** button.

8. Please be patient while WordPress imports all the content.

---

# Update Theme

You can update your theme via FTP or via WordPress. See the information below for each method. No matter what method you choose, you first need to download the new theme files from Themeforest.

#### Prerequisites for updating the theme

0. First you need to download the latest version of theme. Log into your Themeforest account and navigate to your downloads tab. Find the **${var.theme-name}** theme purchase.
1. Click the **download** button next to it and choose to download the **Installable WordPress Theme** which is just the WordPress file, or choose the **Main Files** which is the entire package which include theme documentation, plugins etc.
2. Backup your site before updating the theme. Please follow the steps via using a plugin to automatically backup your current theme and uploading the new version: http://wordpress.org/extend/plugins/easy-theme-and-plugin-upgrades/
3. Backup Setting of Customizer before updating the theme. Please use plugin [Customizer Export/Import](https://wordpress.org/plugins/customizer-export-import/) to backup the setting of Customizer.

#### Method 1 : Update using Envato Market Plugin

0. You need to download the plugin from here.
1. Go to `Themeforest > You Account > Settings > API Key` and copy API Key.
2. Click the **Envato Market** menu in WordPress Dashboard.
3. Enter your API Key and you will be able to see your purchased items which is included ${var.theme-name} theme

#### Method 2 : Update using plugin

0. You need to download and install Easy Theme and Plugin Update.
1. After installing the plugin. Go to `Apperance > Themes > Add New > Upload Theme`
2. Select the downloaded ZIP file and choose **Upgrade existing theme** option to **Yes** and click **Install Now** button

#### Method 3 : Update using WordPress Dashboard

0. You may want to use a plugin to automate backing up your current theme and uploading the new version: http://wordpress.org/extend/plugins/easy-theme-and-plugin-upgrades/
1. You need to deactivate **${var.theme-name}** theme in the `Appearance > Themes` by simply activating a different theme. Once you activate a different theme, you can delete the ${var.theme-name} theme. Don’t worry. You really won’t loose any of your data.
2. Get the installable zip file from `Themeforest > Account > Download`. If you downloaded the **Main Files** from Themeforest, then you need to unzip the archive file you received, the **${var.theme-slug}.zip** will be inside of it.
3. Upload the zip file using `Appearance > Themes`. Once you uploaded successfully, activate the theme.

#### Method 4 : Update using FTP

0. You may want to use a plugin to automate backing up your current theme and uploading the new version: http://wordpress.org/extend/plugins/easy-theme-and-plugin-upgrades/
1. Login to your FTP account. Navigate to `wp-content/themes` location and backup your **${var.theme-slug}** theme folder by saving it to your computer, or you can choose to simply delete it. Don’t worry. You really won’t loose any of your data.
2. Get the installable zip file from `Themeforest > Account > Download`. If you downloaded the **Main Files** from Themeforest, then you need to unzip the archive file you received, the **${var.theme-slug}.zip** will be inside of it.
3. Drag and drop the new **${var.theme-slug}** theme folder into `wp-content/themes` and select **Replace** if you didn’t delete it.

#### Method 5 : Updating from existing theme

If you update your existing blog site to ${var.theme-name} theme. You have to run [this plugin](https://wordpress.org/plugins/regenerate-thumbnails/) to regenerate all posts's thumbnails from your existing theme setting. Once you installed the plugin, open `Tools > Regen. Thumbnails` and click on **Regenerate Thumbnails** button.

#### Common Issues

0. **Are You sure you want to do this?** If you get this message. Please check with your webhost upload file size limit and ask them to increase the limitation.
1. **Theme is missing the style.css stylesheet error** This is because you have choosen an invalid theme file. Please follow instruction on [this page](https://help.market.envato.com/hc/en-us/articles/202821510).
2. **Theme install failed destination folder already exists** This is because WordPress allows you to have only 1 theme with the same name and folder. To get around this issue, please update theme using auto updater or FTP steps above.
