# Plivo pre-bundled php library
This is a pre-bundled version of the [plivo php](https://github.com/plivo/plivo-php) library comes packaged with all the dependencies ready to go out of the box this was original modified to work with the [SMS Plivo](https://www.drupal.org/project/sms_plivo). Drupal module but can be used in any php project.

### Run in Drupal
Follow instructions on module page [SMS Plivo](https://www.drupal.org/project/sms_plivo).

### Run in any other php project
`<?php
require_once ''/plivo/plivo-php/plivo.php';
  $p = new RestAPI($auth_id, $auth_token);
  //Send a message
  $params = array(
        'src' => $number, // Sender's Alphanumeric ID
        'dst' => $mobile_number, // Receiver's phone number with country ode
        'text' => message // Your SMS text message
    );
    $response = $p->send_message($params);`
