---
title: Media Storage
description: Placeholder
---
# Media Storage

Media Storage helps you organize and gain access to media files that are stored on the server. The path to the location of the files is determined by the [Base URL](https://docs.magento.com/user-guide/stores/store-urls.html) configuration. Files in media storage can be accessed from the editor while working on pages and static blocks. Media Storage is usually located in the file system on the same server as the Commerce program files.

Alternatively, media files can be managed in a [database](media-storage-database.md), or located on a separate server or [content delivery network](media-storage-content-delivery-network.md). The advantage of using alternate storage is that it minimizes the effort required to synchronize media when multiple instances of the system that are deployed on different servers that need access to the same images, CSS files, and other media files.

The editor can be configured to use either static or [dynamic media URLs](https://docs.magento.com/user-guide/catalog/catalog-urls-dynamic-media.html) for catalog content in category or product descriptions.

![Commerce Media Storage](./assets/media-storage.png)<!-- zoom -->

## Add files to the Media Storage

The first two steps are the same as if you are inserting an image.

1. On the [editor](editor.md) toolbar, click the _Insert Image_ icon.

   ![Insert Image icon](./assets/editor-toolbar-image-button.png)<!-- zoom -->

   This opens the _Insert/edit image_ dialog.

1. After _Source_, click the _Search_ icon (![Search icon](./assets/media-gallery-icon-browse.png){: width="20px"}).

1. In the directory tree on the left, do one of the following:

   - Navigate to the folder where you want to save the uploaded image.

   - Navigate to the place where you want to create a new folder and click **Create Folder**.

      For adding a new folder, enter the folder name and click **OK**.

1. To add one or more files to Media Storage, you can either upload the files from your system or use the [Adobe Stock Integration](adobe-stock.md):

   - To upload files from your system, click **Choose Files** and do the following:

      - In the directory of your local computer, navigate to the location of the images.

      - Select each image to be uploaded.

      - Click **Open**.

   - To use assets from Adobe Stock using the [integration](adobe-stock.md):

      - Click **Search Adobe Stock**.

      - Add a preview or licensed image from Adobe Stock (see [Using Adobe Stock Images](adobe-stock-manage.md)).

The images are uploaded to the current Media Storage folder on the server.

![Media Storage](./assets/media-storage.png)<!-- zoom -->

## Insert an image from Media Storage

Open the page or block to be edited. Then, use one of the following methods to insert an image from media storage:

### Method 1: WYSIWYG mode

1. On the [editor](editor.md) toolbar, click the _Insert Image_ icon.

1. After _Source_, click the _Search_ icon (![Search icon](./assets/media-gallery-icon-browse.png){: width="20px"}).

   ![Selecting the search icon](./assets/editor-dialog-insert-image.png)<!-- zoom -->

1. In the directory tree on the left, navigate to the folder where the image is stored.

   ![Navigating to the image file](./assets/media-storage-insert-file.png)<!-- zoom -->

1. Select the tile of the image and click **Add Selected**.

### Method 2: HTML mode

1. Position the cursor in the code where the `<img>` tag is to be inserted.

1. Click **Insert Image**.

   ![Insert Image (HTML Mode)](./assets/editor-html-mode-insert-image.png)<!-- zoom -->
