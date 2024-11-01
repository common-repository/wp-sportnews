=== WP-Sportnews ===
Contributors: onmarketing1
Donate link: 
Tags: widget, rss, feed, feeds, sidebar, widgets, atom, xml, rss2, sportgate, news, sport, sportnews, sports, sport-news, sportnachrichten, fussball, formel1, formel 1, handball, EM 2008, Olympia, Tennis, Eishockey, Basketball, Ski, Bundesliga, Boxen
Requires at least: 2.0
Tested up to: 2.5
Stable tag: trunk

Adapted version of the KB Advanced RSS Widget to be used with preset Sportgate News Feeds only, complete with user-friendly customization options

== Description ==

This Widget Plugin enables you to display [Sportgate](http://www.sportgate.de/) News Feeds on your WordPress website without knowing anything about the format of the feeds.
Just select from a preset list of categories which feed you want to have displayed and customize its appearance as you like inside the boundaries of Sportgate's presentation options.

* You can have up to 20 widgets with up to 20 items per feed.
* Change the title of each widget to something more pleasing if you like.
* Display news item titles only or title and short description, click title to go directly to the associated Sportgate news article.

It is an adapted version of the [KB Advanced RSS Widget](http://adambrown.info/b/widgets/category/kb-advanced-rss/) by [Adam R. Brown](http://adambrown.info/).

== Installation ==

You MUST be using a widgets-enabled theme. If you are using pre-2.2 WordPress, you'll also need the [sidebar widgets plugin](http://wordpress.org/extend/plugins/widgets/).

1. Upload `WP-Sportnews.php` to either `/wp-content/plugins/widgets/` or `/wp-content/plugins/`.
1. Activate the widget through the 'Plugins' menu in WordPress.
1. Add the new Sportnews widget to your sidebar through the 'Design => Widgets' menu in WordPress.

If you want more Sportnews widgets, scroll down and increase the allotment.

== Frequently Asked Questions ==

= What code do I need to place in my sidebar? =

None. This is a widget. If you are using pre-WP v2.2, you need to have the [widgets plugin](http://wordpress.org/extend/plugins/widgets/) running. No matter what version of WP you're using, you need to be using a widgets-enabled theme.

= The feeds don't update =

They update only once per hour (as coded in `wordpress/includes/rss.php`). If they don't update after more than a couple hours, look in the top of `WP-Sportnews.php` for this line:

`define('SGRSS_FORCECACHE', false);`

and change it to true. This will manually delete the cache if it's more than 1 hour old. In newer versions of Wordpress, manually deleting the cache in this manner might cause a small error next time you load the page. Just reload the page.

= I add the widget to my sidebar, but it doesn't show up =

In the widget's options, make sure the option to hide the widget when the feed is down is **not** checked. Go back to your website and reload.

= The feed is probably down =

This widget relies on Wordpress's feed parsing abilities (look in `wordpress/includes/rss.php`). Wordpress grabs the requested feed then passes it to this widget for formatting. If you are seeing this error, it means one of three things:

1. The feed really is down. Wait a while and try again.
1. Your host is blocking Wordpress from fetching the feed (very likely). [Read more here](http://wordpress.org/support/topic/120458?replies=24#post-602781).
1. Wordpress's feed parser isn't working. Try updating to the most recent version of Wordpress.
1. Some users of this widget have suggested additional solutions to this problem. Check out the comments on [this blog post](http://adambrown.info/b/widgets/2007/08/20/an-error-has-occured-the-feed-is-probably-down/).

In any case, you may want to first try using Wordpress's built-in RSS widget. If neither it nor this widget can display the feed, then you know for certain that it's one of those three reasons--and not the widget itself--causing the failure.

== Screenshots ==

1. Setup screen
2. Example screen
