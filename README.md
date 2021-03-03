# vaadin-auth0
This is an example project demonstrating how to configure and use the Auth0 Universal Login functionality in Vaadin apps.

## Configuration

### Auth0 Dashboard
1. On the [Auth0 Dashboard](https://manage.auth0.com/#/clients) create a new Application of type **Regular Web Application**.
1. On the **Settings** tab of your application, add the URL `http://localhost:3000/login/oauth2/code/auth0` to the **Allowed Callback URLs** field.
1. On the **Settings** tab of your application, add the URL `http://localhost:3000/` to the **Allowed Logout URLs** field.
1. Save the changes to your application settings. Don't close this page; you'll need some of the settings when configuring the application below.

## Application configuration

Copy `src/main/resources/application.yml.example` to `src/main/resources/application.yml`:

```bash
cp src/main/resources/application.yml.example src/main/resources/application.yml
```

Set the application values in the `src/main/resources/application.yml` file to the values of your Auth0 application.

```yaml
client-id: {YOUR-CLIENT-ID}
client-secret: {YOUR-CLIENT-SECRET}
issuer-uri: https://{YOUR-DOMAIN}/
```

## Running the Application
Import the project to the IDE of your choosing as a Maven project.

Run the application using `mvn spring-boot:run` or by running the `Application` class directly from your IDE.

Open http://localhost:3000/ in your browser.

## Create a free account in Auth0

1. Go to [Auth0](https://auth0.com) and click Sign Up.
2. Use Google, GitHub or Microsoft Account to login.

## More Information

- [Vaadin + OAuth tutorial](https://vaadin.com/learn/tutorials/google-login)
- [Vaadin documentation](https://vaadin.com/docs)
- [Using Vaadin and Spring](https://vaadin.com/docs/v14/flow/spring/tutorial-spring-basic.html) article
- [Auth0 Java Spring Boot QuickStart](https://auth0.com/docs/quickstart/webapp/java-spring-boot)
- [Auth0 documentation] (https://auth0.com/docs)
