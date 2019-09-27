---
title: 'Cycle-1 (Upload Service)'
date: 2019-02-11T19:27:37+10:00
weight: 4
summary: Explains minimum service configuration required to run only the album upload feature. This is used for onboarding new developers into this project
---


This app stores photo albums in cloud server.

### Build and Deploy Instructions
- [Deploy using docker compose](../docker-compose)

### Technical Details

Since all the processes are dockerized in this project, it makes more sense to treat each seperate process, while uploading and persisting a file, as a service.

All the files are stored directly to the file system. 

Services required for this functionality are

1. Front end - with upload button
2. Back end - that handles the http request and saves the file to disk
3. filesystem ui - a simple caddy server as reverse proxy

### Security and Previleges
**TODO**

### Architecture
{{< load-photoswipe >}}
{{< gallery >}}
  {{< figure src="https://placekitten.com/600/400" >}}
  {{< figure src="https://placekitten.com/1200/900" >}}
{{< /gallery >}}

**TODO**

### Testing

Run the album upload test

```
make upload-test-album [path-to-album]
```

After upload goto http://localhost:2015/album-uploads/test-album/uploads

### Metrics
**TODO**

### To Be implemented yet!
- [ ] Make frontend as https.
- [ ] Add authentication.


