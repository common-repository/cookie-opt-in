=== Cookie Opt In ===
Contributors: clearsite
Donate link: https://www.paypal.com/cgi-bin/webscr?cmd=_donations&business=R8ZWGPA4A6U4Q&lc=NL&item_name=Clearsite%20WordPress&currency_code=EUR&bn=PP%2dDonationsBF%3abtn_donateCC_LG%2egif%3aNonHosted
Tags: DPA, european union, cookie, legal, consent, wpml, multi-language
Requires at least: 3.2.1
Tested up to: 4.3
Stable tag: 1.7.0
License: GPLv2 or later
License URI: http://www.gnu.org/licenses/gpl-2.0.html

European Union law state you must ask permission for cookies. This plugin handles that for you.

== Important message ==

Although technically this plugin could function perfectly, this plugin was created to handle each type of cookie individually, and it still can, the lasw on cookies have changed (simpler) rendering this plugin overly complex to implement and maintain.

Therefore we sadly report that this plugin has been abandoned.

Please use a simpler plugin, like [Cookie Consent](https://wordpress.org/plugins/uk-cookie-consent/).

== Description ==

Important notice before you begin:
+ Currently in legislation is a change to this law that will probably make this plugin useless. The pending changes are that a website can use most if not all cookies just by informing the visitor, no longer needing consent. Consent is implied by using the website.

European law states:

+ A website must inform the visitor about both presence and function of each cookie the website creates
+ A website must ask permission for all cookies other than cookies required for the correct function of the website

Cookies you ARE ALLOWED to create WITHOUT permission are
* Session cookies
* E-commerce cookies that provide a function for the visitor, like shopping cart or product filter settings
* Cookies that define the cookie-preferences of the user

You still need to INFORM the visitor.

Cookies you are NOT allowed to create without permission are
* Analytics cookies
* Advertisement cookies
* Any cookie from a third party (i.e. e.g. neither your website nor your visitor)

Again, you also need to INFORM the visitor.

This plugin will handle all these for you, but it takes some configuration.
If the "offending" scripts are added by action, you can configure the plugin to remove_action it when appropriate.
If an action-removal is not possible you must adapt your plugins and themes.

Technical instructions are available in the plugin after installation.
Also help is available*, for contact details, see the plugin admin pages.

(*) Pricing for help, if applicable, available upon request.

== Installation ==

The plugin installation is pretty straightforward.
1. Upload the unpacked folder to the `/wp-content/plugins/` directory
2. Activate the plugin through the 'Plugins' menu in WordPress
3. See the admin pages for more info.
or
1. Install from wp-admin plugins panel

== Frequently Asked Questions ==

No questions asked as of yet, leave a comment on wordpress.org if you need help or contact us by other means.

= How to activate the Example skin? =

A skin to this plugin is - in effect - a separate WordPress plugin. The Example included is called 'Cookie-Opt-In - Example skin'.

= How can I create my own skin? =

Examine the plugin file 'wp_cookie_opt_in_skin.php'. Here you see reference to a JS and a CSS file. Also examine these two files.
There are 4 PSD files inside the CSS folder to generate new images, or you can use your CSS skills and do without images. If you need a custom designed skin for your website, please [contact us](mailto:info@clearsite.nl?subject=Quotation%20request%20for%20custom%20cookie-opt-in%20design) for a quotation.

== Screenshots ==

4. Example skin - notification bar
5. Example skin - cookie selection panel
6. Example skin - preferences button
1. First visit shows this form. The content of the form is dependant on the configuration, the styling is done by CSS.
2. The INFO that is set in settings is visable, in this case, by clicking the ? . A read-more link is only shown when an URL is filled in.
3. When the visitor has made a choice, (s)he can change it by clicking the cookie (also highly customisable).

== Changelog ==

= 1.7.0 =
* Reboot of the project
* Addressed some jQuery issues to make the plugin once again compatible with all WordPress versions
* The first-visit bar no longer automatically reserves space above the body as in most cases it deformed the website. If you need to create a blank space above the body, add this line above your wp_head() call and adjust the size to your liking. `<script>var cookie_opt_in = { _set_bmt: 100 };</script>`. In a future version, this will be a setting, this is a stop-dead measure. Please note; if your cookie bar also moves downward after this, you probably have your body on position: relative; Use a negative top-position for the cookie bar (CSS), try to remove the position relative, or use position: sticky / fixed for the bar.

= 1.6.x, 1.5.7 =
* Never released to community

= 1.5.6 =
* Internal changes: now update WordPress by way of trunk instead of just the tags.

= 1.5.5 =
* Fixed: For those running PHP in "show all the damn errors" mode, fixed all issues I could find.

= 1.5.4 =
* Added: User suggested changes for displaying correctly in responsive designs

= 1.5.1 =
* Fixed: Default cookie was not correct in javascript with 'If no cookie' settings set to 'Allow'

= 1.4.3 =
* Fixed: one style rule was lost, so I placed a backup one for now

= 1.4.2 =
* Updated: Added PSD files for making a new skin easier
* Updated: Placed all color styles at the top of the skin-stylesheet making color adjustment easier

= 1.4.1 =
* Fixed: A missing text in a jQuery().html() call results in a broken chain, causing the script to crash, burn, explode and die.

= 1.4.0 =
* Added: You can now alter the settings panel from your skin. See the example skin on how to do that.
* Changed: Some minor code cleanup. Plans for a rigorous overhaul are underway. Of course - with backwards compatibility always in mind.

= 1.3.0 =
* Fixed: No longer cache actions on every front-page hit. Don't know what I was thinking. With about 30 plugins active, this would add about 2 seconds to a page load.
* Added: Because of this, caching of actions is only done when asked for; a link is now present on the admin page to clear the cache and a reload of the website will fill it again - once - until the cache is cleared again.
* Fixed: No longer try to remove actions that are references to by objects. It appears that the ID of the action is different each WordPress iteration, so it wasn't functioning at all anyways. Sad note to non-developers; removing an action that is referenced to by object now requires programming skill and in most cases hacking the plugin that adds the action.
* Fixed: a style issue in the example skins that would make the top-bar inherit style from the page-theme. In some cases the site would not be pretty :)
* Added: missing translations for admin interface

