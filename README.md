# honeydue-mono-repo

## Understanding the project structure of this monorepo

1. `component-one`, `component-two`, `component-three` are shared components that are used by the teams building out the APIs
2. `accounts-api` depends on `component-one`, `component-two` and `component-three`.  the `accounts-api` is exposed through the `web-frontend` only
![accounts](images/dependency-mapping-accounts.png)
3. `billing-api` depends on `component-one`, `component-two` and the `accounts-api`.  the `billing-api` is exposed through all of the frontends - `web-frontend`, `ios-native`, and `android-native`
![billing](images/dependency-mapping-billing.png)
4. `inventory-api` depends on `component-one`, `component-three`.  the `inventory-api` is exposed through all of the frontends - `web-frontend`, `ios-native`, and `android-native`
![inventory](images/dependency-mapping-inventory.png)
