# Ironman Fanz

## Objective

Confirm custom models have more training-related completions compared to the standard `copilot-codex`.

## Assessment

Using the default (`copilot-codex`) model, open `page.tsx` and in the `return`, type `<StarkPatentTracker `.

```tsx
// Bad
<StarkPatentTracker />

// Good
<StarkPatentTracker patents={patents} />

// Good
<StarkPatentTracker patents={[{ id: 'abc123', title: 'PATENT_TITLE_01' }]} />
```

## Changing Copilot Models

- Open `settings.json` and open Copilot Logs (via `Cmd + Shift + P`)
- The first chunk of logs include all model names available to you
- The default JSON values:

```json
{
  "github.copilot.advanced": {
    "debug.overrideEngine": "copilot-codex"
  }
}
```

- Replace `copilot-codex` with the relevant model. Currently, it'll be something like `copilot-prod-finetune-centralus.Treadstone-Industries-`
- Reload the developer window (via `Cmd + Shift + P`)
