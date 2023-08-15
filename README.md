# Flutter Assignment
This assignment is to embed video vimeo in mobile app.

## What will you do in the assignment.

1. Get video id from video url.
   
   eg. video link is https://vimeo.com/847282750 then video id will be **847282750**

2. Send request to vimeo api.
   
   https://api.vimeo.com/videos/{video_id}?fields=play with GET http verb
   
   eg. https://api.vimeo.com/videos/847282750?fields=play
   
   Headers will be
   
   **Authorization:** 	Bearer e76cd91ebcd375276979cbca386d6c4a
   
   **Accept:**	 application/vnd.vimeo.*+json;version=3.4

3. You will get the following response from vimeo
   ```
   {
    "play": {
        "progressive": [
            {
                "type": "video/mp4",
                "codec": "H264",
                "width": 960,
                "height": 540,
                "link_expiration_time": "2023-08-16T07:18:23+00:00",
                "link": "https://player.vimeo.com/progressive_redirect/playback/847282750/container/72b9d23b-e2cf-4692-aeb7-5be06b96567f/43112588-13aaf5fc?expires=1692170303&loc=external&log_user=0&oauth2_token_id=1733496662&signature=58f80c68371b248f4002d73b04b185e3c882ae5014d48fc227f8799105d69dfa",
                "created_time": "2023-07-21T10:45:17+00:00",
                "fps": 30,
                "size": 156491581,
                "md5": null,
                "rendition": "540p"
            },
            {
                "type": "video/mp4",
                "codec": "H264",
                "width": 1280,
                "height": 720,
                "link_expiration_time": "2023-08-16T07:18:23+00:00",
                "link": "https://player.vimeo.com/progressive_redirect/playback/847282750/container/72b9d23b-e2cf-4692-aeb7-5be06b96567f/51984f48-13aaf5fc?expires=1692170303&loc=external&log_user=0&oauth2_token_id=1733496662&signature=bad05eec89b1a59cd5e81ea7d1c9d86c38a9ef71a78a8a7114b5bba516074ad6",
                "created_time": "2023-07-21T10:44:59+00:00",
                "fps": 30,
                "size": 235417591,
                "md5": null,
                "rendition": "720p"
            },
            {
                "type": "video/mp4",
                "codec": "H264",
                "width": 426,
                "height": 240,
                "link_expiration_time": "2023-08-16T07:18:23+00:00",
                "link": "https://player.vimeo.com/progressive_redirect/playback/847282750/container/72b9d23b-e2cf-4692-aeb7-5be06b96567f/580e987e-13aaf5fc?expires=1692170303&loc=external&log_user=0&oauth2_token_id=1733496662&signature=310bf9e596ff44011ba5fb8450b88a9302ebfa528fad1762171f527fa4ab7942",
                "created_time": "2023-07-21T10:43:26+00:00",
                "fps": 30,
                "size": 47049945,
                "md5": null,
                "rendition": "240p"
            },
            {
                "type": "video/mp4",
                "codec": "H264",
                "width": 640,
                "height": 360,
                "link_expiration_time": "2023-08-16T07:18:23+00:00",
                "link": "https://player.vimeo.com/progressive_redirect/playback/847282750/container/72b9d23b-e2cf-4692-aeb7-5be06b96567f/a32892ac-13aaf5fc?expires=1692170303&loc=external&log_user=0&oauth2_token_id=1733496662&signature=7e43e803e1ea7583a020b7970c14fdb5e0bfc09ac8b17b155d331a516b905c4b",
                "created_time": "2023-07-21T10:44:06+00:00",
                "fps": 30,
                "size": 84588337,
                "md5": null,
                "rendition": "360p"
            }
        ],
        "hls": {
            "link_expiration_time": "2023-08-16T07:17:47+00:00",
            "link": "https://player.vimeo.com/play/72b9d23b-e2cf-4692-aeb7-5be06b96567f/hls.m3u8?s=847282750_1692170267_dc2de2b14563ed0bd54df2976d552ee1&context=Vimeo%5CController%5CApi%5CResources%5CVideoController.&log_user=0&oauth2_token_id=1733496662"
        },
        "dash": {
            "link_expiration_time": "2023-08-16T07:17:47+00:00",
            "link": "https://player.vimeo.com/play/72b9d23b-e2cf-4692-aeb7-5be06b96567f/dash.mpd?s=847282750_1692170267_dc2de2b14563ed0bd54df2976d552ee1&context=Vimeo%5CController%5CApi%5CResources%5CVideoController.&log_user=0&oauth2_token_id=1733496662"
        },
        "status": "playable"
    }
   }

4. Get the video link for **hls** format.
5. Embed in any hls video player available on internet.

## How will you submit the assignment.
1. Clone this repo.
2. Create a branch from **main**
3. Push your code and create a PR to **main** branch.

## References
- https://developer.vimeo.com/api/authentication
- https://developer.vimeo.com/api/files/video-links
- https://flutterawesome.com/yoyo-video-player-a-hls-m3u8-video-player-for-flutter/
- https://pub.dev/packages/video_player_web_hls
