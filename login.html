<html>

<head>
  <title>Login Form with Facebook</title>
  <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.6/css/bootstrap.min.css" />
</head>
<style>
  .box {
    width: 100%;
    max-width: 400px;
    background-color: #f9f9f9;
    border: 1px solid #ccc;
    border-radius: 5px;
    padding: 16px;
    margin: 0 auto;
  }
</style>

<body>

  <?php
  require_once 'vendor/autoload.php';  // Composer autoload file for Facebook SDK

  // Facebook app configuration
  $fb = new \Facebook\Facebook([
    'app_id' => '8477653518940727', // Replace with your app ID
    'app_secret' => '359f9e3b5b3b575ba91d9eb462a20f33', // Replace with your app secret
    'default_graph_version' => 'v16.0',
  ]);

  $helper = $fb->getRedirectLoginHelper();
  $redirectURL = 'http://localhost/facebook-login/home.php'; // Replace with your redirect URL

  $permissions = ['email']; // Optional permissions
  $loginUrl = $helper->getLoginUrl($redirectURL, $permissions);

  try {
    if (isset($_GET['state'])) {
      $helper->getPersistentDataHandler()->set('state', $_GET['state']);
    }
    $accessToken = $helper->getAccessToken();

    if (isset($accessToken)) {
      $response = $fb->get('/me?fields=name,email', $accessToken);
      $user = $response->getGraphUser();
      $name = $user['name'];
      $email = $user['email'];
    }
  } catch (\Facebook\Exceptions\FacebookResponseException $e) {
    // When Graph returns an error
    echo 'Graph returned an error: ' . $e->getMessage();
    exit;
  } catch (\Facebook\Exceptions\FacebookSDKException $e) {
    // When validation fails or other local issues
    echo 'Facebook SDK returned an error: ' . $e->getMessage();
    exit;
  }
  ?>

  <?php if (isset($user)) { ?>
    <div class="container">
      <div class="box">
        <div class="form-group">
          <label for="name">Name: <?php echo htmlspecialchars($name); ?></label><br>
          <label for="email">Email: <?php echo htmlspecialchars($email); ?></label>
        </div>
      </div>
    </div>
  <?php } else { ?>
    <div class="container">
      <div class="table-responsive">
        <h3 align="center">Login using Facebook with PHP</h3>
        <div class="box">
          <form method="post">
            <div class="form-group">
              <label for="email">Email</label>
              <input type="text" name="email" id="email" placeholder="Enter Email" class="form-control" required />
            </div>
            <div class="form-group">
              <label for="password">Password</label>
              <input type="password" name="pwd" id="pwd" placeholder="Enter Password" class="form-control" required />
            </div>
            <div class="form-group">
              <input type="submit" id="login" name="login" value="Login" class="btn btn-success form-control" />
            </div>
            <hr>
            <center>
              <a href="<?php echo htmlspecialchars($loginUrl); ?>">F</a>
            </center>
          </form>
        </div>
      </div>
    </div>
  <?php } ?>

</body>

</html>