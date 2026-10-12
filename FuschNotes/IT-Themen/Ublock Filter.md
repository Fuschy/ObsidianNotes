! YT - Homepage and Subscriptions (Grid View) - Hide the Shorts section
youtube.com##[is-shorts]
! YT - Menu - Hide the Shorts button
www.youtube.com###guide [title="Shorts"], .ytd-mini-guide-entry-renderer[title="Shorts"]
! YT - Search - Hide Shorts
www.youtube.com##ytd-search ytd-video-renderer:has([overlay-style="SHORTS"],[href^="/shorts/"])
! YT - Search, Channels, Subscriptions (List View) and Sidebar/Below Player Recommendations - Hide the Shorts sections
www.youtube.com##ytd-reel-shelf-renderer
! YT - Channels - Hide the Shorts tab
www.youtube.com##[tab-title="Shorts"]
! YT - Subscriptions - Hide Shorts - Grid View
www.youtube.com##ytd-browse[page-subtype="subscriptions"] ytd-grid-video-renderer:has([overlay-style="SHORTS"],[href^="/shorts/"])
! YT - Subscriptions - Hide Shorts - List View
www.youtube.com##ytd-browse[page-subtype="subscriptions"] ytd-video-renderer:has([overlay-style="SHORTS"],[href^="/shorts/"])
! YT - Subscriptions - New Layout - Hide Shorts
www.youtube.com##ytd-browse[page-subtype="subscriptions"] ytd-rich-item-renderer:has([overlay-style="SHORTS"],[href^="/shorts/"])
! YT - Sidebar - Hide Shorts
www.youtube.com###related :is(ytd-compact-video-renderer,yt-lockup-view-model):has([overlay-style="SHORTS"],[href^="/shorts/"])
! YT - History - Hide Shorts
www.youtube.com##ytd-item-section-renderer[page-subtype]:has(>#contents>[is-history]>#dismissible>ytd-thumbnail>#thumbnail[href^="/shorts/"])

! YT Mobile - Hide the Shorts Menu button
m.youtube.com##ytm-pivot-bar-item-renderer:has(>.pivot-shorts)
! YT Mobile - Hide the Shorts sections
m.youtube.com##ytm-reel-shelf-renderer
m.youtube.com##ytm-rich-section-renderer:has([d^="M17.77,10.32l-1.2"])
! YT Mobile - Search - Hide Shorts
m.youtube.com##ytm-search ytm-video-with-context-renderer:has([data-style="SHORTS"])
! YT Mobile - Channels - Hide the Shorts button
m.youtube.com##[tab-title="Shorts"]
! YT Mobile - History - Hide Shorts
m.youtube.com##[tab-identifier="FEhistory"] ytm-compact-video-renderer:has(>div>a[href^="/shorts/"])

! Youtube videoplayer tweaks

! Remove backgrounds from multiple elements
www.youtube.com##.ytp-button.ytp-play-button, .ytp-button.ytp-next-button, .ytp-button.ytp-prev-button, .ytp-time-wrapper, .ytp-time-display, .ytp-time-duration, .ytp-time-current, .ytp-volume-area, .ytp-volume-slider, .ytp-volume-panel, .ytp-chapter-title, .ytp-right-controls-left, .ytp-right-controls, .ytp-right-controls-right, .ytp-volume-popover:style(background: none !important; backdrop-filter: none !important;)

! Tweaked play and volume buttons
www.youtube.com##.ytp-button.ytp-play-button svg:style(transform: scale(0.85) !important;)
www.youtube.com##.ytp-button.ytp-volume-icon svg:style(transform: scale(0.77))

! compact volume popover
www.youtube.com##.ytp-volume-popover:style(transform: translateX(-70%) translateY(88%) rotate(90deg) !important; height:50px !important; width:150px !important;)


! Smaller SponsorBlock buttons
www.youtube.com###startSegmentButton > .playerButtonImage, #submitButton > .playerButtonImage, #deleteButton > .playerButtonImage, #infoButton > .playerButtonImage:style(transform:scale(0.85) !important;)

! Progress bar & control rows
www.youtube.com##.ytp-progress-bar-container:style(position: relative !important; top: 16px !important;)
www.youtube.com##.ytp-right-controls, .ytp-left-controls:style(position: relative !important; top:5px !important;)

! Fix left-controls blocking progress bar control
www.youtube.com##.ytp-left-controls:style(pointer-events: none !important;)
www.youtube.com##.ytp-left-controls :is(.ytp-button, .ytp-volume-panel):style(pointer-events: auto !important;)

! Remove weird floating buttons
www.youtube.com###movie_player > .ytp-overlays-container > .ytp-overlay-bottom-right

