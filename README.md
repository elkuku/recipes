# Symfony Flex recipes

Custom [Symfony Flex](https://symfony.com/doc/current/setup/flex.html) recipes for my packages.

| Package                                                          | What the recipe does                                                           |
|------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [elkuku/symfony-utils](https://github.com/elkuku/symfony-utils) | Copies the dev and deploy scripts (`install`, `start`, `stop`, `deploy`) into `bin/`|

## Usage

Add the endpoint to your project's `composer.json`:

```json
"extra": {
    "symfony": {
        "endpoint": [
            "https://api.github.com/repos/elkuku/recipes/contents/index.json?ref=flex/main",
            "flex://defaults"
        ]
    }
}
```

## Adding or changing a recipe

Recipes live in `<vendor>/<package>/<version>/` on `main`, in the same format as
[symfony/recipes-contrib](https://github.com/symfony/recipes-contrib).
On every push to `main`, the `Update Flex endpoint` workflow regenerates the endpoint files in the `flex/main` branch.
