# WPF Blazor Hybrid Application Sample

## Overview

This sample demonstrates how to host and run Blazor UI content inside a Windows Presentation Foundation (WPF) desktop application. The project combines traditional WPF application infrastructure with Razor components, enabling developers to build desktop applications using familiar Blazor development patterns.

The sample includes a Razor component rendered within a WPF window and provides the foundational setup required for Blazor and WPF integration. It serves as a lightweight starting point for developers who want to reuse Blazor components in desktop environments or explore hybrid application development with .NET.

## Key Features

- Hosts Blazor components inside a native WPF application using `BlazorWebView`.
- Uses the Syncfusion [Blazor Calendar](https://www.syncfusion.com/blazor-components/blazor-calendar) component for date selection and calendar visualization.
- Renders the `SfCalendar` component through the `Counter.razor` Razor component.
- Configures Blazor rendering within WPF using the `AddWpfBlazorWebView()` service registration.
- Registers Syncfusion Blazor services using the `AddSyncfusionBlazor()` extension method.
- Demonstrates dependency injection setup through `ServiceCollection` and application-level service provider registration.
- Uses the `HostPage="wwwroot\index.html"` configuration to load the Blazor application inside the WPF window.
- Registers the Razor component as a root component using the `RootComponent` configuration with:
  - `Selector="#app"`
  - `ComponentType="{x:Type local:Counter}"`
- Demonstrates integration between WPF XAML UI and Blazor Razor components within a single desktop application.
- Uses the `SfCalendar` component with the `TValue="DateTime"` property to enable date-based value selection.

## Prerequisites

- [Visual Studio 2022](https://visualstudio.microsoft.com/vs/) or [Visual Studio Code](https://code.visualstudio.com/)
- [.NET SDK](https://dotnet.microsoft.com/en-us/download/dotnet) compatible with the project's target framework
- Windows operating system with WPF support enabled

## How to Run the Project

**Visual Studio 2022**

1. Clone or download this repository.
2. Open `WpfBlazorApp.sln`.
3. Restore all NuGet packages.
4. Ensure `WpfBlazorApp` is selected as the startup project.
5. Build the solution.
6. Press `Ctrl+F5` to run the application.

**Visual Studio Code**

1. Open the repository folder in Visual Studio Code.
2. Open a terminal and navigate to the project directory.

```bash
cd WpfBlazorApp
dotnet restore
dotnet run
```

3. Launch the application after the build completes successfully.

This sample runs as a desktop WPF application and does not expose a local web URL.

## Project Structure

`WpfBlazorApp.sln` - Visual Studio solution file for the WPF Blazor sample.

`WpfBlazorApp/App.xaml` - Defines application startup behavior and launches `MainWindow.xaml`.

`WpfBlazorApp/App.xaml.cs` - Application entry point and WPF application initialization class.

`WpfBlazorApp/AssemblyInfo.cs` - Configures theme resource dictionary locations using the `ThemeInfo` assembly attribute.

`WpfBlazorApp/MainWindow.xaml` - Hosts the `BlazorWebView` control and configures the Blazor root component rendering pipeline.

`WpfBlazorApp/MainWindow.xaml.cs` - Registers Blazor WebView services, Syncfusion Blazor services, Syncfusion license information, and creates the dependency injection container.

`WpfBlazorApp/Counter.razor` - Razor component containing the Syncfusion `SfCalendar` control with `TValue="DateTime"`.

## Support and Feedback

- For general product questions, visit the [Syncfusion Community Forum](https://www.syncfusion.com/forums) or [Syncfusion Support](https://www.syncfusion.com/support).
- To report an issue specific to this sample, open a GitHub issue in this repository.
- Documentation: https://blazor.syncfusion.com/documentation/getting-started/blazor-web-app

## License

This is a Syncfusion sample project provided to demonstrate product usage. Review the [Syncfusion license terms](https://www.syncfusion.com/sales/pricing?category=ui-components) before using Syncfusion components in your own applications.