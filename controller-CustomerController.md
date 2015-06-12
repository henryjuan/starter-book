# Controller - CustomerController

```php
Route::get('customer/{id}', 'CustomerController@showProfile');
```

```php
php artisan make:controller PhotoController
```

```php
<?php namespace App\Http\Controllers;

use Illuminate\Http\Request;
use App\Http\Controllers\Controller;

class CustomerController extends Controller
{
	protected $customers;

    public function __construct(CustomerRepository $customers)
    {
    	$this->customers = $customers;

        $this->middleware('auth');

        $this->middleware('log', ['only' => ['fooAction', 'barAction']]);

        $this->middleware('subscribed', ['except' => ['fooAction', 'barAction']]);
    }

    public function getNew()
    {
    	return view('customer.new');
    }

    public function postNew(Request $request)
    {
    	//TODO 新客戶審核
    }

    public function postApproval()
    {
    	$credentials = Input::only([
            'email',
            'password',
            'password_confirmation',
            'token'
        ]);

        $response = Password::reset($credentials, function ($user, $password) {
            $user->password = Hash::make($password);

            $user->save();
        });
    }

    public function showProfile($id)
    {
    	$customer = $this->customers->getCustomerById($id)
        return view('customer.profile', ['customer' => $customer]);
    }

    public function store(Request $request)
    {
        $name = $request->input('name');

        //
    }

    public function update(Request $request, $id)
    {
        //
    
}
```