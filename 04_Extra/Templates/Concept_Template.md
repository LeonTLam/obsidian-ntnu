<%*
const hasTitle = !tp.file.title.startsWith("Untitled");
let title;
if (!hasTitle) {
	title = await tp.system.prompt("Give the concept a Title");
	await tp.file.rename(title);
} else {
	title = tp.file.title;
}
_%>
# <% await tp.file.title %>
## Definition:
- Brief definition or description.

## Key Details:
- Point 1
- Point 2

## Examples:
1. Example 1.
2. Example 2.

## References:
- [Source 1](link)
- [Source 2](link)