! vol closer to play
www.youtube.com##.ytp-mute-button:style(margin-left:-14px!important;)

! gradient
www.youtube.com###movie_player::after:style(content:"" !important; position:absolute !important; bottom:0 !important; left:0 !important; width:100% !important; height:7% !important; pointer-events:none !important; background:linear-gradient(to top, rgba(0,0,0,0.8), rgba(0,0,0,0)) !important; z-index:40 !important; opacity:0 !important; transition:opacity 0.2s ease !important;)
www.youtube.com###movie_player:not(.ytp-autohide)::after:style(opacity:1 !important;)

! small btns on the right
www.youtube.com##.ytp-right-controls-left:style(transform:scale(0.87) translateX(18%) !important;)
www.youtube.com##.ytp-right-controls-right:style(transform:scale(0.87) translateX(10%) !important;)

! Hide floating overlays (theater)
www.youtube.com##:is(ytd-watch-flexy[theater] .html5-video-player, .html5-video-player.ytp-fullscreen) > .ytp-overlays-container > .ytp-overlay-bottom-right

! Scale down play & vol (theater)
www.youtube.com##:is(ytd-watch-flexy[theater] .html5-video-player, .html5-video-player.ytp-fullscreen) .ytp-button.ytp-play-button svg:style(transform: scale(0.62) !important;)

! Lower btn row (theater)
www.youtube.com##:is(ytd-watch-flexy[theater] .html5-video-player, .html5-video-player.ytp-fullscreen) .ytp-right-controls, :is(ytd-watch-flexy[theater] .html5-video-player, .html5-video-player.ytp-fullscreen) .ytp-left-controls:style(position:relative !important; top:24px !important;)


! nudge play nd vol
www.youtube.com##:is(ytd-watch-flexy[theater] .html5-video-player, .html5-video-player.ytp-fullscreen) .ytp-mute-button:style(margin-left:-31px!important;)
www.youtube.com##:is(ytd-watch-flexy[theater] .html5-video-player, .html5-video-player.ytp-fullscreen) .ytp-button.ytp-play-button:style(margin-left:-12px!important;)

! smaller SponsorBlock btns (theater)
www.youtube.com##:is(ytd-watch-flexy[theater] .html5-video-player, .html5-video-player.ytp-fullscreen) #startSegmentButton > .playerButtonImage, :is(ytd-watch-flexy[theater] .html5-video-player, .html5-video-player.ytp-fullscreen) #submitButton > .playerButtonImage, :is(ytd-watch-flexy[theater] .html5-video-player, .html5-video-player.ytp-fullscreen) #deleteButton > .playerButtonImage, :is(ytd-watch-flexy[theater] .html5-video-player, .html5-video-player.ytp-fullscreen) #infoButton > .playerButtonImage:style(transform: scale(0.64) !important;)

! Lower progress bar (theater)
www.youtube.com##:is(ytd-watch-flexy[theater] .html5-video-player, .html5-video-player.ytp-fullscreen) .ytp-progress-bar-container:style(position:relative !important; top: 54px !important;)

! small btns on the right in theater
www.youtube.com##:is(.html5-video-player.ytp-fullscreen) .ytp-right-controls-left:style(transform:scale(0.83) translateX(20%) !important;)
www.youtube.com##:is(.html5-video-player.ytp-fullscreen) .ytp-right-controls-right:style(transform:scale(0.83) translateX(18%) !important;)

! progress bar btn circle size (theater)
www.youtube.com##:is(ytd-watch-flexy[theater] .html5-video-player, .html5-video-player.ytp-fullscreen) .ytp-swatch-background-color.ytp-scrubber-button:style(transform:scale(0.7) !important;)
www.youtube.com##:is(ytd-watch-flexy[theater] .html5-video-player, .html5-video-player.ytp-fullscreen) .ytp-swatch-background-color.ytp-scrubber-button:hover:style(transform:scale(.85) !important;)

! time display tweaks (theater)
www.youtube.com##:is(ytd-watch-flexy[theater] .html5-video-player, .html5-video-player.ytp-fullscreen) .ytp-time-display:style(font-size:14px !important; opacity:0.9 !important;)



! random sh#

! move the hover seek preview thumbnail closer to the new controls
www.youtube.com##.ytp-tooltip.ytp-preview:style(transform: translateY(24px) !important;)
www.youtube.com##:is(ytd-watch-flexy[theater] .html5-video-player, .html5-video-player.ytp-fullscreen) .ytp-tooltip.ytp-preview:style(transform:translateY(56px) !important;)

