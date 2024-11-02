# Nostr Feed WordPress Plugin

A WordPress plugin that allows you to display posts from specified Nostr public keys (npubs) on your website, with support for Lightning zaps.

## Description

Nostr Feed is a WordPress plugin that integrates Nostr social network posts into your WordPress site. It allows you to display posts from specific Nostr users and enables Lightning Network zaps through WebLN-compatible wallets like Alby.

## Features

- Display Nostr posts from multiple users
- Support for Lightning zaps via WebLN
- Configurable relay connections
- Automatic URL detection and linking
- Image display support
- Clean, responsive design
- Configurable through WordPress admin panel
- Easy integration using shortcode
- Real-time updates from multiple Nostr relays

## Installation

1. Download the plugin files
2. Upload the plugin folder to the `/wp-content/plugins/` directory
3. Activate the plugin through the 'Plugins' menu in WordPress
4. Configure the plugin settings

## Configuration

1. Go to WordPress admin panel
2. Navigate to Settings > Nostr Feed
3. Configure the following settings:
   - **Nostr Public Keys (npubs)**: Enter the Nostr public keys of the users whose posts you want to display
     - Enter one npub per line
     - Example format:
       ```
       npub1abc123...
       npub1xyz789...
       ```
   - **Nostr Relays**: Configure which relays to connect to
     - Enter one relay URL per line
     - Default relays:
       ```
       wss://relay.damus.io
       wss://relay.nostr.band
       wss://nos.lol
       ```
4. Click 'Save Changes'

## Usage

To display the Nostr feed on any page or post, use the shortcode:

```
[nostr_feed]
```

You can add this shortcode in:
- Posts
- Pages
- Widgets (if your theme supports shortcodes in widgets)
- Template files (using `do_shortcode()`)

## Zap Support

The plugin supports sending zaps to Nostr users who have configured Lightning addresses. To use zaps:

1. Install a WebLN-compatible wallet (like [Alby](https://getalby.com))
2. Click the zap button on any post
3. Enter the amount you want to send
4. Confirm the payment in your wallet

## Technical Details

The plugin connects to configured Nostr relays and:
- Fetches posts (kind 1 events)
- Supports image display
- Handles Lightning Network payments via LNURL
- Implements NIP-57 for zaps
- Uses WebLN for Lightning payments

## Styling

The plugin comes with built-in styling that includes:
- Card-based post layout
- Sport-specific color coding
- Responsive design
- Image gallery support
- Hover effects
- Loading animations

Custom CSS classes:
- `.nostr-post`: Individual post container
- `.nostr-post-content`: Post content area
- `.nostr-post-date`: Post date display
- `.nostr-posts`: Main feed container
- `.nostr-post-images`: Image gallery container
- `.nostr-zap-button`: Zap button

## Requirements

- WordPress 5.0 or higher
- PHP 7.0 or higher
- JavaScript enabled in the browser
- WebLN-compatible wallet for zaps (optional)

## Changelog

### 1.0
- Initial release
- Basic Nostr feed functionality
- Admin configuration panel
- Shortcode implementation
- Lightning zap support
- Configurable relays
- Image display support
