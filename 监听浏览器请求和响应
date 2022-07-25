var originOpen = XMLHttpRequest.prototype.open;
var originSend = XMLHttpRequest.prototype.send;

// 监听请求响应
XMLHttpRequest.prototype.open = function() {
    this.addEventListener('load', function(obj) {
        var url = obj.target.responseURL;
        console.log(this.response)
    });
    originOpen.apply(this, arguments);
};

// 请求发送前切面
XMLHttpRequest.prototype.send = function() {
    // arguments 请求参数,可以在发送请求前修改参数
    originSend.apply(this, arguments);
};
