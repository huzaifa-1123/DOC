# GITHUB WORKFLOW

### Dev Deployment

- pull `dev` to `my_branch`
- fix conflict
- test application run or build
- fix any error caused by merge
- push to `my_branch`
- create PR to `dev` branch from browser. in browser PR create page `base:dev` and `compare:my_branch` thne `Create Pull Request`
- refresh page see anymore confilict remain
- `Squash and Merge`
- Check action ran successfully

### Prod Deployment

- pull `dev` to `main`
- fix conflicts
- test application run or build
- fix any error caused by merge
- push to `dev`
- create PR to `main` branch from browser. in browser PR create page `base:main` and `compare:dev` thne `Create Pull Request`
- refresh page see anymore confilict remain
- `Squash and Merge`
- Check action ran successfully
- Enter prod server
- Enter repo directory inside server
- TAG={Github Action Main Run Number} docker compose pull && TAG={Github Action Main Run Number} docker compose up -d