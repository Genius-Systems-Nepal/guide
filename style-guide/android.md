#### A Style Guide
The following are useful tips and conventions for writing descriptions in doc comments.

**. Use 3rd person (descriptive) not 2nd person (prescriptive).**
The description is in 3rd person declarative rather than 2nd person imperative.
>Gets the label. (preferred)
>
>Get the label. (avoid)

**. Method descriptions begin with a verb phrase.**
A method implements an operation, so it usually starts with a verb phrase:
>Gets the label of this button. (preferred)
>
>This method gets the label of this button.

**. Class/interface/field descriptions can omit the subject and simply state the object.**
These API often describe things rather than actions or behaviors:
>A button label. (preferred)
>
>This field is a button label. (avoid)

**. Use "this" instead of "the" when referring to an object created from the current class.**
For example, the description of the getToolkit method should read as follows:
>Gets the toolkit for this component. (preferred)
>
>Gets the toolkit for the component. (avoid)

**. OK to use phrases instead of complete sentences, in the interests of brevity.**
This holds especially in the initial summary and in @param tag descriptions.

**. Use in-line links economically**
It encouraged to add links for API names (listed immediately above) using the {@link} tag. It is not necessary to add links for all API names in a doc comment. Because links call attention to themselves (by their color and underline in HTML, and by their length in source code doc comments), it can make the comments more difficult to read if used profusely. We therefore recommend adding a link to an API name if:
- The user might actually want to click on it for more information (in your judgment), and
- Only for the first occurrence of each API name in the doc comment (don't bother repeating a link)

**. Omit parentheses for the general form of methods and constructors**
When referring to a method or constructor that has multiple forms, and you mean to refer to a specific form, use parentheses and argument types. For example, ArrayList has two add methods: add(Object) and add(int, Object):

The add(int, Object) method adds an item at a specified position in this arraylist.

However, if referring to both forms of the method, omit the parentheses altogether. It is misleading to include empty parentheses, because that would imply a particular form of the method. The intent here is to distinguish the general method from any of its particular forms. Include the word "method" to distinguish it as a method and not a field.
The add method enables you to insert items. (preferred)
The add() method enables you to insert items. (avoid when you mean "all forms" of the add method)

**. Add description beyond the API name.**
The best API names are "self-documenting", meaning they tell you basically what the API does. If the doc comment merely repeats the API name in sentence form, it is not providing more information. For example, if method description uses only the words that appear in the method name, then it is adding nothing at all to what you could infer. The ideal comment goes beyond those words and should always reward you with some bit of information that was not immediately obvious from the API name.

**Avoid** - The description below says nothing beyond what you know from reading the method name. The words "set", "tool", "tip", and "text" are simply repeated in a sentence.

```/**
* Sets the tool tip text.
*
* @param text  the text of the tool tip
*/
public void setToolTipText(String text) {
/**
* Sets the tool tip text.
*
* @param text  the text of the tool tip
*/
public void setToolTipText(String text) {
```
**Preferred** - This description more completely defines what a tool tip is, in the larger context of registering and being displayed in response to the cursor.

```/**
* Registers the text to display in a tool tip.   The text
* displays when the cursor lingers over the component.
*
* @param text  the string to display.  If the text is null,
*              the tool tip is turned off for this component.
*/
public void setToolTipText(String text) {
/**
```


**. Be clear when using the term "field".**
Be aware that the word "field" has two meanings:
- static field, which is another term for "class variable"
- text field, as in the TextField class. Note that this kind of field might be restricted to holding dates, numbers or any text. Alternate names might be "date field" or "number field", as appropriate.

**Avoid Latin**
use "also known as" instead of "aka", use "that is" or "to be specific" instead of "i.e.", use "for example" instead of "e.g.", and use "in other words" or "namely" instead of "viz."