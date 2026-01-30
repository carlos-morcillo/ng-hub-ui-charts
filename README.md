# ng-hub-ui-charts

[![npm version](https://badge.fury.io/js/ng-hub-ui-charts.svg)](https://badge.fury.io/js/ng-hub-ui-charts)
[![npm downloads](https://img.shields.io/npm/dm/ng-hub-ui-charts.svg)](https://npmjs.org/ng-hub-ui-charts)

> **Part of the [ng-hub-ui](https://github.com/carlos-morcillo/ng-hub-ui) family** - A collection of standalone Angular component libraries

Declarative Charting Framework for Angular with Angular 21+ support!

## About This Fork

**ng-hub-ui-charts** is a maintained fork of [ngx-charts](https://github.com/swimlane/ngx-charts) by Swimlane, updated for Angular 21+ compatibility. It's part of the ng-hub-ui family of component libraries, following the same design patterns and integration standards.

### What's Different

- **Angular 21+ Support**: Updated dependencies and compatibility with the latest Angular versions
- **ng-hub-ui Integration**: Follows ng-hub-ui standards for consistency across the component family
- **Maintained**: Regular updates and maintenance to support current Angular versions

### Original Project

The original and incredible work is by [Swimlane](http://swimlane.com). This fork maintains their excellent charting architecture while updating for modern Angular development.

## About ng-hub-ui

The **ng-hub-ui** family provides a collection of standalone, reusable Angular components:

- [ng-hub-ui-paginable](https://github.com/carlos-morcillo/ng-hub-ui-paginable) - Advanced tables and pagination components
- [ng-hub-ui-charts](https://github.com/carlos-morcillo/ng-hub-ui-charts) - **This library** - Charting and data visualization
- [And more...](https://github.com/carlos-morcillo?tab=repositories&q=ng-hub-ui)

All libraries follow consistent patterns and work seamlessly together.

## Features

### Chart Types

- Horizontal & Vertical Bar Charts (Standard, Grouped, Stacked, Normalized)
- Line
- Area (Standard, Stacked, Normalized)
- Pie (Explodable, Grid, Custom legends)
- Bubble
- Donut
- Gauge (Linear & Radial)
- Heatmap
- Treemap
- Number Cards
- Sankey Diagram

### Customization

- Autoscaling
- Timeline Filtering
- Line Interpolation
- Configurable Axis Labels
- Legends (Labels & Gradient)
- Advanced Label Positioning
- Real-time data support
- Advanced Tooltips
- Data point Event Handlers
- Works with ngUpgrade

## Quick Start

### Installation

```bash
npm install ng-hub-ui-charts
```

### Usage

Import the chart component in your Angular module:

```typescript
import { NgxChartsModule } from 'ng-hub-ui-charts';

@NgModule({
  imports: [NgxChartsModule]
})
export class AppModule { }
```

Use in your template:

```html
<ngx-charts-bar-horizontal
  [view]="view"
  [scheme]="colorScheme"
  [results]="data"
  [xAxis]="true"
  [yAxis]="true"
  [legend]="true"
  [showXAxisLabel]="true"
  [showYAxisLabel]="true"
  xAxisLabel="Country"
  yAxisLabel="Sales">
</ngx-charts-bar-horizontal>
```

## Documentation

- **Live Demo**: Coming soon with ng-hub-ui-charts
- **Original ngx-charts Docs**: [https://swimlane.gitbook.io/ngx-charts](https://swimlane.gitbook.io/ngx-charts)
- **Custom Charts**: See [custom-charts.md](docs/custom-charts.md) for building custom charts using ngx-charts components

## Requirements

- Angular 21+
- RxJS 7.8+
- TypeScript 5.9+
- Node.js 22.16+

## API & Architecture

ng-hub-ui-charts maintains full compatibility with the ngx-charts API. Charts are built using:

- **Angular** for rendering and animation of SVG elements
- **D3** for mathematical functions, scales, axis and shape generators
- Signal-based reactivity for optimal change detection

This approach provides:
- Native Angular rendering with AoT compilation support
- Server-side rendering (SSR) compatibility
- Type safety and excellent IDE support

## Custom Charts

Leverage various ngx-charts components to build custom charts:

```typescript
import {
  ChartComponent,
  AreaChartComponent,
  AxisComponent
} from 'ng-hub-ui-charts';
```

Refer to [custom-charts.md](docs/custom-charts.md) for detailed examples.

## 🤝 Contributing

We welcome contributions! Whether you've found a bug, want to improve the documentation, or add new features, your help is appreciated.

### Getting Started

1. **Fork** the repository
2. **Clone** your fork: `git clone https://github.com/your-username/ng-hub-ui-charts.git`
3. **Install dependencies**: `yarn install`
4. **Create a branch**: `git checkout -b feature/your-feature-name`

### Development

```bash
# Start development server
yarn start

# Run tests
yarn test

# Build the library
yarn build:lib:prod

# Run linting and formatting checks
yarn lint
yarn prettier:ci
```

### Submitting Changes

1. **Code Style**: Ensure your code follows the project's style (run `yarn fix` to auto-fix)
2. **Tests**: Add tests for new features or bug fixes
3. **Commit**: Use clear, descriptive commit messages
4. **Push**: Push to your fork
5. **Create a Pull Request**: Open a PR with a clear description of your changes

### Issues

Found a bug? Please [create an issue](https://github.com/carlos-morcillo/ng-hub-ui-charts/issues) with:
- Clear description of the problem
- Steps to reproduce
- Expected vs actual behavior
- Angular and library versions

### Development Guidelines

- Follow the existing code patterns and structure
- Maintain compatibility with Angular 21+
- Update documentation for new features
- Ensure all tests pass before submitting PR
- Keep commits atomic and focused

### Questions?

Feel free to open a [discussion](https://github.com/carlos-morcillo/ng-hub-ui-charts/discussions) or reach out through the repository issues.

## License

MIT - See [LICENSE](LICENSE) for details

## Credits & Attribution

**Original Project**: [ngx-charts](https://github.com/swimlane/ngx-charts) by [Swimlane](http://swimlane.com)

Swimlane is an automated cyber security operations platform. Learn more at [swimlane.com](http://swimlane.com)

**Current Maintainer**: Carlos Morcillo
**Package**: ng-hub-ui-charts
**Part of**: [ng-hub-ui](https://github.com/carlos-morcillo/ng-hub-ui) family
