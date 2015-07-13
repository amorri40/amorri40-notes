

## Delete
```
/**
	 * Delete an OBJECT
	 * @param  integer $id The list ID
	 * @return Response
	 */
	public function destroy($id)
	{
        $object = OBJECT::findOrFail($id);
        $object->delete();
        return \Redirect::route('OBJECT.index')
            ->with('message', 'OBJECT deleted!');
	}
```
