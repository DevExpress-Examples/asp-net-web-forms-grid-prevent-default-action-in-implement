<!-- default badges list -->
![](https://img.shields.io/endpoint?url=https://codecentral.devexpress.com/api/v1/VersionRange/128535892/13.1.4%2B)
[![](https://img.shields.io/badge/Open_in_DevExpress_Support_Center-FF7200?style=flat-square&logo=DevExpress&logoColor=white)](https://supportcenter.devexpress.com/ticket/details/E3937)
[![](https://img.shields.io/badge/📖_How_to_use_DevExpress_Examples-e9f6fc?style=flat-square)](https://docs.devexpress.com/GeneralInformation/403183)
<!-- default badges end -->

# Grid View for ASP.NET Web Forms - How to specify HeaderCaptionTemplate and prevent the default mouse actions

This example demonstrates how to add a control in a column header and prevent a default action for the specified events.
  
1. Define a control in [GridViewColumn.HeaderCaptionTemplate](https://docs.devexpress.com/AspNet/DevExpress.Web.GridViewColumn.HeaderCaptionTemplate) and wrap it with a `div` tag.
   
    ```aspx
    <HeaderCaptionTemplate>
        <div onmousedown="return CancelEvent(event)" onmouseup="return CancelEvent(event)">
            <dx:ASPxComboBox ID="cmb" runat="server" DataSourceID="dsCmb" ValueType="System.String"
                TextField="CategoryName" ValueField="CategoryID">
                <ClientSideEvents SelectedIndexChanged="OnSelectedIndexChanged" />
            </dx:ASPxComboBox>
        </div>
    </HeaderCaptionTemplate>
    ```

3. Handle the div client-side `onmousedown` and `onmouseup` events and prevent the default action (column sorting) via the client-side [ASPxClientUtils.PreventEventAndBubble](https://docs.devexpress.com/AspNet/js-ASPxClientUtils.PreventEventAndBubble.static(htmlEvent)) method.
   
    ```jscript
    function CancelEvent(evt) {
        return ASPxClientUtils.PreventEventAndBubble(evt);
    }
    ```

## Files to Review

* [Default.aspx](./CS/WebSite/Default.aspx) (VB: [Default.aspx](./VB/WebSite/Default.aspx))
