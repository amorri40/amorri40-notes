
# Controllers

## Redirect
```
return \Redirect::route('lists.edit', 
            array($task->todolist->id))->with('message', 'Your list has been updated!');
```

## Flash message and then redirect
```
Flash::message('You have successfully verified your account.');
        return Redirect::route('login_path');
```
