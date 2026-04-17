# POCKET ID - IdentifyProvider

--- 

## How to use

### 1. Clone repo
```
git clone git@github.com:Gu35t09/IdentifyProvider.git
cd IdentityProvider
```

### 2. TRAEFIK - Configure environment variables
```
cd traefik
# Create a copy of the example env file
cp .env_example .env
# Fill the variable with the correct values
nano .env
```

### 3. TRAEFIK - Configure traefik.yml
```
# Change the e-mail address to the correct let's encrypt one
nano data/traeik.yaml
```

### 4. TRAEFIK -  Start container
```
docker compose up -d
```

### 5. TRAEFIK - Check status 
```
docker compose logs -f
```

### 6. POCKET ID - Configure environment variables
```
cd ../pocketid
# Create a copy of the example env file
cp .env_example .env
# Fill the variable with the correct values
nano .env
```

### 7. POCKET ID - Configure docker compose and webfinger
```
# Change traefik route id.greyroom.net and greyroom.net with the desired FQDN
nano docker-compose.yaml
# Create a copy of the example webfinger file
cp webfinger-data/.well-known/webfinger.example webfinger-data/.well-known/webfinger
# Fill the webfinger file with the e-mail of the future pocket id account and the FQDN of the pocket id instance
nano webfinger-data/.well-known/webfinger
```

### 8. Start pocket id
```
docker compose up -d
```

### 9. Check status 
```
docker compose logs -f
```

### 10. Start using pocket id
```
# Go to https://id.yourdomain.com/set and register the first account
```
