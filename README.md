# UrlLinker

Twig extension of Kwi / UrlLinker (https://bitbucket.org/kwi/urllinker).

## Usage

### With Silex

    use Kwi\TwigUrlLinker;

    $app['twig'] = $app->share($app->extend('twig', function($twig, $app) {

        $twig->addExtension(new TwigUrlLinker());

        return $twig;
    }));

Then, in a template:

    {{ text|UrlLinker|raw }}