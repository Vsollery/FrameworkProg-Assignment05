# Session 8 - Templated Components

In this session we will make some of the original components more reusable by refactoring them. We'll also construct a separate library project along the way to serve as a home for the additional components.

#### new component library

![](/images/session-8/template-components.jpg)

#### templated dialog

```html
@if (Show)
{
    <div class="dialog-container">
        <div class="dialog">
            @ChildContent
        </div>
    </div>
}

@code {
    [Parameter] public RenderFragment ChildContent { get; set; }
    [Parameter] public bool Show { get; set; }
}


```

### Using new dialog
We can use it in `index.razor`

```html
<TemplatedDialog Show="OrderState.ShowingConfigureDialog">
    <ConfigurePizzaDialog
        Pizza="OrderState.ConfiguringPizza"
        OnCancel="OrderState.CancelConfigurePizzaDialog"
        OnConfirm="OrderState.ConfirmConfigurePizzaDialog" />
</TemplatedDialog>
```
