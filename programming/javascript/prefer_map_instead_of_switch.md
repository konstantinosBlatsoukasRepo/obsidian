example with switch:

```javascript
switch (fmService.qualityType) {
	case 'ncr':
		fileDownloadApiTemplate = lodash.template('api/non-conformances/download-file/<%= jcrUUID %>');
        break;

    case 'rca':
        fileDownloadApiTemplate = lodash.template('api/root-cause-analysis/download-file/<%= jcrUUID %>');
		break;

    case 'capa':
          fileDownloadApiTemplate = lodash.template('api/corrective-actions/download-file/<%= jcrUUID %>');
        break;
      }
```

example with map:

```javascript
let urlMap = {
	'capa': 'corrective-actions',
    'ncr': 'non-conformances',
    'rca': 'root-cause-analysis'
 };

let fileDownloadApiTemplate = lodash.template(`api/${urlMap[fmService.qualityType]}/download-file/<%= jcrUUID %>`);
```