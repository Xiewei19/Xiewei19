/**

脚本名称: #小程序://题材库/XW

解锁会员



[rewrite_local]


^https:\/\/miniapp\.guniuniu\.com\/api\/mini-app\/user$ url script-response-body https://raw.githubusercontent.com/Yu9191/Rewrite/main/ticaiku.js

[mitm] 

hostname = miniapp.guniuniu.com



*/




    let obj = JSON.parse($response.body);
    
    // 不能删
    obj.data.nickName = "我是股神";  

    obj.data.vipTime = "2099-09-09 02:20:13";                 

    $done({
        body: JSON.stringify(obj)
    });
