<img src="lib/images/readme/logo.png" alt="Insoftver"> 
<h1>Atmosfera</h1>
<h3>RubyOnRails simple environment.</h3>
<p>This gem is aimed to help future Insoftver developers to avoid initialization of a RubyOnRails server environment. Its intention is to reduce these tasks to generators. While building it SCRUM Agile Methodology was implemented, so it will be updated on that pace.</p>

<h3>Information</h3>
<p>
	This gem generates a controller called Start and sets its index.html.erb file up as root_path.<br>
	It applies to the Devise gem views the Insoftver CSS layouts.<br>
	It generates a calendar with three different views, month, week, and day, as well as an event planner.<br><br>
	More features will be added.
</p>

<h3>Getting started</h3>
<p>Atmosfera 1.0 works with Rails 6.0 onwards. Add the following line to your Gemfile:</p>

<blockquote>gem 'atmosfera'</blockquote>

<h3>Usage</h3>
<p>
	It is necessary to have a clean Rails project, if possible just created. After installation on the Gemfile some generators can be run, they will be listed and updated on this document.<br>
	<blockquote>rails generate atmosfera:start</blockquote>
	This generator will install the Start controller its views and apply the Insoftver CSS layouts to the Devise views. It sets the root_path to the Start controller index.html.erb file.
	It is necessary to know that we need to have previously installed the Devise gem. Once this last done, Atmosfera creates the following files:<br><br>
	<ul>
	app/assets/images/start
		<br>
		<li>250x250px icon.xcf file with the following exportings.</li>
		<li>favicon.png</li>
		<li>icon_cancel.png</li>
		<li>icon_finished.png</li>
		<li>icon_green_add.png</li>
		<li>icon_green_delete.png</li>
		<li>icon_green_edit.png</li>
		<li>icon_green_email.png</li>
		<li>icon_green_eyeglasses.png</li>
		<li>icon_green_left_arrow.png</li>
		<li>icon_green_menu.png</li>
		<li>icon_green_pause.png</li>
		<li>icon_green_phone.png</li>
		<li>icon_green_play.png</li>
		<li>icon_green_right_arrow.png</li>
		<li>icon_green_search.png</li>
		<li>icon_green_statistics.png</li>
		<li>icon_green_stop.png</li>
		<li>icon_in.png</li>
		<li>icon_ongoing.png</li>
		<li>icon_out.png</li>
		<li>icon_red_pause.png</li>
		<li>icon_red_stop.png</li>
		<br>
		<li>250x250px social.xcf file with the following exportings.</li>
		<li>social_facebook.png</li>
		<li>social_twitter.png</li>
		<li>social_wattsapp.png</li>
		<li>social_youtube.png</li>
		<br>
		<li>1920x1080px landscape_background.xcf file and landscape_background.png</li>
		<li>1920x250px landscape_footer.xcf file and landscape_footer.png</li>
		<li>1920x250px landscape_header.xcf file and landscape_header.png</li>
		<li>250x600px portrait_background.xcf file and portrait_background.png</li>
		<li>250x200px portrait_footer.xcf file and portrait_footer.png</li>
		<li>250x200px portrait_header.xcf file and portrait_header.png</li>
		<li>250x250px logo_250x250_short_name.xcf file and logo_250x250_short_name.png</li>
		<li>250x250px logo_960x1080_short_name.xcf file and logo_250x250_short_name.png</li>
		<li>250x250px no_user_photo.xcf file and no_user_photo.png</li>
		<li>250x250px no_item_photo.xcf file and no_item_photo.png</li>
	</ul>
	<ul>
	app/assets/stylesheets
		<br>
		<li>start.scss - This file contents the CSS Insoftver layout.</li>
	</ul>
	<ul>
	app/controllers
		<br>
		<li>start_controller.rb</li>
	</ul>	
	<ul>
	app/views/start
		<br>
		<li><b>index.html.erb</b> This file will display your starting content, it is aimed to be your landing page.</li>
		<li><b>_menu.html.erb</b> This file is great to display all the different links to your different controllers and views.</li>
		<li><b>_top.html.erb</b> This is the right place to put your header image and company name.</li>
		<li><b>_bottom.html.erb</b> This place may content some footer image and some contact data.</li>
	</ul>
	This generator will modify the app/layouts/application.html.erb file as well in order to customize it to the Insoftver menu format. The layout sketch generated by this tool may look like the following image:<br><br>
	<img src="lib/images/readme/start_sketch.png" alt="Insoftver"><br><br>
	NOTE: It is neccesary to execute the rake routes command on the terminal in order to set the changes done in the routes.rb file.<br><br>
	After installing all the files listed before, the gem will replace the default Devise views with the previously customized. The files will be replaced according to the gem version list below.<br><br>
	<ul>
	app/views/devise/confirmations (V1.0).
		<li>new.html.erb</li><br>
	app/views/devise/mailer (V2.0).
		<li>confirmation_instructions.html.erb</li>
		<li>email_changed.html.erb</li>
		<li>password_change.html.erb</li>
		<li>reset_password_instructions.html.erb</li>
		<li>unlock_instructions.html.erb</li><br>
	app/views/devise/passwords (V2.0).
		<li>edit.html.erb</li>
		<li>new.html.erb</li><br>
	app/views/devise/registrations (V1.0).
		<li>edit.html.erb</li>
		<li>new.html.erb</li><br>
	app/views/devise/sessions (V1.0).
		<li>new.html.erb</li><br>
	app/views/devise/shared (V1.0).
		<li>_error_messages.html.erb</li>
		<li>_links.html.erb</li><br>
	app/views/devise/unlocks (V2.0).
		<li>new.html.erb</li><br>
	</ul>
	Atmosfera will configure the Devise gem internationalization for Spanish Language as well.<br>
	<br>
	<blockquote>rails generate atmosfera:calendar</blockquote>
	This generator will install the Calendar controller its views with the Insoftver CSS layouts. It creates the following files:<br><br>
	<ul>
	On the app/views/calendar/ folder:
		<br>
		<li>start.html.erb</li>
		<li>_month.html.erb</li>
		<li>_week.html.erb</li>
		<li>_day.html.erb</li>
	</ul>
	<ul>
	On the app/assets/stylesheets/ folder:
		<br>
		<li>calendar.scss</li>
	</ul>
	<ul>
	On the app/controllers/ folder:
		<br>
		<li>calendar_controller.rb</li>
	</ul>
	NOTE: It is neccesary to execute the <b>rake routes</b> command on the terminal in order to set the changes done in the routes.rb file.<br><br>	
</p>

<h3>Releases</h3>
<table style="width:100%">
	<tr>
    	<td>1st. Release.</td>
    	<td>
    		<p>
    		Creation of Start controller files.<br>
    		Customization of the <a href="https://github.com/heartcombo/devise">Heartcombo's Devise</a> gem.<br>
    		Creation of the calendar and setup of events.<br>
	    	</p>
    	</td>
  	</tr>
	<tr>
    	<td>2nd. Release.</td>
    	<td>
    		<p>
    		Addition of JQuery routines.<br>
    		Addition of the responsive modules.<br>
    		Setup of the user profile module.<br>
    		</p>
    	</td>
  	</tr>  
</table>