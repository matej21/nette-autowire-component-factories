# Autowire arguments in createComponent* methods


discussion: http://forum.nette.org/cs/13791-createcomponent-injectovani-tovarnicky-primo-do-metody (czech only)


## Include in application


```php
abstract class BasePresenter extends Nette\Application\UI\Presenter
{
	use \matej21\AutowireComponentFactories;

}
```


## Usage


```php
class FooPresenter extends BasePresenter
{

    public function createComponentBar(BarFactory $factory)
    {
        $component = $factory->create();
        return $component;

    }
}
```