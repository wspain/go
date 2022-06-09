hostname = ap?.bilibili.com, testflight.apple.com, ems.youku.com, optimus-ads.amap.com, ma-adx.ctrip.com, m.ctrip.com, weixin110.qq.com, *.baidu.com, api.bilibili.com, biz.caiyunapp.com

# 哔哩哔哩(By srk24)
^https?:\/\/app\.bilibili\.com\/x\/v\d\/splash\/list url script-response-body https://github.com/srk24/profile/raw/master/js/bilibili_splash.js
# hostname = ap?.bilibili.com

#TestFlight(By NobyDa)
^https?:\/\/testflight\.apple\.com\/v\d\/accounts\/.+?\/install$ url script-request-body https://gist.githubusercontent.com/NobyDa/9be418b93afc5e9c8a8f4d28ae403cf2/raw/TF_Download.js
# hostname = testflight.apple.com

# 高德地图广告
^http:\/\/ems\.youku\.com\/imp\? url reject
^http:\/\/optimus-ads\.amap\.com\/uploadimg\/.+ url reject
# hostname = ems.youku.com, optimus-ads.amap.com

# 携程广告
^https:\/\/ma-adx\.ctrip\.com\/_ma\.gif url reject
^https:\/\/m\.ctrip\.com\/restapi\/.+\/json\/tripAds url reject
^https:\/\/m\.ctrip\.com\/html5\/webresource\/js\/iscroll\.js$ url reject
# hostname = ma-adx.ctrip.com, m.ctrip.com

# 微信
^https?:\/\/weixin110\.qq\.com\/cgi-bin\/mmspamsupport-bin\/newredirectconfirmcgi url script-response-body https://github.com/HotKids/Rules/raw/master/Script/weixin110.js
# hostname = weixin110.qq.com

# 百度跳转 Fokit 15
^https?:\/\/(?!d\.pcs).*(?<!map)\.baidu\.com url request-header (\r\n)User-Agent:.+iPhone.+(\r\n) request-header $1User-Agent: Mozilla/5.0 (iPhone; CPU iPhone OS 15_1 like Mac OS X) AppleWebKit/605.1.15 (KHTML, like Gecko) Version/15.1 Mobile/15E148 Safari/16C50 Quark/604.1 T7/10.3 SearchCraft/2.6.3 (Baidu; P1 8.0.0)$2

# 百度网盘 解锁倍率/清晰度
https:\/\/pan\.baidu\.com\/rest\/\d\.\d\/membership\/user url script-response-body https://github.com/NobyDa/Script/raw/master/Surge/JS/BaiduCloud.js
# hostname = *.baidu.com

# Bilibili 番剧 1080p+
https:\/\/ap(p|i)\.bilibili\.com\/((pgc\/player\/api\/playurl)|(x\/v2\/account\/myinfo\?)|(x\/v2\/account/mine\?)) url script-response-body https://github.com/Sunert/Script/raw/master/Script/Bilibili/BiliHD.js
# hostname = api.bilibili.com
