####This is an example of solution for adding contextual links to custom block rendered outside Block Layout in Drupal 8 *
This fixes an issue of contextual links are not showing up when a custom block is rendered outside of blocks.

See
https://www.drupal.org/project/drupal/issues/2704331
https://www.drupal.org/project/drupal/issues/2666578

### What you'll find here 
1. A theme hook added within module to provide custom template
2. Implementation of hook_theme_suggestions_HOOK_alter() within module to provide a separate template for each custom block
3. Twig template within theme which will wrap our entity in a container with all required markup 
4. Example of rendering of example block in hook_preprocess_page within theme.

### How to run through 
1. Install block_content_contextual_links module
2. Use an example of rendering of example block presented in hook_preprocess_page
3. Output the rendered_example_block in page.html.twig or other page template
4. Create a template of following name structure block-content-contextual-links-wrap--yourblockname.html.twig (use block-content-contextual-links-wrap.html.twig as a base template structure)
