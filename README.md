# Orca Veracode Scan Composite Action  

In order to use this action, please work in concert with the Application Security team by visiting this [link](https://swcompany.sharepoint.com/sites/SPApplicationSecurity/SitePages/Assurance.aspx?OR=Teams-HL&CT=1642620247402&sourceId=&params=%7B%22AppName%22%3A%22Teams-Desktop%22%2C%22AppVersion%22%3A%2228%2F21110108720%22%7D#q-i-d-like-to-use-the-github-composite-action-to-kick-off-security-scans%2C-what-do-i-need-to-do-that)

### Parameters
Name | Type |   | Default | Note |
|--- | ---- |---| ------- | ---- |
`artifact_path` | String | Required* | `${{ github.workspace }}`
`artifact_name` | String | Required* | 
`config_id` | Integer | Required* | 
`orca_api_key` | Secret | Required* | 
`orca_url` | String | *Optional* | `https://orca.sherwin.com` | 
`request_timeout` | Integer | *Optional* | `20000` | 

### Response
| Variable |  Description  |
|---|---|
`response` | Response as JSON String

Usage:

```yaml
 - uses: sherwin-williams-co/sw-orca-veracode-scan-composite-action@main
   with:
     artifact_path: '${{ github.workspace }}'
     artifact_name: 'HelloWorld.jar'
     config_id: 46
     orca_api_key: '${{ secrets.BEARER_TOKEN }}'
     # Optional
     # orca_url: 'https://orca.sherwin.com'
     # request_timeout: '20000'
     
```
