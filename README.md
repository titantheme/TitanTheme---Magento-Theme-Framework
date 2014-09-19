TitanTheme - Magento Theme Framework
=====================================

Titan Framework (or T2 Framework) is a Magento Theme Framework , an easy way to make Magento theme with many cool features was developed based on Bootstrap library (both frontend and backend), open for every Magento developer.  
You will get a tool with many settings options for your magento theme, transforming the layout, add/edit the Add-on from the Add-ons library. It will also available in a basic configuration to improve depending on the design. 

Magento developers can develop Add-on block to add to our library.  We are hard working to improve this theme framework for the community, and we will gladly cooperate with any designer / developer who wants to develop a template library and change the configuration to make your template so special with customers.

Functional API
------------------------------------------------------------------------------------------
==============================General Tab==============================

Frontend file path: frontend/t2-frame/default/template/titan/container/general.phtml


- Get start with GeneralInfo():
$t2 = new MST_Titan_Block_Main();
$generalInfo = $t2->getGeneralInfo();

+ Get Theme Layout: 
<?php 
echo $generalInfo["theme_layout"]; 
//return one of values {fullwidth,t2-boxed,t2-boxed-medium,..}
?>

+ Get Theme Style: 
<?php 
echo $generalInfo['theme_style'];  
//return one of values {style1,style2,style3,..}
?>
Note: Add Theme Style: add new value from line 23 in frontend/t2-frame/default/template/titan/container/general.phtml

+ Get Enable Top Bar: 
<?php 
echo $generalInfo['enable_top_bar']; 
//return true/false
?>

+ Get Enable Setting Box: 
<?php 
echo $generalInfo['enable_setting_block']; 
//return true/false
?>

+ Get Logo information: 

++ Logo Type: 
<?php 
echo $generalInfo['logo_type'];
//return one of values {1,2,3}. 1: Logo image; 2: logo text; 3: Default Magento Setting;
?>

++ Logo Image: 
<?php 
echo $generalInfo['logo_image'];
//return file name value. example 1410631206.png
?>

++ Logo Text: 
<?php 
echo $generalInfo['logo_text'];
//return input text value
?>

++ Slogan: 
<?php 
echo $generalInfo['slogan']; 
//return input text value
?>

==============================Layout Tab==============================

Frontend file path: frontend/t2-frame/default/template/titan/container/layout.phtml

See Layout Wizard Action 

==============================Pages Option tab==============================

Frontend file path: frontend/t2-frame/default/template/titan/container/page_options.phtml


- Get start:
<?php 
$t2 = new MST_Titan_Block_Main();
$options = $t2->getPageOption();
?>

---------------------------------------------
1. Category Page Options:
---------------------------------------------

- Get Show sub categories value: 
<?php echo $options['category']['show_sub_categories']; 
//return true/false
?>

- Get 'How many items per row' value: 
<?php 
echo $options['category']['item_per_row']; 
//return a number
?>

- Get 'Item image WIDTH' value: 
<?php 
echo $options['category']['image_width']; 
//return a number
?>

- Get 'Item image HEIGHT' value: 
<?php 
echo $options['category']['image_height']; 
//return a number
?>
 
---------------------------------------------
2. Product Details Page options:
---------------------------------------------

- Get Media Layout value: 
<?php 
echo $options['product']['media'];
//return one of values {1,2,3,4}
?>

- Get Main image WIDTH value: 
<?php 
echo $options['product']['image_width'];
//return a number
?>

- Get Main image HEIGHT value: 
<?php 
echo $options['product']['image_height']; 
//return a number
?>

- Get Thumbnail image WIDTH value: 
<?php 
echo $options['product']['thumb_image_width']; 
//return a number
?>

- Get Thumbnail image HEIGHT value: 
<?php 
echo $options['product']['thumb_image_height']; 
//return a number
?>

- Get Keep Frame value: 
<?php 
echo $options['product']['keep_frame']; 
//return true/false
?>

- Get Enable Thumbnail Slider value: 
<?php 
echo $options['product']['thumb_slider']; 
//return true/false
?

- Get Zooming Type value: 
<?php 
echo $options['product']['thumb_slider']; 
//return one of values {inner,popup,lightbox,..}
?>

- Get Product Informations Format value: 
<?php 
echo $options['product']['productinfo']; 
//return one of values {tabs,listview,accordion,..}
?>
 
---------------------------------------------
3. Shopping Cart Page options:
---------------------------------------------

- Get Shopping Cart Layout value: 
<?php 
echo $options['cart']['layout']; 
//return one of values {standard,advanced1,advanced2,..}
?>

- Show 'Estimate Shipping and Tax': 
<?php 
echo $options['cart']['enable_estimate']; 
//return true/false
?>

---------------------------------------------
4. Default Checkout Page options:
---------------------------------------------

- Get Checkout Layout value: 
<?php 
echo $options['checkout']['layout']; 
//return one of values {standard,tab,..}
?>

 
---------------------------------------------
5. My Account Page options:
---------------------------------------------

- Get Checkout Layout value: 
<?php 
echo $options['checkout']['layout']; 
//return one of values {standard,tab,..}
?>
 
---------------------------------------------
6. Contact Us Page options:
---------------------------------------------

- Get Checkout Layout value: 
<?php 
echo $options['checkout']['layout']; 
//return one of values {standard,tab,..}
?>

 
==============================Navigation tab==============================

Frontend file path: frontend/t2-frame/default/template/titan/container/navigation.phtml


- Get start:
<?php 
$t2 = new MST_Titan_Block_Main();
$navigationConfig = $t2->getNavigationConfig();
?>

+ Get Navigation Type: 
<?php 
echo $navigationConfig['menu_type']; 
//return one of values {default,mcp}
?>

+ Get Menu Group if Navigation Type is MCP enabled:
<?php 
echo $navigationConfig['menu_group']; 
//return number (group id)
?>

+ Get Navigation Custom Class:
<?php 
echo $navigationConfig['custom_class']; 
//return input text  value
?>


==============================Customization tab==============================

Frontend file path: frontend/t2-frame/default/template/titan/container/customization.phtml


- Get start:
<?php 
$t2 = new MST_Titan_Block_Main();
$customization = $t2->getCustomizationConfig();
?>

+ Get After <Head> content: 
<?php 
echo $customization['after_head_open']; 
//return textarea value
?>

+ Get Before <Head> content:
<?php 
echo $customization['before_head_close']; 
//return textarea value
?>

+ Get After <Body> content:
<?php 
echo $customization['after_body_open']; 
//return textarea value
?>

+ Get Before </Body> content: 
<?php 
echo $customization['before_body_close']; 
//return textarea value
?>



