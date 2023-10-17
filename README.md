# MyWallet

## Description:
<p>The project is an expense and earnings management application, simulating a wallet, where the user can create an account and perform authentication, check the entries and exits of their wallet, and insert new entries and exits. On the front-end, the site structure was divided into code through components, in addition context was used to store the token necessary to make requests from the back-end. In the back-end, the code was created following a layered architecture, with routers, middleware and controllers.</p>

![Layout](./layout/tela1.png)
![Layout](./layout/tela2.png)
![Layout](./layout/tela3.png)
![Layout](./layout/tela4.png)
![Layout](./layout/tela5.png)
![Layout](./layout/tela6.png)
![Layout](./layout/tela7.png)


## Front-end
<p>Made using React.js</p>

* Login persistence check
* Access authenticated by token verification using uuid
* UseNavigate to change routes
* Transactions displayed on the home screen
* Addition of wallet entries and exits with transactions and balance stored in the database

## Back-end

<p>Made using Node.js, Express.js, and MongoDB</p>

* Using express Router to divide the backend layers into routers, middleware and controllers.
* Account creation with encrypted password using bcrypt
* Request validation in the backend using Joi

## Collections of MongoDB
The Database was divided by this manner:

### users
{<br/>
  name: string,<br/>
  email: string,<br/>
  password: string<br/>
}

### wallet
{<br/>
  name: string,<br/>
  total: number,<br/>
  transactions: [ ]<br/>
}

### sessions
{<br/>
  token: string,<br/>
  userId: number,<br/>
  lastStatus: Date<br/>
}