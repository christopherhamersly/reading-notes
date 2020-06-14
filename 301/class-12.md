# EJS Partial

1. Partials come in handy when you want to reuse the same HTML across multiple views. Think of partials as functions, they make large websites easier to maintain as you don’t have to go and change a piece of text in every page it appears in. Instead, you define that reusable bundle of code in a file andinclude it wherever you need it.
  >Under the views/partials/ directory create a file callednavbar.ejs which will contain only the HTML for the navigation bar at the top of the home and post pages:
  > <!-- views/partials/navbar.ejs -->
    < div class="header clearfix">
        < nav>
            < ul class="nav nav-pills pull-right">
                <li role="presentation"><a href="/">Home</a></li>
            < /ul>
            < h3 class="text-muted">Node.js Blog</h3>
        </ nav>
    </ div>
  1. In EJS, any JavaScript or non-HTML syntax you include in your templates is always surrounded by <% %> delimiters (you could change these delimiters if you really wanted to).
  1. Note: The <%- %> tags allow us to output the unescaped content onto the page (notice the -). This is important when using the include() statement since you don’t want EJS to escape your HTML characters like ‘<’, ‘>’, etc…
  1. 

1. Reusable test that stays static.  


  