# Video Editor Bundle

Bundle based on [Symfony](http://symfony.com/) to work with the [PuMuKIT Video Platform](https://github.com/campusdomar/PuMuKIT2/blob/2.3.x/README.md).

This bundle provides a basic mono-stream video editor. Useful to create new multimedia objects from hard trimming operations.

## Installation

Step 1 requires you to have Composer installed globally, as explained
in the [installation chapter](https://getcomposer.org/doc/00-intro.md)
of the Composer documentation.


### Step 1: Download the Bundle

Open a command console, enter your project directory and execute the
following command to download the latest stable version of this bundle:

```bash
$ composer require teltek/pumukit-hard-video-editor-bundle
```

### Step 2: Install the Bundle

Install the bundle by executing the following line command. This command updates the Kernel to enable the bundle (app/AppKernel.php) and loads the routing (app/config/routing.yml) to add the bundle routes.

```bash
$ php app/console pumukit:install:bundle Pumukit/HardVideoEditorBundle/PumukitHardVideoEditorBundle
```

### Step 3: Update assets

```bash
$ php app/console cache:clear
$ php app/console cache:clear --env=prod
$ php app/console assets:install
```


### Step 4: Configure your default role

After install the bundle you can configure the role that you want use when uses hard trimming. To change it you should add to your parameters.yml these 
configuration:

```
pumukit_hard_video_editor:
    default_set_role: Participant
```

Change "Participant" by the role that you want.