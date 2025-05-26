# Documentation Rules for Utility CSS Framework

## Layout Properties Documentation Guidelines

When creating documentation for CSS properties in the `layouts` folder, follow these rules to ensure consistency and clarity across all documentation files.

## Prerequisite Research

1. **Review Existing Class Definitions**:

   - **IMPORTANT**: Thoroughly review the entire `classes.md` file before creating or updating any documentation
   - Understand all available utility classes for the property you're documenting
   - Note any special variations, modifiers, or responsive versions of the classes
   - Ensure your documentation covers all implemented utility classes for the property
   - Verify the exact shorthand notation used in the framework

2. **Cross-Reference Related Properties**:
   - Identify related CSS properties that might interact with the one you're documenting
   - Check how these related properties are documented to maintain consistency
   - Consider linking to related property documentation where appropriate

## File Structure and Format

1. Each CSS property should have its own dedicated Markdown file in the `layouts` folder
2. File naming should match the CSS property name with hyphens (e.g., `aspect-ratio.md`, `grid-template-columns.md`)
3. Follow the established documentation pattern:

   ````markdown
   - **Property:** [full-css-property-name]
   - **Shorthand:** [framework-shorthand]  
     [Brief description of what the property does]

   ```css
   [class-example] {
     [css-property]: [value];
   }
   [additional-class-examples...]
   ```
   ````

   **Example:**

   ```html
   [HTML example showing the utility class in use]
   ```

   [Visual example reference or explanation]
   [Additional information if needed]

   ```

   ```

## Visual Examples Requirements

1. **Evaluate Visual Necessity**:

   - Determine if the CSS property has visible effects that benefit from visual demonstration
   - Properties that affect layout, sizing, spacing, or visual appearance generally require images
   - Properties with subtle or print-only effects may use diagrams instead of screenshots

2. **For Properties with Visual Effects**:

   - Create corresponding examples in `index.html` that demonstrate each utility class variation
   - Structure examples to make visual differences between class values immediately apparent
   - Use consistent sample content for visual demonstrations:
     - Images: Use `nha-trang-beaches-1.webp` from the `layouts/img` folder
     - Text: Use lorem ipsum or descriptive text that explains the effect
     - Colors: Use consistent color schemes across examples

3. **Image Creation and Naming**:

   - Take screenshots of rendered examples from a browser
   - Crop images to focus on the relevant visual effect
   - Save images in property-specific subfolders within the `layouts/img` folder:
     - Create a subfolder named after the CSS property (e.g., `layouts/img/aspect-ratio/`)
     - Store all images related to that property in its dedicated subfolder
   - Use consistent naming convention within each property subfolder:
     - For basic utility classes: Use the class name directly (e.g., `arA.png`)
     - For practical examples: Use descriptive names (e.g., `responsive.png`, `card.png`)
     - For comparison examples: Use descriptive prefixes (e.g., `comparison-square-video.png`)
   - Example path: `layouts/img/aspect-ratio/arA.png` for the aspect-ratio property with arA class

4. **Example Structure**:
   - HTML examples should be minimal but complete
   - Include only the code necessary to demonstrate the utility class
   - For complex properties, show multiple variations to demonstrate different values

## Documentation Content Requirements

1. **Property Description**:

   - Begin with a clear, concise description of what the CSS property does
   - Explain when and why a developer would use this property
   - Note any browser compatibility concerns if relevant

2. **Class Examples**:

   - Document all available utility classes for the property
   - Include the CSS output for each class
   - Group related classes together logically

3. **HTML Examples**:

   - Provide practical usage examples that show the utility class in context
   - Examples should be simple enough to understand at a glance
   - Include multiple examples if the property has different use cases

4. **Visual Output**:
   - For each significant example, include a reference to a screenshot showing the result
   - Caption images to explain what aspect of the property is being demonstrated
   - For properties with subtle effects, consider before/after comparisons

## Special Cases

1. **Print-Related Properties** (like `break-after`, `break-before`):

   - Use print preview screenshots to demonstrate pagination effects
   - Consider using diagrams to illustrate concepts that are difficult to capture in screenshots
   - Explain both the visual effect and the functional purpose

2. **Interactive Properties**:

   - For properties that respond to user interaction, consider animated GIFs if appropriate
   - Otherwise, show before/after states with clear labeling

3. **Complex Layout Properties** (like grid or flexbox):
   - Break down examples into simple use cases first, then show more complex applications
   - Use highlighting or annotations to point out key aspects of the layout

## Quality Control Checklist

Before submitting new documentation:

- [ ] Thoroughly reviewed the entire `classes.md` file to understand all available utility classes
- [ ] File follows the established naming convention and structure
- [ ] All utility classes for the property are documented
- [ ] HTML examples are provided for each significant variation
- [ ] Visual examples are included where appropriate
- [ ] Examples use the standard sample content (`nha-trang-beaches-1.webp` for images)
- [ ] Code blocks are properly formatted with correct syntax highlighting
- [ ] Property description is clear and accurate
- [ ] Documentation matches the style and tone of existing files
- [ ] All images are properly saved in the property-specific subfolder within `layouts/img` with correct naming
- [ ] Links to images use relative paths and are correctly formatted
- [ ] Related properties are referenced where appropriate

## Example Documentation Review

Compare your new documentation against existing files like `aspect-ratio.md` and `columns.md` to ensure consistency in:

- Level of detail
- Example complexity
- Visual demonstration approach
- Overall structure and formatting
