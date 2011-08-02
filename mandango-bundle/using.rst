Usage
=====

You can now use *Mandango* in a *normal way*.

You can access the *mandango* object through the container::

    # app/config/mandango/schema.yml
    $mandango = $this->get('mandango');

But *mandango* can also beinitialized automatically -in a lazy way ::

    # src/Mandango/MandangoUserBundle/Controller/MandangoUserController.php

    // create a document
    $article = $mandango->create('Model\Article');
    $article->setTitle($title);
    $article->save();

    // query a repository
    $articles = $mandango->getRepository('Model\Article')->createQuery();

    // ...
