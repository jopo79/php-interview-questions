# WordPress
1. What are the disadvantages of using WP-Cron?
2. What is the purpose of the function `wp_register_script()`?
3. Which of the following will pass variables to the included template file?

	```php
	    a. include(locate_template('templates/partials/author.php'));
	    b. get_template_part('templates/partials', 'author.php');
	    c. include(get_template_part('templates/partials', 'author.php'));
	    d. locate_template('templates/partials/author.php');
	```
4. How can you protect WordPress from a brute force attack?
5. What is the `Walker` class used for?
6. Explain what hooks are and give two examples of how they might be used.
7. How do you create a static home page?
8. Explain what the following code does:

	```php
		remove_filter( 'the_content', 'wpautop' );
		remove_filter( 'the_excerpt', 'wpautop' );
	```
9. You've registered a new post type, named `books`, however when you visit http://yoursite.com/books you are redirected to the homepage. What steps would you take to troubleshoot this issue?
10. When should WordPress nonces be used?
11. Name 3 methods of data sanitization available in WordPress and what each of them do. For example, `sanitize_email()` strips out all characters that are not allowable in an email address
12. Explain the Transients API.
13. What does the following line of code do?

	```php
		add_action( 'wp_ajax_nopriv_send_email', 'send_email' );
	```
14. What might the following code be used for?

	```php
		function register_query_vars( $vars ) {
			$vars[] = 'photos';
			$vars[] = 'files';
			return $vars;
		}
		add_filter( 'query_vars', 'register_query_vars' );
	```
15. What does the function `wp_parse_args()` do?


# PHP
1. What is an autoloader and what does it do?
2. After the code below is run, what are the values of `$a` and `$b`?

	```php
	    $a = '5';
	    $b = &$a;
	    $b = "2$b";
	```
3. Name 2 ways to sort an array and explain what they do. For example, `sort()` arranges array elements from lowest to highest.
4. What’s the difference between functions `include()` and `require()`?
5. What are the `__construct()` and `__destruct()` methods in a PHP class?
6. How can you determine the number of items in an array?
7. What are two advantages of using namespaces?
8. What are the 3 scope levels available in PHP and how would you define them?
9. What are getters and setters and why are they important?
10. Explain the difference between `===` and `==`.
11. What is meant by dependency injection?
12. Looking at the code below, what will the function `getTemplateName()` return?

	```php
	class Template
	{
	    protected $template_name;

	    public function __construct()
	    {
		$this->template_name = 'innovation_card';
	    }

	    public static function getTemplateName()
	    {
		return $this->template_name;
	    }
	}
	```
13. Name 3 ways to protect against SQL injection?
14. What is the difference between $_GET and $_POST
15. What are some magic methods in PHP? How might they be used?
16. Briefly explain one or both of the following design patterns:
	- Singleton
	- Factory
17. What is cURL extention used for?
18. What is a Closure?
19. Explain, line by line, what the following code does. Can it be improved? If so, how?

	```php
	function inline_tweet($content, $options)
	{
	    $url = get_url();
	    $content = trim($content);
	    $tweet = strlen($content) > 140 ? substr($content, 0, 140 - (strlen($url)) : $content;

	    return sprintf(
		'<span class="%1$s"><a href="https://twitter.com/intent/tweet?text=%2$s&url=%3$s&via=%4$s" target="_blank">%5$s</a></span>',
		$options['class'],
		urlencode($tweet),
		urlencode($url),
		'trendwatching',
		$content
	    );
	}
	```
20. Write your name below this line, commit your changes and push your branch to the remote repository:
