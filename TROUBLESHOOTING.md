# Troubleshooting Guide

## CSS Not Loading (404 Error)

If you see `Failed to load resource: style.css:1 404` in browser console:

### Solution 1: Restart Jekyll Server
```bash
# If using Docker:
docker-compose down
docker-compose up

# If using local Jekyll:
# Press Ctrl+C to stop
bundle exec jekyll serve
```

### Solution 2: Clear Jekyll Cache
```bash
# Stop the server, then:
rm -rf _site .jekyll-cache .jekyll-metadata

# Restart server:
docker-compose up
# OR
bundle exec jekyll serve
```

### Solution 3: Check Browser Console
1. Open browser DevTools (F12)
2. Check Console tab for the exact URL it's trying to load
3. Should be: `http://localhost:4000/assets/css/style.css`
4. If it's missing `/assets/`, check `_config.yml` baseurl setting

### Solution 4: Force Rebuild
If using Docker:
```bash
docker-compose down
docker-compose up --build --force-recreate
```

### Solution 5: Verify File Permissions
```bash
ls -la assets/css/style.css
# Should show read permissions (r)
```

## Other Common Issues

### Port 4000 Already in Use
```bash
# Find and kill the process:
lsof -ti:4000 | xargs kill -9
# OR on Windows:
netstat -ano | findstr :4000
taskkill /PID [PID_NUMBER] /F
```

### Docker Not Starting
- Ensure Docker Desktop is running
- Check Docker Desktop → Settings → Resources
- Try: `docker-compose down && docker-compose up`
