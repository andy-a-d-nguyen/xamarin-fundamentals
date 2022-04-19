# Xamarin

- [Xamarin](#xamarin)
  - [Pages](#pages)
  - [Layouts](#layouts)
  - [Views](#views)
  - [Xamarin.Forms Visual Components](#xamarinforms-visual-components)
  - [Xamarin.Forms Tooling](#xamarinforms-tooling)
  - [DependencyService Class](#dependencyservice-class)
  - [Xamarin.Forms Shell](#xamarinforms-shell)
  - [Xamarin.Forms Project Layout](#xamarinforms-project-layout)
  - [Data Binding](#data-binding)
    - [Binding to Data Values](#binding-to-data-values)
    - [Binding Context](#binding-context)
  - [Model-View-ViewModel (MVVM)](#model-view-viewmodel-mvvm)
    - [MVVM with Xamarin.Forms](#mvvm-with-xamarinforms)

## Pages

- Represent a screen
- Generally occupies the entire screen
- Native Mapping
  - iOS is a ViewController
  - Android is like an Activity (not specifically mapped to Android Activities)
- Types:
  - ContentPage
  - MasterDetailPage
  - NavigationPage
  - TabbedPage
  - CarouselPage
  - TemplatedPage
- Each page represented by two files
  - XAML file describes the UI
    - XAML file leverages XML namespaces
      - Xamarin.Forms normally default
    - Enable C# access to XAML content
      - Include the Name attribute
      - Part of Microsoft XAML namespace
      - Uses x namespace prefix by default
  - C# file provides functionality

## Layouts

- Size and position screen content
- Can be nested
- Children to Pages
- Specialized views that act as containers
- Types:
  - StackLayout and FlexLayout
    - Arrange in horizontal/vertical line
  - Grid
    - Arrange in rows and columns
  - AbsoluteLayout
    - Arrange using absolute values/ratios
  - RelativeLayout
    - Arrange relative to parent or siblings
  - ScrollView

## Views

- Represent page content
- User-interface objects within Layouts
- Native Mapping
  - iOS maps to UIView
  - Android maps to Widgets
- Categories:
  - Presentation (labels, images, etc.)
  - Initiate Commands (buttons, etc.)
  - Setting Values (checkbox, etc)
  - Editing Text (text fields, etc)
  - Display Collections (lists, etc)
  - Indicate Activity (progress bars, etc)

## Xamarin.Forms Visual Components

- Platform Specifics: Allows you to declare functionality that is only available on a specific platform
- Shell: Reduces the complexity of mobile application development by providing the fundamental features that most applications require
- Material Visual: Apply Material Design rules to Xamarin.Forms applications

## Xamarin.Forms Tooling

- Previewer: Shows you how your Xamarin.Forms XAML page will look on iOS and Android
- Toolbox: Lists the available Xamarin.Forms controls and allows you to drag them directly onto the XAML editing surface
- Hot Reload: When saving your XAML file the changes are reflected live in your running app
- Hot Restart: Make and debug changes to your app using a much faster build and deploy cycle

## DependencyService Class

- A service locator that enables Xamarin.Forms applications to invoke native platform functionality from shared code

## Xamarin.Forms Shell

- Reduces the complexity of mobile application development by providing the fundamental features that most mobile applications require

## Xamarin.Forms Project Layout

- Logical Application
  - Abstracts platform details
  - Starting point for Xamarin.Forms experience
- Native Application
  - Initializes environment
  - Quickly hands-off to logical app
  - Can be used to provide platform-specific behavior
- Application Root Page
  - Initial display page
- Toolbars
  - Use page's ToolbarItems property
- Toolbar Items
  - Added with ToolbarItem element

## Data Binding

- Connects a target to a data source
- Target: consumes data from source (Page classes, View classes)
- Specifying source: Use target's BindingContext property

### Binding to Data Values

- Source data: Public properties visible
- Accessing from XAML: Use Binding extension
- Binding mode: Controls binding direction

### Binding Context

- Commonly set only on page
- Child views inherit parent's BindingContext
- Views can set separately if desired

## Model-View-ViewModel (MVVM)

- Decouples data from presentation
- Presentation and data unaware of the other's details
- Adds an intermediary (presentation-friendly layer over data) known as the ViewModel

### MVVM with Xamarin.Forms

- ViewModel classes: Provides presentation-friendly layer over data
- BaseViewModel class: Serves as base to ViewModel classes
- Xamarin.Forms services: Framework features that handle common management and interaction tasks
