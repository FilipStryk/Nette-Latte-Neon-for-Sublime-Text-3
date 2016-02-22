# Nette + Latte + Neon for Sublime Text 3
Latte and Neon syntax highlighting, code completions and Nette snippets for Sublime Text 3.

## Installation
### Via [Package Control](https://packagecontrol.io/installation):
1. Press `Control + Shift + P` on Windows/Linux or `Command + Shift + P` on OS X
2. Search `Nette + Latte + NEON`
3. Press `Enter`
4. **Complete!**

### Via [Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git):
1. Go to your Sublime Text packages folder (In ST3 `Preferences -> Browse Packages...`)
2. `git clone http://github.com/FilipStryk/Nette-Latte-Neon-for-Sublime-Text-3.git`
3. **Complete!**

## Neon syntax highlighting
![Neon syntax highlighting](http://s13.postimg.org/wfvp5f453/neon_highlighting.png)

## Available snippets:
### persist
**Persistent property**
```php
/**
 * @persistent
 * @var type
 */
public $property;
```
### inject
**Inject property**
```php
/**
 * @inject
 * @var type
 */
public $property;
```
### act
**Action method**
```php
public function actionName()
{

}
```
### ren
**Render method**
```php
public function renderName()
{

}
```
### hand
**Handle method**
```php
public function handleName()
{
	
}
```
### sup
**Stratup method**
```php
protected function startup()
{
	parent::startup();
	
}
```
### con
**Constructor that calls parent**
```php
public function __construct()
{
	parent::__construct();
	
}
```
### inject-method
**Inject method**
```php
/**
 * @param  Service $service
 */
public function injectService(Service $service)
{
	$this->service = $service;
}
```
### form-component
**Component factory with form definition**
```php
/**
 * @return Nette\Application\UI\Form
 */
protected function createComponentForm()
{
	$form = new Nette\Application\UI\Form;
	$form->
	$form->addSubmit('send', 'Odeslat');
	$form->onSuccess[] = function (Nette\Application\UI\Form $form) {
		$values = $form->getValues();
	};

	return $form;
}
```
### form-control
**Form control class**
```php
class SignInForm extends \Nette\Application\UI\Control
{

	/**
	 * @return \Nette\Application\UI\Form
	 */
	protected function createComponentSignInForm()
	{
		$form = new \Nette\Application\UI\Form;
		$form->
		$form->addSubmit('send', 'Odeslat');
		$form->onSuccess[] = ->signInFormSucceeded;

		return $form;
	}

	/**
	 * @param  \Nette\Application\UI\Form  $form
	 * @param  \Nette\Utils\ArrayHash      $values
	 */
	public function SignInFormSucceeded(\Nette\Application\UI\Form $form, \Nette\Utils\ArrayHash $values)
	{
		
	}

}
```
### ifa
**Interface form factory**
```php
interface ISignInFormFactory
{

	/**
	 * @return SignInForm
	 */
	function create();

}
```
### kdel
**Kdyby Events listener**
```php
class ApplicationListener extends \Nette\Object implements \Kdyby\Events\Subscriber
{

	/**
	 * @var \Monolog\Logger
	 */
	private $logger;

	/**
	 * @param \Monolog\Logger $logger
	 */
	public function __construct(\Monolog\Logger $logger)
	{
		$this->logger = $logger;
	}

	/**
	 * @return array
	 */
	public function getSubscribedEvents()
	{
		return [
			'Nette\Application\Application::onStartup'
		];
	}

	public function onStartup()
	{
		
	}

}
```

## Completions:
### Functions:
* `barDump` => `\Tracy\Debugger::barDump(var, title);`
* `dump` => `\Tracy\Debugger::dump(var);`
* `timer` => `\Tracy\Debugger::timer(name);`
* `tlog` => `\Tracy\Debugger::log(message, priority);`
* `flog` => `\Tracy\Debugger::fireLog(message);`

### Namespaces
**Nette\Application**
* `n-a-c` => `Nette\Application\UI\Control`
* `n-a-f` => `Nette\Application\UI\Form`
* `n-a-p` => `Nette\Application\UI\Presenter`
* `n-a-re-c` => `Nette\Application\Responses\CallbackResponse`
* `n-a-re-fi` => `Nette\Application\Responses\FileResponse`
* `n-a-re-fo` => `Nette\Application\Responses\ForwardResponse`
* `n-a-re-j` => `Nette\Application\Responses\JsonResponse`
* `n-a-re-r` => `Nette\Application\Responses\RedirectResponse`
* `n-a-re-t` => `Nette\Application\Responses\TextResponse`
* `n-a-ro-c` => `Nette\Application\Routers\CliRouter`
* `n-a-ro-r` => `Nette\Application\Routers\Route`
* `n-a-ro-rl` => `Nette\Application\Routers\RouteList`
* `n-a-ro-sr` => `Nette\Application\Routers\SimpleRouter`

**Nette\Database**
* `n-d-con` => `Nette\Database\Connection`
* `n-d-ctx` => `Nette\Database\Context`

**Nette\Http**
* `n-h-ctx` => `Nette\Http\Context`
* `n-h-fu` => `Nette\Http\FileUpload`
* `n-h-h` => `Nette\Http\Helpers`
* `n-h-rq` => `Nette\Http\Request`
* `n-h-rs` => `Nette\Http\Response`
* `n-h-s` => `Nette\Http\Session`
* `n-h-url` => `Nette\Http\Url`

**Nette\Mail**
* `n-m-m` => `Nette\Mail\Message`
* `n-m-sm` => `Nette\Mail\SendmailMailer`
* `n-m-smtp` => `Nette\Mail\SmtpMailer`
* `n-m-im` => `Nette\Mail\IMailer`

**Nette\Security**
* `n-s-id` => `Nette\Security\Identity`
* `n-s-pass` => `Nette\Security\Passwords`
* `n-s-perm` => `Nette\Security\Permission`
* `n-s-us` => `Nette\Security\User`
* `n-s-iauthenticator` => `Nette\Security\IAuthenticator`
* `n-s-iauthorizator` => `Nette\Security\IAuthorizator`
* `n-s-iid` => `Nette\Security\IIdentity`
* `n-s-ire` => `Nette\Security\IResource`
* `n-s-iro` => `Nette\Security\IRole`
* `n-s-ius` => `Nette\Security\IUserStorage`
* `n-s-ae` => `Nette\Security\AuthenticationException`

**Nette\Utils**
* `n-u-ah` => `Nette\Utils\ArrayHash`
* `n-u-al` => `Nette\Utils\ArrayList`
* `n-u-ar` => `Nette\Utils\Arrays`
* `n-u-c` => `Nette\Utils\Callback`
* `n-u-dt` => `Nette\Utils\DateTime`
* `n-u-fs` => `Nette\Utils\FileSystem`
* `n-u-f` => `Nette\Utils\Finder`
* `n-u-h` => `Nette\Utils\Html`
* `n-u-i` => `Nette\Utils\Image`
* `n-u-j` => `Nette\Utils\Json`
* `n-u-p` => `Nette\Utils\Paginator`
* `n-u-r` => `Nette\Utils\Random`
* `n-u-s` => `Nette\Utils\Strings`
* `n-u-v` => `Nette\Utils\Validators`
* `n-o` => `Nette\Object`