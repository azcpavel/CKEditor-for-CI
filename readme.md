```
This is a extend copy of ckeditor for codeigniter
Modified by Pavel
Email:  azc.pavel@gmail.com
Date:   2014-02-05
Mobile: +8801677533818

Extract & Put ckeditor folder in your js folder [you can change the dir from helper file]

Put the helper file in to application/helpers

load the helper from autoload application/config/autoload.php
$autoload['helper'] = array('url', 'file','form','ckeditor'); /*only 'ckeditor' is needed you can skip others*/

or 

you can load it using 
$this->load->helper('ckeditor');



in view page just call set_ckeditor() after the element for load with all options
Example:
	<input type="text" id='ckeditor'>
	<?php set_ckeditor();?> <!--Default id is ckeditor-->




if you want to customize call with customize parameters 
set_ckeditor(String Id, String Width, String Height, String Option, Array (String Skin Name, String Body Color), Array (Array Toolbar));

Example
	<input type="text" id='test'>
	<?php set_ckeditor('test');?> <!--If you have custome id-->
					or
	<?php set_ckeditor('test','500px');?> <!--If you want to change only width-->
					or
	<?php set_ckeditor('test','500px','100px');?> <!--If you want to change only width and height-->
					or
	<?php set_ckeditor('test','50%','10%','Fixed');?> <!--If you want to show only some toolbar-->
					or
	<?php set_ckeditor('test','50%','10%','FUll',array('moonocolor',''));?> <!--If you want show full toolbar with custom skin-->
					or
	<?php set_ckeditor('test','50%','10%','Full',array('','#AA1189'));?> <!--If you want show full toolbar with custom body color-->
					or
	<?php set_ckeditor('test','50%','10%','Fixed',array('',''),array(array('Smiley')));?> <!--If you want show Fixed toolbar-->





Note: you have to provide all the previous value for customize options
Example
	<?php set_ckeditor('','','100px');?> 
	<!--You have to pass the id,width with '' if you want to change the height only -->

Note: '' mean default value for customize options


	

List of Toolbars
[
	{ name: 'document', items : [ 'Source','-','Save','NewPage','DocProps','Preview','Print','-','Templates' ] },
	{ name: 'clipboard', items : [ 'Cut','Copy','Paste','PasteText','PasteFromWord','-','Undo','Redo' ] },
	{ name: 'editing', items : [ 'Find','Replace','-','SelectAll','-','SpellChecker', 'Scayt' ] },
	{ name: 'forms', items : [ 'Form', 'Checkbox', 'Radio', 'TextField', 'Textarea', 'Select', 'Button', 'ImageButton', 
        'HiddenField' ] },
	'/',
	{ name: 'basicstyles', items : [ 'Bold','Italic','Underline','Strike','Subscript','Superscript','-','RemoveFormat' ] },
	{ name: 'paragraph', items : [ 'NumberedList','BulletedList','-','Outdent','Indent','-','Blockquote','CreateDiv',
	'-','JustifyLeft','JustifyCenter','JustifyRight','JustifyBlock','-','BidiLtr','BidiRtl' ] },
	{ name: 'links', items : [ 'Link','Unlink','Anchor' ] },
	{ name: 'insert', items : [ 'Image','Flash','Table','HorizontalRule','Smiley','SpecialChar','PageBreak','Iframe' ] },
	'/',
	{ name: 'styles', items : [ 'Styles','Format','Font','FontSize' ] },
	{ name: 'colors', items : [ 'TextColor','BGColor' ] },
	{ name: 'tools', items : [ 'Maximize', 'ShowBlocks','-','About' ] }
];	
```
