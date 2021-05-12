## OVERVIEW

POC to test the Cluster API on NodeJS

### SETUP

```
nvm use
npm install
```

### RUN 

Run the app in a single process:

```
npm run start:single-process
```

Test it:

```
npx loadtest http://localhost:3000/api/50 -n 1000 -c 100
npx loadtest http://localhost:3000/api/50000000 -n 1000 -c 100
```

Run the app with multi processes:

```
npm run start:multi-process
```

Test it:

```
npx loadtest http://localhost:4000/api/50 -n 1000 -c 100
npx loadtest http://localhost:4000/api/50000000 -n 1000 -c 100
```

Compare the results!