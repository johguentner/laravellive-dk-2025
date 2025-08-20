# ShowNotes - The Mindful Laravel Developer
## Books
Laravel Up & Running (Matt Stauffer):
https://mattstauffer.com/laravel-up-and-running/

Best Practices for Laravel Enterprice Applications (Wendell Adriel):
https://wendelladriel.com/best-practices-for-laravel-enterprise-applications

Battle Ready Laravel (Ash Allen):
https://battle-ready-laravel.com/

Advanced Inertia (Boris Lepikhin):
https://advanced-inertia.com/

## Online Resources
### General
Repository with various Laravel Best Practices:
https://github.com/alexeymezenin/laravel-best-practices

### Online Courses and Videos about Actions, Modularization etc.
Modular Laravel (Laracasts, Mateus Guimarães):
https://laracasts.com/series/modular-laravel

Laravel Project Structure (LaravelDaily, Povilas Korop):
https://laraveldaily.com/lesson/laravel-projects-structure/validation-to-form-request

Intermediate Developer Trap (Youtube, Jeffrey Way):
https://www.youtube.com/watch?v=-ezOz6vPLoo

Various Laravel Best Practice Advice (Youtube, Nuno Maduro):
https://www.youtube.com/@nunomaduro/videos

## Packages / Extensions
Laravel Validated DTO (Wendell Adriel):
https://github.com/WendellAdriel/laravel-validated-dto

Laravel Actions (Loris Leiva):
https://www.laravelactions.com/

Todo Tree VSCode Extension (Gruntfuggly):
https://marketplace.visualstudio.com/items?itemName=Gruntfuggly.todo-tree

## Code Boundaries

### Simple Version
```
- Input -> f.e. FormRequest
- Delegation -> f.e. Controller
- Orchestration -> f.e. Action
- Business Logic -> f.e. Action
- Utilities -> f.e. Service
```

### Version with Transitions
```
// ">" is a Transition; "-" is a Boundary
> Inbound Processing (f.e. Routing, Middlewares, Policies)
- Delegation (Controller)
> Contract Validation (f.e. FormRequest, Policies, DTOs)
- Orchestration (Action)
> Domain Enforcement (Business Logic Conditions, DTOs)
- Business Logic (Action)
> System Integration (DTOs, Mapping Data)
- Utilities (Service)
``` 
