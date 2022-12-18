
```
composer create-project "laravel/laravel=9.*" laravel9-breeze
cd laravel9-breeze
```

```
composer require laravel/breeze
php artisan breeze:install
```

```
php artisan route:list

 GET|HEAD  / ...............................................................................................................................
  POST      _ignition/execute-solution ........................ ignition.executeSolution › Spatie\LaravelIgnition › ExecuteSolutionController
  GET|HEAD  _ignition/health-check .................................... ignition.healthCheck › Spatie\LaravelIgnition › HealthCheckController
  POST      _ignition/update-config ................................. ignition.updateConfig › Spatie\LaravelIgnition › UpdateConfigController
  GET|HEAD  api/user ........................................................................................................................
  GET|HEAD  confirm-password ..................................................... password.confirm › Auth\ConfirmablePasswordController@show
  POST      confirm-password ....................................................................... Auth\ConfirmablePasswordController@store
  GET|HEAD  dashboard ............................................................................................................. dashboard
  POST      email/verification-notification .......................... verification.send › Auth\EmailVerificationNotificationController@store
  GET|HEAD  forgot-password ...................................................... password.request › Auth\PasswordResetLinkController@create
  POST      forgot-password ......................................................... password.email › Auth\PasswordResetLinkController@store
  GET|HEAD  login ........................................................................ login › Auth\AuthenticatedSessionController@create
  POST      login ................................................................................. Auth\AuthenticatedSessionController@store
  POST      logout ..................................................................... logout › Auth\AuthenticatedSessionController@destroy
  PUT       password ....................................................................... password.update › Auth\PasswordController@update
  GET|HEAD  profile ................................................................................... profile.edit › ProfileController@edit
  PATCH     profile ............................................................................... profile.update › ProfileController@update
  DELETE    profile ............................................................................. profile.destroy › ProfileController@destroy
  GET|HEAD  register ........................................................................ register › Auth\RegisteredUserController@create
  POST      register .................................................................................... Auth\RegisteredUserController@store
  POST      reset-password ................................................................ password.store › Auth\NewPasswordController@store
  GET|HEAD  reset-password/{token} ....................................................... password.reset › Auth\NewPasswordController@create
  GET|HEAD  sanctum/csrf-cookie ........................................... sanctum.csrf-cookie › Laravel\Sanctum › CsrfCookieController@show
  GET|HEAD  verify-email .............................................. verification.notice › Auth\EmailVerificationPromptController@__invoke
  GET|HEAD  verify-email/{id}/{hash} .............................................. verification.verify › Auth\VerifyEmailController@__invoke
```

```
php artisan migrate
```

```
php artisan tinker

> $user = new User;
> $user->name = "ユーザー名";
> $user->email = "メールアドレス";
> $user->password = Hash::make("パスワード");
> $user->save();
```



php artisan serve


Access to http://127.0.0.1:8000/login