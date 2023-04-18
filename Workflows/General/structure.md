# General Structure

## Backend
Our backend works with node.js/express/mongodb stack. Mongodb databse is based on Mongodb Atlas Cloud Database, therefore its link is needed when deploying the backend. We used the service architecture, which means we have:
- Routes
- Middlewares

Also, since we wanted to use mongoose, we have implemented Model-View-Controller architecture, therefore, the backend works with **Models**.

In the backend, we use several packages to reach our aim. The most important packages and services we use are:
- Express
- Alchemy
- ipfs-only-hash
- Axios
- Cloudinary
- Mongoose
- jsonwebtoken
- uuid

## Mobile 
Our mobile application is written with Flutter. It has atomic-design architecture (mostly), which means we have divided our components into four groups:
- atoms
- molecules
- organisms
- pages

Also, to simplfy login processes, we have used Provider Structures.

While we are developing, we used following packages and services to reach our aim:
- WalletConnect
- Alchemy
- urllauncher
- qrcodescanner