<!doctype html>
<html>
<head>
    <link href="https://fonts.googleapis.com/css?family=Bahnschrift&display=swap" rel="stylesheet" />
</head>
<body>
    <div class="v31_2">
        <div class="v31_3">
        </div>
        <div class="v31_4">
        </div>
        <div class="v31_12">
            <div class="v31_13">
                <div class="name">
                </div>
                <div class="name">
                </div>
                <div class="name">
                </div>
            </div>
            <span class="v31_17">AUTOMATE YOUR WORK FLOW OF CREATING PLAYLISTS. </span>
        </div>
        <div class="v31_7">
            <div class="name">
            </div>
            <div class="name">
            </div>
            <div class="name">
            </div>
        </div>
        <div class="v31_18">
            <div class="v31_19">
            </div>
            <span class="v31_20">START NOW</span>
        </div>
    </div>
</body>
</html>
<br />
<br />
<style>
    * {
        box-sizing: border-box;
    }

    body {
        font-size: 14px;
    }

    .v31_2 {
        width: 100%;
        height: 1080px;
        background: rgba(255,255,255,1);
        opacity: 1;
        position: relative;
        top: 0px;
        left: 0px;
        overflow: hidden;
    }

    .v31_3 {
        width: 100%;
        height: 100%;
        background: rgba(0,0,0,1);
        opacity: 1;
        position: relative;
        top: 0px;
        left: 0px;
        overflow: hidden;
    }

    .v31_4 {
        width: 214px;
        height: 119px;
        background: url("../images/v31_4.png");
        background-repeat: no-repeat;
        background-position: center center;
        background-size: cover;
        opacity: 1;
        position: absolute;
        top: 22px;
        left: 645px;
        overflow: hidden;
    }

    .v31_12 {
        width: 100%;
        height: 462px;
        background: url("../images/v31_12.png");
        background-repeat: no-repeat;
        background-position: center center;
        background-size: cover;
        opacity: 1;
        position: absolute;
        top: 209px;
        left: 84px;
        overflow: hidden;
    }

    .v31_13 {
        width: 775px;
        height: 308px;
        background: url("../images/v31_13.png");
        background-repeat: no-repeat;
        background-position: center center;
        background-size: cover;
        opacity: 1;
        position: absolute;
        top: 132px;
        left: 0px;
        overflow: hidden;
    }

    .name {
        color: #fff;
    }

    .name {
        color: #fff;
    }

    .name {
        color: #fff;
    }

    .v31_17 {
        width: 100%;
        color: rgba(255,255,255,1);
        position: absolute;
        top: 0px;
        left: 3px;
        font-family: Bahnschrift;
        font-weight: Condensed;
        font-size: 128px;
        opacity: 1;
        text-align: left;
    }

    .v31_7 {
        width: 30px;
        height: 20px;
        background: url("../images/v31_7.png");
        background-repeat: no-repeat;
        background-position: center center;
        background-size: cover;
        opacity: 1;
        position: absolute;
        top: 20px;
        left: 20px;
        overflow: hidden;
    }

    .name {
        color: #fff;
    }

    .name {
        color: #fff;
    }

    .name {
        color: #fff;
    }

    .v31_18 {
        width: 270px;
        height: 81px;
        background: url("../images/v31_18.png");
        background-repeat: no-repeat;
        background-position: center center;
        background-size: cover;
        opacity: 1;
        position: absolute;
        top: 912px;
        left: 617px;
        overflow: hidden;
    }

    .v31_19 {
        width: 270px;
        height: 80px;
        background: rgba(0,0,0,0);
        opacity: 1;
        position: absolute;
        top: 1px;
        left: 0px;
        border: 5px solid rgba(255,255,255,1);
        overflow: hidden;
    }

    .v31_20 {
        width: 234px;
        color: rgba(255,255,255,1);
        position: absolute;
        top: 0px;
        left: 18px;
        font-family: Bahnschrift;
        font-weight: Condensed;
        font-size: 64px;
        opacity: 1;
        text-align: left;
    }
</style>

<title>Example of the Authorization Code flow with Spotify</title>
<link rel="stylesheet" href="//netdna.bootstrapcdn.com/bootstrap/3.1.1/css/bootstrap.min.css">
<style type="text/css">
    #login, #loggedin {
        display: none;
    }

    .text-overflow {
        overflow: hidden;
        text-overflow: ellipsis;
        white-space: nowrap;
        width: 500px;
    }
</style>
</head>

<body>
    <div class="container">
        <div id="login">
            <h1>This is an example of the Authorization Code flow</h1>
            <a href="/login" class="btn btn-primary">Log in with Spotify</a>
        </div>
        <div id="loggedin">
            <div id="user-profile">
            </div>
            <div id="oauth">
            </div>
            <button class="btn btn-default" id="obtain-new-token">Obtain new token using the refresh token</button>
        </div>
    </div>

    <script id="user-profile-template" type="text/x-handlebars-template">
        <h1>Logged in as {{display_name}}</h1>
        <div class="media">
            <div class="pull-left">
                <img class="media-object" width="150" src="{{images.0.url}}" />
            </div>
            <div class="media-body">
                <dl class="dl-horizontal">
                    <dt>Display name</dt>
                    <dd class="clearfix">{{display_name}}</dd>
                    <dt>Id</dt>
                    <dd>{{id}}</dd>
                    <dt>Email</dt>
                    <dd>{{email}}</dd>
                    <dt>Spotify URI</dt>
                    <dd><a href="{{external_urls.spotify}}">{{external_urls.spotify}}</a></dd>
                    <dt>Link</dt>
                    <dd><a href="{{href}}">{{href}}</a></dd>
                    <dt>Profile Image</dt>
                    <dd class="clearfix"><a href="{{images.0.url}}">{{images.0.url}}</a></dd>
                    <dt>Country</dt>
                    <dd>{{country}}</dd>
                </dl>
            </div>
        </div>
    </script>

    <script id="oauth-template" type="text/x-handlebars-template">
        <h2>oAuth info</h2>
        <dl class="dl-horizontal">
            <dt>Access token</dt>
            <dd class="text-overflow">{{access_token}}</dd>
            <dt>Refresh token</dt>
            <dd class="text-overflow">{{refresh_token}}</dd>
        </dl>
    </script>

    <script src="//cdnjs.cloudflare.com/ajax/libs/handlebars.js/2.0.0-alpha.1/handlebars.min.js"></script>
    <script src="http://code.jquery.com/jquery-1.10.1.min.js"></script>
    <script>
        (function () {

            /**
             * Obtains parameters from the hash of the URL
             * @return Object
             */
            function getHashParams() {
                var hashParams = {};
                var e, r = /([^&;=]+)=?([^&;]*)/g,
                    q = window.location.hash.substring(1);
                while (e = r.exec(q)) {
                    hashParams[e[1]] = decodeURIComponent(e[2]);
                }
                return hashParams;
            }

            var userProfileSource = document.getElementById('user-profile-template').innerHTML,
                userProfileTemplate = Handlebars.compile(userProfileSource),
                userProfilePlaceholder = document.getElementById('user-profile');

            var oauthSource = document.getElementById('oauth-template').innerHTML,
                oauthTemplate = Handlebars.compile(oauthSource),
                oauthPlaceholder = document.getElementById('oauth');

            var params = getHashParams();

            var access_token = params.access_token,
                refresh_token = params.refresh_token,
                error = params.error;

            if (error) {
                alert('There was an error during the authentication');
            } else {
                if (access_token) {
                    // render oauth info
                    oauthPlaceholder.innerHTML = oauthTemplate({
                        access_token: access_token,
                        refresh_token: refresh_token
                    });

                    $.ajax({
                        url: 'https://api.spotify.com/v1/me',
                        headers: {
                            'Authorization': 'Bearer ' + access_token
                        },
                        success: function (response) {
                            userProfilePlaceholder.innerHTML = userProfileTemplate(response);

                            $('#login').hide();
                            $('#loggedin').show();
                        }
                    });
                } else {
                    // render initial screen
                    $('#login').show();
                    $('#loggedin').hide();
                }

                document.getElementById('obtain-new-token').addEventListener('click', function () {
                    $.ajax({
                        url: '/refresh_token',
                        data: {
                            'refresh_token': refresh_token
                        }
                    }).done(function (data) {
                        access_token = data.access_token;
                        oauthPlaceholder.innerHTML = oauthTemplate({
                            access_token: access_token,
                            refresh_token: refresh_token
                        });
                    });
                }, false);
            }
        })();
    </script>
</body>
</html>
