
# Controllers

## Redirect
```
return \Redirect::route('lists.edit', 
            array($task->todolist->id))->with('message', 'Your list has been updated!');
```
