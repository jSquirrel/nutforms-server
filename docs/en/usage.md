# Nutforms Server Usage Documentation

Usage of Nutforms Server intergared with Nutforms
Web Client is demonstrated in [Nutforms Example](https://github.com/jSquirrel/nutforms-example).

## Using Adaptive RESTful API

The recommended usage is with [Adaptive RESTful API](https://github.com/jSquirrel/adaptive-restful-api),
which provides its own example and installation information.

## Registering servlets

Once you installed Adaptive RESTful API, you need to register the servlets
in your `WEB-INF/web.xml`.

```xml
<servlet>
    <servlet-name>MetadataServlet</servlet-name>
    <servlet-class>cz.cvut.fel.nutforms.meta.MetadataServlet</servlet-class>
</servlet>
<servlet>
    <servlet-name>LayoutServlet</servlet-name>
    <servlet-class>cz.cvut.fel.nutforms.layout.LayoutServlet</servlet-class>
</servlet>
<servlet>
    <servlet-name>LocalizationServlet</servlet-name>
    <servlet-class>cz.cvut.fel.nutforms.localization.LocalizationServlet</servlet-class>
</servlet>
<servlet>
    <servlet-name>RuleServlet</servlet-name>
    <servlet-class>cz.cvut.fel.nutforms.rules.servlet.RuleServlet</servlet-class>
</servlet>
<servlet>
    <servlet-name>WidgetServlet</servlet-name>
    <servlet-class>cz.cvut.fel.nutforms.widget.WidgetServlet</servlet-class>
</servlet>
<servlet>
    <servlet-name>WidgetMappingServlet</servlet-name>
    <servlet-class>cz.cvut.fel.nutforms.widget.WidgetMappingServlet</servlet-class>
</servlet>

<servlet-mapping>
    <servlet-name>MetadataServlet</servlet-name>
    <url-pattern>/meta/*</url-pattern>
</servlet-mapping>
<servlet-mapping>
    <servlet-name>LayoutServlet</servlet-name>
    <url-pattern>/layout/*</url-pattern>
</servlet-mapping>
<servlet-mapping>
    <servlet-name>LocalizationServlet</servlet-name>
    <url-pattern>/localization/*</url-pattern>
</servlet-mapping>
<servlet-mapping>
    <servlet-name>RuleServlet</servlet-name>
    <url-pattern>/rules/*</url-pattern>
</servlet-mapping>
<servlet-mapping>
    <servlet-name>WidgetServlet</servlet-name>
    <url-pattern>/widget/*</url-pattern>
</servlet-mapping>
<servlet-mapping>
    <servlet-name>WidgetMappingServlet</servlet-name>
    <url-pattern>/widget-mapping/*</url-pattern>
</servlet-mapping>
```

See [more detailed example](https://github.com/jSquirrel/nutforms-example/blob/master/src/main/webapp/WEB-INF/web.xml).

## Defining aspects

Finally, you can define your aspects in your `resources` folder.

### Layouts

Layouts are stored in `HTML` files in `resources/layout` folder
separated into sub-folders by namespace.
If name of the layout is `<namespace>/<layout-identifier>`,
then it is stored in `resources/layout/<namespace>/<layout-identifier>.html`.

See [more detailed example](https://github.com/jSquirrel/nutforms-example/tree/master/src/main/resources/layout).

### Widgets & Widget

Widgets are stored in `HTML` files in `resources/widget` folder
separated into sub-folders by namespace.
If name of the widget is `<namespace>/<widget-identifier>`,
then it is stored in `resources/widget/<namespace>/<widget-identifier>.html`.

See [more detailed example](https://github.com/jSquirrel/nutforms-example/tree/master/src/main/resources/widget).

### Widget Mapping function

Widget mapping function is saved in `resources/widget/mapping/function.js`.

See [more detailed example](https://github.com/jSquirrel/nutforms-example/tree/master/src/main/resources/widget/mapping).

### Localization

Localization is stored in `properties` files in the root `/resources` directory
and are named `FormBundle[_<locale>].properties`.
You can leave out the locale identifier for default
localization of forms.

See [more detailed example](https://github.com/jSquirrel/nutforms-example/tree/master/src/main/resources/FormBundle.properties).
