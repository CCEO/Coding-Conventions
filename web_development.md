Web Development 
Files Conventions

  	File names must be named in English

Code Conventions

    -  Lines SHOULD be 80 characters or less.
    -  If a line of code contains more than 80 characters, it must be partitioned into two lines or more, always starting with a tab
    -  There MUST be one blank line after the namespace declaration, and there MUST be one blank line after the block of use declarations.
    -  There MUST be one blanck line after the <?php declaration, and there MUST be one blank line after the imports
    -  Opening braces for classes MUST go on the next line and closing braces MUST go on the next line after the body.
    -  Opening braces for methods MUST go on the next line and closing braces MUST go on the next line after the body.
    -  The content of a function MUST contain 20 lines of code or less
    -  Visibility MUST be declared on all properties and methods; abstract and final MUST be declared before the visibility; static MUST be declared after the visibility.
    -  Control structure keywords MUST have one space after them; method and function calls MUST NOT.
    -  Opening braces for control structures MUST go on the same line and closing braces MUST go on the next line after the body.
    -  The control structures MUST NOT have braces if the body content is just one line
    -  Opening parentheses for control structures MUST NOT have a space after them and closing parentheses for control structures MUST NOT have a space before.
    -  When matching a variable, there must be a space between each element that contains
                      $variable = $loquesea + $otroloquesea;
Laravel Naming Conventions
 
   Routes
	 
	 -	Routes must be named in plural and lowercase
                         Good	       Bad
                     articles/1	   article/1

    -	The named route must be in snake_case with dot notation
                      Good	                     Bad
               Users.show_active    	Users.show-active,show active-users

   Controllers, Methods

    -	Controller must be named in singular
                       Good	              Bad
                ArticleController	   ArticlesController

    -	The models must be named in singular
                       Good	                       Bad
                  Users.show_active	  Users.show-active,show active-users

    -	Model properties must be named in snake_case
                        Good	                 Bad
                 $model->created_at	       $model->createAt

    -	Migration
                         Good	                                   Bad
          2017_01_01_000000_create_articles_table	    2017_01_01_000000_articles

    -	The methods must be named in camelCase
                         Good          	Bad
                        getAll	       get_all

    -	The methods in resource controller are
                         Good	                                  Bad
        Index, create, store, show, edit, update, delete	    saveArticle

    -	The methods in test class must be named in camelCase
                         Good	                                  Bad
                testGuestCannotSeeArticle	           test_guest_cannot_see_article

  Data Base

    -	The relationships hasOne or belongsTo must be named in singular
                         Good	                           Bad
                    articleComment	         articleComments, article_comment

     -	All the other relationships must be named in plural
                         Good	                            Bad
                   articleComments	        articleComment, article_comments

     -	The name of a table must be in plural
                          Good                            Bad
                     article_comments	              articleComments

    -	The Pivot table must me named in singular model names and alphabetical order
                          Good                           	Bad
                       article_user         	User_article, articles_users

    -	Table columns must be named in snake_case without the model name
                          Good	                           Bad
                        meta_title	           MetaTitle; article_meta_title

    -	The foreign keys must include the model name in singular with_id suffix
                          Good	                           Bad
                        article_id	       Article, id_article, articles_id

    -	Primary keys 
                          Good	                            Bad
                           id	                           custom_id
Files

    -	The Config file and language index must be in snake_case
                          Good	                            Bad
                     Articles_enabled     	ArticlesEnabled; articles enabled

    -	The views must be named in snake_case
                          Good	                             Bad
                show_filtered.blade.php	     showFiltered.blade.php, show-filtered.blade.php

    -	The files of the folder config must be named in snake_case 
                          Good	                              Bad
                    google_calendar.php	         googleCalendar.php, google-calendar.php

    -	The contract (interface) must be written in adjective or noun
                           Good	                               Bad
                      Authenticatable	       AuthenticationInterface, Authentication

    -	The traits must be written in adjective
                           Good                                	Bad
                         Notifiable	                      NotificationTrait

  Code

    -	A collection must be descriptive and named in plural
                        Good	                                  Bad
            $activeUsers = User::active()->get()	        $active, $data

     -	A object must be descriptive and named in singular
                        Good                                   	Bad
              $activeUser = User::active()->first()       	$users, $obj

    -	The variables must be named in camelCase
                        Good	                                  Bad
                 $articlesWithAuthor                	$articles_with_author

    -	The code comments should contain a brief description of the function
                         /**
                         * Breve descripción de la función
                         *
                         * @param  \Illuminate\Http\Request  $request  	← Parametros
                         * @param  int  $id
                         * @return \Illuminate\Http\Response 			← Retorno
                         * 
                         * En caso de ser necesario describir de forma más detalla la función
                         *
                         * @author Nombre
                         */
												 
Folders
  
  	-	Folders must be named in snake_case
              Good	        Bad
           users_new	   usersnew

    -	Create a folder for each singular role
    -	One folder for each controller
    -	Create a partial folder at the height in which it will be used, that is, you can have many partial folders (local and global).
                                    Good	                  Bad
                   |-- partials                          |-- users
                   |-- users                             |-- partials
                     |-- users                             |-- users
                       |-- partials                          |-- partials
                       |-- create.blade.php                  |-- create.blade.php
                       |-- edit.blade.php                    |-- edit.blade.php
                       |-- index.blade.php                   |-- index.blade.php
                  |-- departments                        |-- departments 
                     |-- users                             |-- users     
                       |-- partials                          |-- partials
                       |-- create.blade.php                  |-- create.blade.php
                       |-- edit.blade.php                    |-- edit.blade.php
                       |-- index.blade.php                   |-- index.blade.php
	

-	For assets create a folder for each type of files within public, css, js, fonts, img

ESLint for VUE

For Vue.js we will use an add-on called ESLint, which allows us to verify the template and scripting of .vue files to find:

   -	Syntax errors
   -	Incorrect use of Vue.js Directives
   -	Violations of Vue.js Style Guide

You can find the Plug-in by following the link   https://github.com/vuejs/eslint-plugin-vue  
And the installation manual  ( https://eslint.vuejs.org/user-guide/#installation ) so you can start working with this incredible tool and get a higher quality code

											


