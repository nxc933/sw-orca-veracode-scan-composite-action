# Orca Veracode Scan Composite Action  

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
