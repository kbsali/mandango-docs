Security
========

The *MandangoBundle* comes with a *MandangoUserProvider* provider which allows you to integrate your *Mandango* documents to the security layer of Symfony2.

.. code-block:: yaml

    # app/config/security.yml
    services:
        security.provider.mandango:
            class: Mandango\MandangoBundle\Security\MandangoUserProvider
            arguments: [@mandango, Model\User, username]

    security:
        providers:
            mandango:
                id: security.provider.mandango
