Angular form-model
==================

Angularjs directive for defining a model on a form. Directive will set the ng-model property on all inputs with the name-attribute.

Lets say you have an input form for registering users.

```html
<form>
	<input name="username" />
	<input name="email" />
</form>
```

Normally you would add an ng-model attribute to each field, like this:

```html
<form>
	<input name="username" ng-model="newUser.username" />
	<input name="email" ng-model="newUser.email" />
</form>
```

With this directive you can define the "newUser" model on the form
like this: <form form-model="newUser">. The directive will add 
ng-model to all child inputs with a name attribute.

This gives you the power of ng-model with a lot less effort.

Example:

```html
<form form-model="newUser">
	<input name="username" />
	<input name="email" />
</form>
```

Will automatically be transformed into :

```html
<form form-model="newUser">
	<input name="username" ng-model="newUser.username" />
	<input name="email" ng-model="newUser.email" />
</form>
```