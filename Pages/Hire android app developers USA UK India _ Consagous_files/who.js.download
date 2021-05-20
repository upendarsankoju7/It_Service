var whoistrack_obj = function ()
{
    this.wait = function (accNo)
    {
        if (document.body != null)
        {
            whoistrack.immediate(accNo);
            return;
        };
        window.setTimeout(function ()
        {
            whoistrack.wait(accNo);
        }, 100);
    }

    this.immediate = function (accNo)
    {
        try
        {
            var r = encodeURIComponent(document.referrer.replace(/<\/?[^>]+(>|$)/g, ""));
            var w = screen.width;
            var h = screen.height;
            var i = document.createElement("img");
            var u = window.location.href;
            var p = u.split("/")[0];
            i.src = p + "//dashboard.whoisvisiting.com/who.ashx?Type=Hit&Data=" + w + "|" + h + "|" + r + "|" + accNo + "|" + encodeURIComponent(u.replace(/<\/?[^>]+(>|$)/g, ""));
            i.style.display = "none";
            document.body.appendChild(i);
        }
        catch (e)
        {
        }
    }
};
var whoistrack = new whoistrack_obj();
var whoistrack_params = whoistrack_params || [];
for (var i = 0; i < whoistrack_params.length; i++)
{
    switch (whoistrack_params[i][0])
    {
    case "immediate":
        whoistrack.immediate(whoistrack_params[i][1]);
        break;
    case "wait":
        whoistrack.wait(whoistrack_params[i][1]);
        break;
    }
}