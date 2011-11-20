A Symfony2 bundle for the Redmine class from http://tspycher.com/using-the-redmine-api-with-php/


## INSTALLATION

Add the following entry to ``deps`` the run ``php bin/vendors install``.

    [RedmineBundle]
        git=http://github.com/roderik/RedmineBundle.git
        target=/bundles/RedmineBundle

Register namespace in ``app/autoload.php``

    $loader->registerNamespaces(array(
        // ...
        'Redmine'          => __DIR__.'/../vendor/bundles/RedmineBundle/src',
    ));

## USAGE

    $redmine = new Redmine($config);
    $overdueissues = $redmine->getIssues("?query_id=10");

    More on: http://tspycher.com/using-the-redmine-api-with-php/
