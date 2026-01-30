# Digital Ecosystem Library

A C# library for visualizing digital ecosystems with animals and plants.

## What It Does

Provides visualization tools for ecosystem simulations:
- `AsCircle()` - Displays organisms in a circular "circle of life" layout
- `AsHierarchy()` - Shows organisms grouped by type (Animals/Plants)
- Color-coded display (red for animals, green for plants)

## Installation

### Building the Package
```bash
cd DigitalEcosystemLib
dotnet pack
```

This creates `DigitalEcosystemLib.1.0.0.nupkg` in `bin/Release/` (or `bin/Debug/`).

### Installing in Your Project
```bash
dotnet add package DigitalEcosystemLib --source /path/to/DigitalEcosystemLib/bin/Release
```

## Usage

Implement the `IOrganism` interface in your classes, then visualize your ecosystem:
```csharp
using DigitalEcosystemLib;

List<IOrganism> world = new List<IOrganism>();
// ... add your organisms ...

EcosystemDisplay.AsCircle(world);
```

## Requirements

- .NET 10.0 or higher
- Your organism classes must inherit from `Animal` or `Plant` base classes
