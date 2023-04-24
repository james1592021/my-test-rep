# my-test-rep

With the configuration in Configuration/Objects.yaml you can inject/instantiate the Psr\EventDispatcher\EventDispatcherInterface interface

use Psr\EventDispatcher\EventDispatcherInterface;

public function __construct(
    protected readonly EventDispathcerInterface $eventDispathcer
) {}

public function method(string $argument): void
{
    // what ever business logic goes before the dispatching
    $this->eventDispatcher->dispatch(new ProductWasCreated($argument));
}
