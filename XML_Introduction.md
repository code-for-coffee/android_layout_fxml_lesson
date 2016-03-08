# What is XML?

**XML** stands for *extensible markup language*. It is the base schema that is used by HTML, so you may already be familiar with XML.

### XML Tags

XML contains **tags**. These are defined as something of importance. When it comes to Android, **tags** can be *various user interface components* such as a `TextView` (which is an element that renders text on the phone). A tag could look like `<someTag>`. Notice the starting `<` and closing `>`. These define our tags by wrapping around them.

Each *tag* contains a **start** and an **end** tag. Alternatively, some tags may be **abbreviated** (also known as self-closing). Let's take a look at what those look like:

A TextView that contains a *start* and *end* tag:
```xml
<TextView></TextView>
```

A TextView that is self-closing:

```xml
<TextView />
```

Let's consider a **Button**:

```xml
<Button></Button>
```

```xml
<Button />
```

#### Checking for Understanding

* Each XML tag must be *wrapped* with special characters. What are they?
* What is the primary difference between these two types of **XML Tags**?
* Which of these two types appears easier (or more convenient) to write?

### Elements

XML is defined by a series of **elements**. These are just *tags* with definition. For example, we could define a basic Android layout using **elements**. A basic Android *Layout* requires a Layout *element* (in this case, we are using *RelativeLayout*).

```xml
<?xml version="1.0" encoding="utf-8"?>
<RelativeLayout>
</RelativeLayout>
```

#### Nested Elements

This layout will then contain a *TextView* element that will show the user `Hello World!` when the app has loaded. The *TextView* element is **nested** inside of the *parent* element - our `<RelativeLayout>`.

```xml
<?xml version="1.0" encoding="utf-8"?>
<RelativeLayout>
    <TextView android:text="Hello World!" />
</RelativeLayout>
```

Naturally, XML could also be used to nest any sort of objects:

```xml
<Book>
  <Chapter>1</Chapter>
  <Quote>Inspirational quote goes here.</Quote>
  <Content>...</Content>
</Book>
```

#### Attributes

You'll notice that our *TextView* has a property - or **attribute** of `android:text`. It has an **associated value** of `Hello World!`. XML elements may contain multiple tags that describe themselves. Think of them as *objects* that contains *attributes* and possibly even *abilities*.

If we want to force our *TextView* to be wrapped horizontally in our app (so forced to display content from one side to the other), we can add a new attribute - **android:layout_width**. It would have an *associated value** of `wrap_content`.

```xml
<TextView
    android:layout_width="wrap_content"
    android:text="Hello World!" />
```

What if we want it to cover content from top to bottom as well? We could add another *xml attribute* - **android:layout_height**. It would have an *associated value** of `wrap_content`.

```xml
<TextView
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"
    android:text="Hello World!" />
```

##### Checking for Understanding

Can you identify the following in the XML file below?

- Each individual XML *tags* and how they are closed.
- Each *element* and what they may do (feel free to look them up online).
- How each element is *nested* and what this may implicate?
- The various *attributes* of each element?

```xml
<Button
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"
    android:text="Click me for things to happen"
    android:id="@+id/button"
    android:layout_alignParentTop="true"
    android:layout_alignParentStart="true" />
```
