<!-- default badges list -->
![](https://img.shields.io/endpoint?url=https://codecentral.devexpress.com/api/v1/VersionRange/128535892/13.1.4%2B)
[![](https://img.shields.io/badge/Open_in_DevExpress_Support_Center-FF7200?style=flat-square&logo=DevExpress&logoColor=white)](https://supportcenter.devexpress.com/ticket/details/E3937)
[![](https://img.shields.io/badge/📖_How_to_use_DevExpress_Examples-e9f6fc?style=flat-square)](https://docs.devexpress.com/GeneralInformation/403183)
<!-- default badges end -->
<!-- default file list -->
*Files to look at*:

* [Default.aspx](./CS/WebSite/Default.aspx) (VB: [Default.aspx](./VB/WebSite/Default.aspx))
<!-- default file list end -->
# ASPxGridView - How to specify HeaderCaptionTemplate and prevent the default mouse actions
<!-- run online -->
**[[Run Online]](https://codecentral.devexpress.com/e3937/)**
<!-- run online end -->


<p>This example demonstrates how to define some control inside a header caption template and prevent a default action for the specified events.<br />
</p><p>1) Define any control in <a href="http://documentation.devexpress.com/#AspNet/DevExpressWebASPxGridViewGridViewColumn_HeaderCaptionTemplatetopic"><u>GridViewColumn.HeaderCaptionTemplate</u></a> and wrap it with a div tag/container;<br />
2) Handle the div client-side<strong> onmousedown</strong> and <strong>onmouseup</strong> events and prevent the default action (column sorting) via the client-side <a href="http://documentation.devexpress.com/#AspNet/DevExpressWebASPxClassesScriptsASPxClientUtils_PreventEventAndBubbletopic"><u>ASPxClientUtils.PreventEventAndBubble</u></a> method.</p>

<br/>


