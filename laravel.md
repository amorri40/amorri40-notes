
# Models

## Find an instance of a Model
```
Role::where('name','=','create-users')->first()
```

# Controllers

## Redirect
```
return \Redirect::route('lists.edit', 
            array($task->todolist->id))->with('message', 'Your list has been updated!');
```

## Flash message and then redirect
```
\Session::flash('message', 'Successfully updated!');
        return Redirect::route('login_path');
```

## Send Email Message
```
Mail::send('email.verify', $confirmation_code, function($message) {
            $message->to(Input::get('email'), Input::get('username'))
                ->subject('Verify your email address');
        });
```