= 1.2.5 =
* Added: Now you can set how the system responds if there is no cookie. Cookies are Accepted or Denied until the visitor makes a choice. This is very useful if you want Google to see you're using Google+ and Analytics. Third setting is have Accept/Deny determined by the per-cookie-type-settings 'Default value for new visitors'.
* Added: a little bit of code comment
* Changed: example now reads if (!function_exists(...) || coia(...)) so the code will return true if either the visitor accepts or the function doesn't exist (in case the plugin is off or missing)

= 1.2.3 =
* Fixed: Upgrade from old data-structure now deletes old setting after upgrade, preventing the old settings from reverting the new settings.
* Fixed: Found some more E_NOTICE messages
* Fixed: bug that prevented the use of other languages other than NL and EN.

= 1.2.2 =
* Updated: Interface translation for nl_NL.
* Added: POT Interface translation template added.

= 1.2.1 =
* Fixed: Prevent E_NOTICE messages - http://wordpress.org/support/topic/plugin-cookie-opt-inbugsfixes-lots-of-php-error-notices

= 1.2.0 =
* Feature added: Cookie-Opt-In is now WPML Aware!
* Automatically converts old settings to new
* Settings page handles settings for the selected language through the WPML Language Selector (Admin)
* Front-end listens to the language selected by the visitor (Front-end)

= 1.1.5 =
* Removes: Debug console.log line in js file

= 1.1.4 =
* Added: more exclusions of Google Analytics Filters/Actions to the default list
* Fixed: When clicking View Details, then accept without selecting a cookie-type, settings were not stored (Example skin issue)

= 1.1.1 =
* Minor fixes in translations and texts

= 1.1.0 =
* Made our personal skin available as a demo skin for all of you :)

= 1.0.4 =
* Updated information shown on WordPress.org

= 1.0.3 =
* Fixed issue with preference-cookie not sticking on 32-bit server

= 1.0.2 =
* Allow other types of buttons in interface (not just input.button, but any item with class button inside the scope)

= 1.0.1 =
* Initial release to WordPress.org

== Arbitrary section ==

You may provide arbitrary sections, in the same format as the ones above.  This may be of use for extremely complicated
plugins where more information needs to be conveyed that doesn't fit into the categories of "description" or
"installation."  Arbitrary sections will be shown below the built-in sections outlined above.

== Upgrade Notice ==

* No upgrade notice yet.
