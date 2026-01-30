# ng-hub-ui-charts Library

Internal library documentation for development and contribution.

## Project Structure

```
projects/swimlane/ngx-charts/
├── src/
│   ├── public-api.ts          # Main entry point for the library
│   ├── lib/                   # Library components and modules
│   │   ├── area-chart/        # Area chart components
│   │   ├── bar-chart/         # Bar chart components
│   │   ├── bubble-chart/      # Bubble chart components
│   │   ├── box-chart/         # Box plot chart components
│   │   ├── gauge/             # Gauge components
│   │   ├── heat-map/          # Heatmap components
│   │   ├── line-chart/        # Line chart components
│   │   ├── pie-chart/         # Pie/Donut chart components
│   │   ├── polar-chart/       # Polar chart components
│   │   ├── sankey/            # Sankey diagram components
│   │   ├── tree-map/          # Treemap components
│   │   ├── number-card/       # Number card components
│   │   ├── common/            # Shared components and utilities
│   │   └── models/            # TypeScript models and interfaces
│   ├── test.ts                # Test configuration
│   └── ...
├── ng-package.json            # ng-packagr configuration
├── package.json               # Library-specific metadata
├── tsconfig.lib.json          # TypeScript configuration for library
├── tsconfig.lib.prod.json     # TypeScript configuration for production build
└── tsconfig.spec.json         # TypeScript configuration for tests
```

## Development

### Building the Library

```bash
# Development build
npm run build:lib

# Production build (optimized for distribution)
npm run build:lib:prod
```

Output is generated in `dist/ng-hub-ui-charts/`

### Running Tests

```bash
# Run tests once
npm run test:unit

# Watch mode for development
npm run test:watch

# CI mode (headless, no watch)
npm run test:ci
```

### Linting

```bash
# Check linting issues
npm run lint

# Fix linting issues automatically
npm run fix:lint
```

## Adding a New Chart Type

1. Create a new folder in `src/lib/` (e.g., `src/lib/my-chart/`)
2. Create the main component (`my-chart.component.ts`)
3. Create a series component if needed (`my-chart-series.component.ts`)
4. Create a module (`my-chart.module.ts`)
5. Export from `src/public-api.ts`
6. Add to `src/lib/ngx-charts.module.ts` if needed for global export

## Component Guidelines

- Use Angular components and directives
- Leverage D3 for calculations and data processing
- Use RxJS for reactive updates
- Follow existing naming conventions
- Include proper TypeScript types
- Document public APIs with JSDoc comments

## Publishing

```bash
# Prepare library for distribution
npm run package

# Publish to npm
npm run publish:lib

# Publish beta version
npm run publish:lib:beta
```

## Dependencies

### Peer Dependencies
- @angular/core 21.x
- @angular/common 21.x
- @angular/animations 21.x
- @angular/forms 21.x
- @angular/platform-browser 21.x
- rxjs 7.x

### Direct Dependencies
- d3-* libraries (scales, shapes, selections, etc.)
- gradient-path (for gradient effects)
- tslib (TypeScript utilities)

## References

- [Original ngx-charts](https://github.com/swimlane/ngx-charts)
- [ng-packagr Documentation](https://ng-packagr.github.io/)
- [Angular Library Guide](https://angular.io/guide/creating-libraries)