! YouTube progress bar + hover
youtube.com##.ytp-progress-bar-container:style(height:7px !important; margin-top:0 !important;)
youtube.com##.ytp-progress-bar-padding:style(height:0 !important; margin-top: 0 !important;)
youtube.com##.ytp-progress-bar:style(height:4px !important; bottom:0 !important;)
youtube.com##.ytp-progress-bar:hover:style(height:5px !important; bottom:0 !important;)
youtube.com##.ytp-hover-progress-bar:style(height: 2px !important; bottom:0 !important;)
youtube.com##.ytp-load-progress:style(height:4px !important; bottom:0 !important;)

! move settings menu closer to new controls
www.youtube.com##:is(ytd-watch-flexy[theater] .html5-video-player, .html5-video-player.ytp-fullscreen) .ytp-popup:style(transform: translateY(50px) !important;)

! Remove white/gray background circles behind yt controls
youtube.com##.ytp-button:style(background:none !important; box-shadow:none !important;)
youtube.com##.ytp-play-button:style(background:none !important;)
youtube.com##.ytp-button::before, .ytp-button::after:style(display:none !important;)
www.youtube.com##.ytp-volume-area::after:style(background:none!important;)

! progress bar handle circle size
www.youtube.com##.ytp-swatch-background-color.ytp-scrubber-button:hover:style(transform: translateY(-1px) scale(1.3) !important;)
www.youtube.com##.ytp-swatch-background-color.ytp-scrubber-button:style(transform: scale(1.1) !important;)

! darken the btns on hover slightly enlargen to add some feedback
youtube.com##.ytp-button svg:style(transition:opacity 0.2s ease-out !important;)
youtube.com##.ytp-button:hover svg:style(opacity:0.75 !important;)
youtube.com##.ytp-size-button:hover, .ytp-settings-button:hover, .ytp-fullscreen-button:hover, .ytp-subtitles-button:hover svg:style(transform: scale(1.03) !important;)

! move more video btn in fullscreen above progress bar
www.youtube.com##.ytp-fullscreen-grid-expand-button:style(transform:translateY(-40px) !important;)

youtube.com##.ytp-volume-icon[data-title-no-tooltip="Unmute"] svg path:style(fill:#FF6969!important;)

! scrubbing thumbnails above the progress bar
www.youtube.com##.ytp-fine-scrubbing-container:style(transform: translateY(-110px) !important;)

! when pausing, made the fat button in the middle way easier to look at lol
www.youtube.com##.ytp-bezel:style(transform:scale(.6) !important; background:none !important;)
www.youtube.com##.ytp-bezel-icon:style(filter: drop-shadow(0px 5px 30px #000);)

! controls stay visible while paused, I feel like this was like this before idr
www.youtube.com##.html5-video-player.paused-mode .ytp-chrome-bottom:style(opacity: 1 !important;)
www.youtube.com###movie_player:not(.html5-video-player.playing-mode)::after:style(opacity:1 !important;)

! settings menu touch up, personal touches, removed the scrolling, so the menu just extends as needed
www.youtube.com##.ytp-settings-menu:style(transform:scale(.85) translate(30px, 45px) !important; background: rgba(15,15,15,0.6) !important; backdrop-filter: blur(24px) saturate(110%) !important; -webkit-backdrop-filter: blur(18px) saturate(180%) !important; border-radius:2px !important;) 
www.youtube.com##.ytp-panel:style(overflow: visible !important; max-height: none !important;)
! theater button visible in fullscreen
youtube.com##.ytp-button[data-title-no-tooltip="Theater mode"],[data-title-no-tooltip="Default view"]:style(display: inline-block !important;)

! removing the fullscreen "more videos" grid, you can get rid of this if you want, but I dont know anyone who uses it lol
www.youtube.com##.ytp-fullscreen-grid:style(display:none!important;)
www.youtube.com##.ytp-fullscreen-grid-active:remove-class(ytp-fullscreen-grid-active)
www.youtube.com##.ytp-grid-scrolling:remove-class(ytp-grid-scrolling)
www.youtube.com##.ytp-fullscreen-grid-peeking:remove-class(ytp-fullscreen-grid-peeking)
www.youtube.com##.ytp-gradient-bottom
www.youtube.com##.ytp-grid-scrollable:remove-class(ytp-grid-scrollable)

! remove end cards
www.youtube.com##.ytp-endscreen-content


! Number of videos per row [change the "4" below to whatever you want]

www.youtube.com##.ytd-rich-grid-renderer:style(--ytd-rich-grid-items-per-row: 6 !important;)

! Remove empty spaces

youtube.com###contents.ytd-rich-grid-renderer > :not(ytd-rich-item-renderer, ytd-continuation-item-renderer)

youtube.com##ytd-rich-item-renderer[is-in-first-column]:style(margin-left: calc(var(--ytd-rich-grid-item-margin)/2) !important;)

youtube.com##ytd-ghost-grid-renderer

