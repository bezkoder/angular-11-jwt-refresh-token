# Angular 11 JWT Refresh Token example with Http Interceptor

You can take a look at following flow to have an overview of Requests and Responses that Angular 11 Client will make or receive.

## Angular JWT Refresh Token Flow
![angular-11-refresh-token-jwt-interceptor-example](angular-11-refresh-token-jwt-interceptor-example.png)

For more detail, please visit:
> [Angular 11 JWT Refresh Token example with Http Interceptor](https://www.bezkoder.com/angular-11-jwt-refresh-token/)

> [Angular 11 JWT Authentication & Authorization with Web API](https://bezkoder.com/angular-11-jwt-auth/)

## Fullstack
> [Angular + Spring Boot: JWT Authentication & Authorization example](https://bezkoder.com/angular-11-spring-boot-jwt-auth/)

> [Angular + Node.js Express: JWT Authentication & Authorization example](https://bezkoder.com/node-js-angular-11-jwt-authentication/)

Open `app/_helpers/auth.interceptor.js`, modify the code to work with **x-access-token** like this:
```js
...

// const TOKEN_HEADER_KEY = 'Authorization'; // for Spring Boot back-end
const TOKEN_HEADER_KEY = 'x-access-token';   // for Node.js Express back-end

@Injectable()
export class AuthInterceptor implements HttpInterceptor {
  ...

  private addTokenHeader(request: HttpRequest<any>, token: string) {
    /* for Spring Boot back-end */
    // return request.clone({ headers: request.headers.set(TOKEN_HEADER_KEY, 'Bearer ' + token) });

    /* for Node.js Express back-end */
    return request.clone({ headers: request.headers.set(TOKEN_HEADER_KEY, token) });
  }
}

...
```

Run `ng serve --port 8081` for a dev server. Navigate to `http://localhost:8081/`.

## More practice
> [Angular 11 CRUD Application example with Web API](https://bezkoder.com/angular-11-crud-app/)

> [Angular 11 Pagination example using ngx-pagination](https://bezkoder.com/angular-11-pagination-ngx/)

> [Angular 11 File Upload example with progress bar](https://bezkoder.com/angular-11-file-upload/)

Fullstack with Node.js Express:
> [Angular 11 + Node.js Express + MySQL](https://bezkoder.com/angular-11-node-js-express-mysql/)

> [Angular 11 + Node.js Express + PostgreSQL](https://bezkoder.com/angular-11-node-js-express-postgresql/)

> [Angular 11 + Node.js Express + MongoDB](https://bezkoder.com/angular-11-mongodb-node-js-express/)

> [Angular 11 + Node.js Express: JWT Authentication & Authorization example](https://bezkoder.com/node-js-angular-11-jwt-authentication/)

Fullstack with Spring Boot:
> [Angular 11 + Spring Boot + MySQL](https://bezkoder.com/angular-11-spring-boot-crud/)

> [Angular 11 + Spring Boot + PostgreSQL](https://bezkoder.com/angular-11-spring-boot-postgresql/)

> [Angular 11 + Spring Boot + MongoDB](https://bezkoder.com/angular-11-spring-boot-mongodb/)

> [Angular 11 + Spring Boot: File upload example](https://bezkoder.com/angular-11-spring-boot-file-upload/)

> [Angular 11 + Spring Boot: JWT Authentication & Authorization example](https://bezkoder.com/angular-11-spring-boot-jwt-auth/)

Fullstack with Django:
> [Angular 11 + Django Rest Framework](https://bezkoder.com/django-angular-11-crud-rest-framework/)

> [Angular 11 + Django + MySQL](https://bezkoder.com/django-angular-mysql/)

> [Angular 11 + Django + PostgreSQL](https://bezkoder.com/django-angular-postgresql/)

Serverless with Firebase:
> [Angular 11 Firebase CRUD Realtime DB | AngularFireDatabase](https://bezkoder.com/angular-11-firebase-crud/)

> [Angular 11 Firestore CRUD | AngularFireStore](https://bezkoder.com/angular-11-firestore-crud-angularfirestore/)

> [Angular 11 Upload File to Firebase Storage example](https://bezkoder.com/angular-11-file-upload-firebase-storage/)

Integration (run back-end & front-end on same server/port)
> [How to Integrate Angular with Node.js Restful Services](https://bezkoder.com/integrate-angular-10-node-js/)

> [How to Integrate Angular with Spring Boot Rest API](https://bezkoder.com/integrate-angular-11-spring-boot/)