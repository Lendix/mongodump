# mongoS3

⚠️ This package is no longer maintained, you should use an alternative solution for your backups ⚠️

Simply dump a Mongo DB, then stream everything to AWS S3, promise flavoured

## Usage

```es6
const mongoS3 = require('mongo-s3');

mongoS3({
  log: console.log,
  uri: process.env.MONGO_URI,
  s3: {
      accessKeyId: process.env.AWS_ACCESS_KEY_ID,
      secretAccessKey: process.env.AWS_SECRET_ACCESS_KEY,
      bucket: process.env.AWS_S3_DUMP_BUCKET,
      key: process.env.AWS_S3_DUMP_KEY
  }
}).then(function (result) { console.log('EVERYTHING SHOULD BE OK') })
  .catch(function (err) { console.error('Snap, something went wrong :(') });
```
