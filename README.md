[![Tech Space Hub](https://techspacehub.com/wp-content/uploads/2022/06/tech-space-logo-black.svg)](https://techspacehub.com)[![GitHub release](https://techspacehub.com/wp-content/themes/astra-child/assets/images/outer-scripts-version.svg)](https://github.com/tech-space-hub/Outer-Scripts/releases)

## ABOUT

Outer Scripts enables the use of unique external scripts (such as PHP, HTML, JS, and CSS) in Joomla pages. Both inline scripts and external file paths may be added to the same page. When using external scripts on Joomla pages, this plugin seeks to provide users a little more flexibility. A component, module, and sample script are included with this extension.

## Features

1. Inline PHP script.
2. External PHP script.
3. Show PHP script under a menu or in any template position using module.
4. Back-end admin panel to enter unlimited number of inline/external PHP Script.
5. External PHP script supports almost every method used by core Joomla 4 version.
6. An example script has been added under media/com_outerscripts/example-script.php, please follow that one to create yours

## REQUIREMENTS

Every external PHP script should start with _defined('\_JEXEC') or die('This file cannot be accessed directly.');_ at the very first line of your PHP Code.

defined('\_JEXEC') or die('This file cannot be accessed directly.');

We suggest you to add above line so that no one can execute that script outside of Joomla 4 framework.

## Example

<?php
/**
 * @package Outerscripts
 *
 * @copyright (C) 2023 Tech Space Hub.
 * @license GNU General Public License version 3 or later
 */
 
defined('_JEXEC') or die('This file cannot be accessed directly.');

/************* These sample codes can be used to suit your needs and are provided below. ************/

/* Setting Meta Data */
echo 'LOL this is a test';

$document = JFactory::getDocument();
$document->setTitle('Title of Page');
$document->setDescription('this is the description');
$document->setGenerator('My Custom Code');
$document->setMetaData('title', "Your meta title");
$document->setMetaData('keywords', "keyword1,keyword2, etc.");
$document->setMetaData('robots', "index,follow");
$document->setMetaData('author', "Jobin Jose");

/* Regular Joomla Classes Usages */

use Joomla\CMS\Factory;
$user = Factory::getUser();
echo $user->name;

/* Basic Session Access*/

$session = JFactory::getSession();
echo $session->getId();

/* Basic Get Method */

$getparam = JFactory::getApplication()->input->get('urlparam', '', 'string');
echo $getparam;

/* Basic Post Method */

$getemail = JFactory::getApplication()->input->get('email', '', 'string');
echo $getemail;

?>

## Changelog

= 1.0.0 - 26/01/2023 =
Initial Release

## LICENSE

[GNU/GPL Version 3 or later](https://www.gnu.org/licenses/gpl-3.0.html)
