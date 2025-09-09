

### Issue 1: Build command missing in the workflow
      name: Build Python package
      run: python -m build


### Issue 2: Project name needs to be passed
    name = "example_package"


### Issue 3: Project version needs to be passed
     version = "0.0.1"

### Issue 4: cloudsmith: command not found
      name: Install Cloudsmith CLI and authenticate with OIDC
      uses: cloudsmith-io/cloudsmith-cli-action@v1.0.3

### Issue 5: OIDC configuration needs to be passed
    with: oidc-namespace: ${{ env.CLOUDSMITH_NAMESPACE }} 
    oidc-service-slug: ${{ env.CLOUDSMITH_SERVICE_SLUG }}

### Issue 6: Incorrect repository names
    env: 
     CLOUDSMITH_STAGING_REPO: 'staging' 
     CLOUDSMITH_PRODUCTION_REPO: 'production'
