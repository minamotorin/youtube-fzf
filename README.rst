README Version 1.5

.. contents::

Abstract
########

Browse YouTube in CLI with fzf without YouTube Data API.

NOTE
####

I'm beginner. This program will not work if YouTube changes things. And it will take long time to push fix.

Some codes and English will wrong. If you find something, please use `Github issues <https://github.com/minamotorin/youtube-fzf/issues>`_ feel free.

Usage
#####

  :About:
    :youtube-fzf:
      Browse YouTube in CLI with fzf without YouTube Data API.
    :Repository:
      https://github.com/minamotorin/youtube-fzf
    :License:
      `GNU General Public Lisence 3 <https://www.gnu.org/licenses/gpl-3.0.html>`_
    :Subscribed channels database:
      value of YOUTUBE_FZF_DATABASE environmental valuables
    
  :mode:
    :youtube-fzf:
      Read from subscribed channels database
    :youtube-fzf [OPTIONS]:
      Womk with option

  :Options:
    --videos URL			Channel's videos
    --lives URL			Channel's stream archives
    --shorts URL			Channel's shorts
    --channels URL		Channel's urls
    --watch URL			Video's information
    --comments URS		Video's comments (depend on youtube-comment-downloader)
    -v, --fzf-videos HEADER	fzf mode for list of video's url
    -c, --fzf-channels HEADER	fzf mode for list of channel's url
    -q, --query WORDS		Search videos from words
    -s, --search WORDS		Search videos from words and select in fzf mode
    -V, --version			Show version information
    -h, --help			Show this help
  
  :fzf:
    :Ctrl-t:
      Toggle-preview
    :Ctrl-y:
      Yank (work on only macOS now)
    :Up:
      Page-up
    :Down:
      Page-down
      
    Run \`man fzf' and get more informations.

  :fzf-videos:
    :Ctrl-o:
      Other videos
    :Ctrl-s:
      Show comments
    :Ctrl-u:
      Uploader information
    :Ctrl-w:
      Watch video with mpv

  :fzf-channels:
    :Ctrl-o:
      Open channel
    :Ctrl-s:
      Suggested channels

TODO
  More informations

Environmental variables
***********************

:``YOUTUBE_FZF_DATABASE``:
  Subscribed channels database. The default is ``/dev/stdin``.

:``YOUTUBE_FZF_TMP``:
  For debugging, temporary files are created in ``$YOUTUBE_FZF_TMP``.
  In default, temporary directory is created by ``mktemp``.

:``YOUTUBE_FZF_VIDEOS``:
  Custom fzf options for fzf-videos. Overwrites default key bindings.

:``YOUTUBE_FZF_CHANNELS``:
  Custom fzf options for fzf-channels. Overwrites default key bindings.

:``YOUTUBE_FZF_LANG``:
  Languages information for query. Support is still incomplete.

Dependencies
############

Must
****

:Bourne Shell:
  ``/bin/sh``

:`curl <https\://curl.se/>`_:
  For fetch YouTube API

:`fzf\: 🌸 A command-line fuzzy finder <https\://github.com/junegunn/fzf>`_:
  For filter results of videos or channels

:`jq\: Command-line JSON processor <https\://stedolan.github.io/jq/>`_:
  For parse JSON file from YouTube API

Options
*******

:`mpv\: 🎥 Command line video player <https\://mpv.io/>`_:
  For play YouTube videos

:`youtube-dl\: Command-line program to download videos from YouTube.com and other video sites <https\://youtube-dl.org/>`_:
  For play YouTube videos with mpv

:`youtube-comment-downloader\: Simple script for downloading Youtube comments without using the Youtube API <https\://github.com/egbertbouman/youtube-comment-downloader>`_:
  For watch comments

Q&A
###

:Why don't you use YouTube Data API?:
  Because of freedom. Use it if you want.

Reference
#########

:`fzf\: 🌸 A command-line fuzzy finder <https\://github.com/junegunn/fzf>`_:
  Default key bindings of fzf mode

Similar projects
################

Shell Script
************

:`ytfzf <https\://github.com/pystardust/ytfzf>`_:
  Good! Thumbnails, History, and some features will be useful. However, it seems that this script is not able to get videos from channels.

:`yt <https\://github.com/sayan01/scripts/blob/master/yt>`_:
  Require GNU grep but jqless. Not only channel's videos but also playlists. I haven't understood how to use.

If you know other similar projects, please let's me know.

TODO
####

- More detailed README

  - Description or Background
  - Screenshots
  - Examples
  - Knowledge issues
  - More Q&A
  - More Reference
  - More Similar Projects (other than shell scripts)
  - More TODO

- Watch videos without youtube-dl
- Better languages support
- Use variables with ``--data-raw``
- Exit codes
- Autocomplete
- Support yt-dlp
- Create test
- Automatically Usage update
- Make logo image
- Yank in multi-platform
- More options
- More search results
- Info of deleted videos
- Support URL in description
- Playlist support
- Channel information
- Custom search options
- Better User Agent
- Use shell script instead of youtube-comment-downloader (and jq)

  - (Is there any shell script alternative of fzf?)

Issue
#####

If you find something, report bugs, or have any requests, questions, suggestations, opnions, or feedbacks, please use `Github issues <https://github.com/minamotorin/youtube-fzf/issues>`_ feel free.

License
#######

This project is under the `GNU General Public License Version 3 <https://www.gnu.org/licenses/gpl-3.0.html>`_.
