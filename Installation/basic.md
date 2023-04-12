# Basic Installation

## Prerequisites
Prerequisites of basic installation parts are:
- Node.js with CLI
- Flutter
- Android Emulator

## Deploying Backend on Your Local
If you are not going to use our backend services that are deployed on online, you may want to look at this part. Other than that, you can skip into mobile part.

After installing node.js, go to project's root folder that you are cloned from GitHub. 

After that, in command line, run: 
```
npm install
```

Now, we have installed our dependencies, therefore we can run the backend. However, if you are getting any errors, you may want to install packages that throws the error by:
```
npm install --global {PACKAGE_NAME}
```

After that, create a file named .env in your root folder of the backend project. The environment file should have following variables:
```
MONGO_URI={MONGO_ATLAS_URI_WITH_AUTHENTICATION}
SESSION_KEY={RANDOM_SESSION_KEY}
JWT_SECRET={RANDOM_JWT_SECRET}
PORT={PORT}
PINATA_API_KEY={PINATA_API_KEY}
PINATA_SECRET_API_KEY={PINATA_SECRET_API_KEY}
ALCHEMY_API_KEY={ALCHEMY_API_KEY}
ALCHEMY_PRIVATE_KEY={ALCHEMY_PRIVATE_KEY}
CLOUDINARY_URL={CLOUDINARY_URL}
CLOUDINARY_NAME={CLOUDINARY_PROJECT_NAME}
CLOUDINARY_API_KEY={CLOUDINARY_API_KEY}
CLOUDINARY_SECRET={CLOUDINARY_SECRET_KEY}
```

After these steps, if you have nodemon in your machine, start the backend by:
```
nodemon start
```

If you do not have nodemon in your machine, use:
```
npm start
```

## Installing the Mobile Project
Clone the mobile project from GitHub. Then, go to project's root folder and open an .env file. After opening it, change its content to:
```
BACKEND_URL={YOUR_LOCAL_BACKEND_IP || OUR_DEPLOYED_IP}
```

Then, in the project directory, run:
```
flutter pub get
```

If you do not face any error, open an Android Emulator and run project through your personal choices.


That is it! You have installed our development environment on your local machine.

