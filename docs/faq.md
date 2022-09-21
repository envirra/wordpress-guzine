# FAQ

?>**Info** : This section is incomplete. More questions will be added as we receive more questions from our customers</div>

### How to Increase the Limit of Custom Menu Items 
There are two ways to fix the variables to enable a larger number of items to be saved. In most cases, one of these fixes should remove the menu item limit.

##### 1) Editing the .htaccess file.
The first method you could try is to edit the `.htaccess` file which is stored in the home directory of your WordPress installation. You’ll have to connect to your FTP account using some FTP client like FileZilla. Once you connected, open `.htaccess` file and add the following code snippet:

```
php_value max_input_vars 5000
```

From here you can increase the `max_input_vars` limit from 1000 to 5000, which will allow your menu items limit in WordPress to increase automatically. You can also try to increase the value from 5000 to 7000 or more if the limitations persist, however – another reason they may persist is because the PHP server is not responding to your code entry, and in that case you could try to use the solution number two.

##### 2) Editing PHP.INI file.

Editing the Php.ini file is the same thing as with the `.htaccess`. You need to locate your PHP.ini file on your server via FTP and add the following lines of code:

```
max_input_vars = 5000
```

or this:

```
suhosin.post.max_vars = 5000
suhosin.request.max_vars = 5000
```

and restart the server if necessary.

---

### How to improve my website loading speed and performance?

${var.theme-name} is highly optimised right out of the box, and we're constantly working on improvements. However, there are a few recommendations, which can help you to increase your site performance and loading speed:

1. Deactivate and delete all unused plugins, some of them can add an extra script and style files, which can slow down your site.

2. We wouldn't recommend applying a lot of appearance animations on a single page. Big amount of animations requires a lot of processor resources and slows down page viewing.

3. Install and activate some cache plugin, we highly recommend to use [WP Super Cache](https://wordpress.org/plugins/wp-super-cache/) (there are a lot of other caching pluings like [W3 Total Cache](https://wordpress.org/plugins/w3-total-cache/), so you can try them out), because it is made by WordPress developers and constantly updated, also we are using it on our demo sites .

4. If you have a lot of traffic on your site it will be good practice to use CDN, we recommend [CloudFlare](https://www.cloudflare.com), it has a free plan with all basic features.

5. Install some image optimizer plugin like [Smush Image Compression](https://wordpress.org/plugins/wp-smushit/) or [EWWW Image Optimizer](https://wordpress.org/plugins/ewww-image-optimizer/) to optimize images in Media Library.

---

### How to improve SEO? Have you any recommended plugins?

${var.theme-name} comes SEO ready and friendly right out of the box, though a lot of our clients use [Yoast SEO plugin](https://wordpress.org/plugins/wordpress-seo/), which works just fine.

---

### Can't import demo data (never ending process), can I cancel it or what should I do?

Usually, this issue appears due to a lack of memory, **deactivate all 3d party plugins** and try importing once again. If it won't help, we recommend to increase `memory_limit` to **256M**, `max_upload_size` to **50M**, and `max_execution_time` to **300**, you should ask your host to increase these values for PHP.

---

### How to get Google API Key

Please go to [this page](https://developers.google.com/maps/documentation/javascript/get-api-key) to find out more about getting API Key.

---

### How to change 'Read More', 'Load More' wording?

You can change any words by [translation](/translation/README.md#main).

---

### Wrong Facebook sharing image / text, how can I refresh Facebook snippet?

Open [this page](https://developers.facecom/tools/debug/og/object/) in a browser and ask Facebook to refresh snippet for your page.

![](faq/wrong_facebook_image.jpg)

---

### Why doesn't background video play on mobiles automatically?

The autoplay feature was disabled by Apple from iOS 6.1. In Safari on iOS (for all devices, including iPad), where the user may be on a cellular network and be charged per data unit, preload and autoplay are disabled. This means the JavaScript play() and load() methods are also inactive until the user initiates playback by touching a Play button. But for background videos all controls are hidden, just because the video is overlapped by content and user cannot access to the video player directly. **So background videos won't work on iOS devices**.

From **iOS 10** video autoplay policies were changed, so **on iPad with iOS 10 background videos will play automatically if they don't have a sound** (and some other criteria described in [this article](https://webkit.org/blog/6784/new-video-policies-for-ios/)).

---

### Contact form doesn't send emails, how can I resolve the issue?

Most probably, this issue related to wrong server configuration, try to change receiver email to Gmail, if it won't help we recommend to contact your host regarding this issue.

---

### How to install addons if I get this error: "Please adjust file permissions to allow plugins installation"?

There is a chance that uploading feature was disabled by your host, you can try enabling it in `wp-config.php` file within your WordPress folder, append next line to `wp-config.php`:

```
define('FS_METHOD', 'direct');
```

If it doesn't help, add your FTP credentials into wp-config.php file using next example:

```
define('FTP_USER', 'username');
define('FTP_PASS', 'password');
define('FTP_HOST', 'ftp.domain.com');
```