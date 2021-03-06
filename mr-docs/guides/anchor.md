---
author: Mamaylya
description: Learn about anchoring holograms in Dynamics 365 Guides and how to create a printed anchor or digital anchor.
ms.author: mamaylya
ms.date: 01/28/2020
ms.service: crm-online
ms.topic: article
title: Choose an anchoring method for your guide in Dynamics 365 Guides
ms.reviewer: v-brycho
---

# Anchor your guide to the real world in the Dynamics 365 Guides PC app

When you create a guide with the [!include[pn-dyn-365-guides](../includes/pn-dyn-365-guides.md)] PC app, one of the first steps is to choose an anchoring method. When you anchor a guide, you synchronize it spatially with your real-world environment (for example, a factory floor). Anchoring is how holograms know where they are in the real world. You must create an anchor for your guide for it to work on [!include[pn-hololens](../includes/pn-hololens.md)].

It's crucial to ensure that your guide alignment is correct and as precise as possible. If the guide is misaligned, your instructions may show actions at incorrect locations, which can result in operator confusion or damage to parts.

## Two ways to anchor a guide

There are two ways to anchor a guide:

- With a **printed anchor** (recommended), you align a guide by gazing at (scanning) a printed anchor that is attached to a physical object in the real world.

- With a **digital anchor**, you align a guide to a digital 3D hologram that is overlaid on a physical object in the real world. 

A printed anchor is recommended because it's more accurate. You might want or need to use a digital anchor, however, for any of the 
following reasons:

- It might not be feasible to attach a printed anchor because the authoring is done in a location different than where the parts are located.

- It might not be feasible to attach a printed anchor due to moving parts.

- You can't guarantee that the placement of the printed anchor will be the same every time.

- A part is too small to attach a printed anchor to.

[!include[pn-dyn-365-guides](../includes/pn-dyn-365-guides.md)] includes an **Anchor** wizard that makes it easy to select and set up the most appropriate anchor type for your situation.

## Anchor your guide by using a printed anchor

![Video camera graphic](media/video-camera.PNG "Video camera graphic") [Watch a video about creating a printed anchor](https://aka.ms/guidesprintedanchor)

Creating a printed anchor involves four basic steps:

1. Use the **Anchor** wizard to select an anchor method.

2. Print the anchor from the PDF file that the **Anchor** wizard createas.

3. Attach the printed anchor to a physical object in the real world.

4. Gaze at the anchor on [!include[pn-hololens](../includes/pn-hololens.md)] to anchor the guide.

### Set up a printed anchor

You can access the **Anchor** wizard from the **Outline** page. The **Outline** page automatically appears after you create or open a guide.

1. On the **Outline** page, select **Set your anchor now**.

    ![Set your anchor now button](media/outline-page-3.PNG "Set your anchor now button")

2. On the **Choose an anchor method** page, in the **Printed Anchor** tile, select **Select**.

    ![Select button in the Printed Anchor tile](media/choose-anchor-method.PNG "Select button in the Printed Anchor tile")

3. In step 1 of the wizard, select **Save to print** to create a PDF file that is named **Guides-PrintedAnchor**. This file includes the anchor that you will print in step 6.

    ![Save to print button](media/save-to-print-button.PNG "Save to print button")

4. On your computer, in Adobe Acrobat Reader, open the **Guides-PrintedAnchor** file.

5. Select **File** \> **Print**, and then, under **Page Sizing & Handling**, select the **Actual size** option.

    ![Actual size option](media/adobe-actual-size.PNG "Actual size option")

6. Print the last page of the document on matte stock. (Glossy materials can affect scanning.)

7. After printing is completed, make sure that the marker spacing matches the measurements that are shown in the following illustration.

    ![Printed anchor measurements](media/printed-anchor-measurements.PNG "Printed anchor measurements")

    > [!NOTE]
    > If the anchor spacing isn't within +/– 0.1 mm, in the **Print** dialog box, select the **Custom Scale** option, and then change the percentage to compensate for the size discrepancy. For example, if the result is 49 mm when you print the anchor, you must change the scale to 100.4 percent to get 49.196 mm, which is within tolerance.

8. Attach the printed anchor to a physical object in the real world, and then take a picture of the place where you put it, to help the operator find it.

9. Go back to the **Anchor** wizard in the PC app, and then select **Next** two times. 

10. In step 3 of the wizard, select **Import** to import the picture that you took in step 8. Then drag it to the **Import anchor placement photo** box. When you've finished, select **Next** to move to the next step.

    ![Import button](media/import-buttton.PNG "Import button")

11. In step 4 of the wizard, if you want to change the default instructions for the operator, select **Edit step card text**, and then enter your instructions. When you've finished, select **Next** to move to the next step.

    ![Edit step card text button](media/edit-step-card-text-button.PNG "Edit step card text button")

12. Put on your [!include[pn-hololens](../includes/pn-hololens.md)], open your guide, and then gaze at the printed anchor to anchor the guide.

### Best practices for printed anchors

Keep the following in mind when working with printed anchors:

- **Material surface.** Be sure to print the anchor on matte stock, and don't laminate it. Glossy materials can negatively affect scanning because of reflected light. Also, make sure that the anchor is flat. An anchor that is curved or distorted can affect alignment and detection.

- **Same anchor for authoring and printing.** For the best accuracy, use the **same** printed anchor for authoring and operating.

- **Size.** Make sure that your printed anchor is the exact size that is indicated in this topic. Incorrect anchor size causes misalignment of the guide.

    - Some applications and printers might change the size of the image.

    - If the anchor is larger than indicated, [!include[pn-hololens](../includes/pn-hololens.md)] interprets the scale difference in distance. Therefore, the anchor is identified as closer than it really is.

    - The best way to make sure that the anchor isn't resized is to print it from the PDF file, as described earlier in this topic.

- **Location.** Place the anchor in a location on the physical object that is easy to access and out of the way.

    - Ideally, the anchor placement should be central to the steps that are being performed.

    - Content placed farther away from the anchor will be less accurate.

    - Place the anchor where operators can quickly rescan to realign at any time.

    - Ideally, the anchor should not be moved after the author places it. If a permanent placement isn't possible, consider creating a mount so that the anchor can be consistently placed in the same location/orientation every time.

    - Take a photo or video to document the printed anchor placement, and add it to the guide instructions to increase operator confidence. To capture a photo or video from [!include[pn-hololens](../includes/pn-hololens.md)], see [Mixed reality capture](https://docs.microsoft.com/windows/mixed-reality/mixed-reality-capture).

- **Scanning angle.** Make sure you're facing the anchor straight on at the correct distance when gazing at it. 

    - Scanning from glancing angles can cause detection failure or misalignment.

    - Ideal scanning range is from 60 to 80 cm.

### How HoloLens establishes anchor position, scale, and orientation

During scanning, the forward-facing camera on [!include[pn-hololens](../includes/pn-hololens.md)] is used to measure the horizontal and vertical distances on the anchor. This information is combined with the actual anchor values that are stored internally in the application 
(49.2 mm and 32.8 mm) to establish the anchor's precise position, scale, and orientation in space.

[!include[pn-dyn-365-guides](../includes/pn-dyn-365-guides.md)] includes an additional correction method that lets users improve the alignment by manually overriding any offset that is generated by the variability of the acquired image and anchor size. For more information, see [Ensuring accurate placement of holograms for printed anchors](known-issues.md#how-do-i-address-hardware-offset-in-hololens-1-devices-to-ensure-accurate-placement-of-holograms-for-printed-anchor-alignment).

## Anchor your guide by using a digital anchor

![Video camera graphic](media/video-camera.PNG "Video camera graphic") [Watch a video about creating a digital anchor](https://aka.ms/guidesdigitalanchor)

Digital anchoring involves two basic steps:

1. Use the **Anchor** wizard in the PC app to import a custom 3D model that can be used as the anchor. Then assign the 3D model as the anchor for the guide. The 3D model can be a representation of a physical object or a generic 3D object. If you don't select a custom 3D model, a default digital anchor will be used.

2. In the [!include[pn-hololens](../includes/pn-hololens.md)] app, in **Author** mode, use gestures to align the digital anchor to a physical object in the real world.

### Set up a digital anchor

You can access the **Anchor** wizard from the **Outline** page. The **Outline** page automatically appears after you create or open a guide.

1. On the **Outline** page, select **Set your anchor now**.

   ![Set your anchor now button](media/outline-page-3.PNG "Set your anchor now button")

2. On the **Choose an anchor method** page, in the **Digital Anchor** tile, select **Select**.

   ![Select button in the Digital Anchor tile](media/choose-anchor-method-digital-anchor.PNG "Select button in the Digital Anchor tile")

3. In step 1 of the wizard, select **Import**, find your custom 3D model, and then select **Open** to import it. The model is added to the **3D parts** tab in the gallery.

   ![Import button](media/import-button-digital-anchor.PNG "Import button")

4. Drag the 3D model from the **3D parts** tab to the **Assign digital anchor** box. The 3D model is assigned as the digital anchor for the guide. When you've finished, select **Next** to move to the next step.

   ![Assign digital anchor box](media/drag-model-digital-anchor.PNG "Assign digital anchor box")

5. Put on your [!include[pn-hololens](../includes/pn-hololens.md)], open the guide, and then use air tap and hold to move the digital anchor directly over a physical object in your work environment. If you must rotate the object, use air tap and hold to move the blue spheres.

   ![Blue spheres](media/blue-spheres-digital-anchor.PNG "Blue spheres")

   > [!TIP]
   > On [!include[pn-hololens](../includes/pn-hololens.md)] 2, you can use your hand to directly select and place a digital anchor when you author a guide. For more information, see [Place your holograms](https://docs.microsoft.com/dynamics365/mixed-reality/guides/hololens-authoring#place-your-holograms).

6. Take a picture of the place where you put the digital anchor, to help the operator find it.

7. Go back to the PC app, and then select **Next** in the wizard two times.

8. In step 4 of the wizard, select the **Import** button to import the photo that you took in step 6. Then drag it to the **Import photo of anchor location** box. When you've finished, select **Next** to move to the next step.

    ![Import photo of anchor location box](media/drag-photo-digital-anchor.PNG "Import photo of anchor location box")

9. In step 5 of the wizard, if you want to change the default instructions for the operator, select **Edit step card text**, and then enter your instructions. When you've finished, select **Next** to move to the next step, and then select **Confirm**.

    ![Edit step card text button](media/edit-step-card-text-digital-anchor.PNG "Edit step card text button")

### Best practices for digital anchors

- **Size.** Select a digital anchor that's not too small or too big. 

  - Medium-size digital objects are best. Very small or very large holograms are difficult to manipulate. 
  
  - Shoebox size or slightly larger is ideal.
  
- **Placement.** Choose a digital anchor that's as close to the center of the work being done as possible. The farther you place digital content away from the digital twin, the less accurate it becomes.

- **Shape.** Select a digital anchor that has a non-uniform or uncommon shape. Unusual shapes are easiest to align to.

  - Avoid objects that are mirrored. This can cause 180-degree misalignment.
  
  - Pick shapes that have clear edges and corners to help orient your content properly.
  
- **Recognizable.** Select a digital anchor that's obvious, easily recognizable, and easy for the operator to find. Make sure that they can access the object without any obstructions.

- **Alignment direction.** Always align the digital anchor to your physical object from the same direction. This maximizes repeatability for operators.

    - Placement from different perspectives can cause misalignment.

    - Always look at the digital anchor from multiple angles to make sure that it's aligned to the physical object.

## Change from one anchor type to the other

1. On the **Outline** page, select the anchor at the top of the page, or select the **Anchor** button in the left navigation pane. The **Anchor** wizard is opened.

    ![Anchor button and anchor](media/change-anchor-method.PNG "Anchor button and anchor")

2. In the lower-left corner of the wizard window, select **Change anchor method**.

   ![Change anchor method button](media/change-anchor-method-button.PNG "Change anchor method button")

3. Select the anchor type that you want to change to.

4. In the warning message that appears, select **Switch anchor method**.

## Other factors that affect anchoring accuracy

The following factors can also affect the accuracy of the anchor and/or user perception of the alignment:

- **Interpupillary distance (IPD) setting.** IPD is the distance between the center of the user's pupils. Because different users might have different IPDs, it's crucial that the appropriate IPD be set, so that [!include[pn-hololens](../includes/pn-hololens.md)] can adapt its display. An incorrect IPD setting can cause inaccurate perception. It can also cause instability of holograms in space. To calibrate your IPD on [!include[pn-hololens](../includes/pn-hololens.md)] 1, [use the HoloLens Calibration app](https://docs.microsoft.com/windows/mixed-reality/calibration).

- **Pre-scanning the environment.** [!include[pn-hololens](../includes/pn-hololens.md)] actively scans its environment for visible features to map its surroundings. This scan occurs whenever the device is turned on and a user is signed in. It occurs regardless of whether you're in the [!include[pn-hololens](../includes/pn-hololens.md)] shell or running apps. [!include[pn-hololens](../includes/pn-hololens.md)] constantly improves the accuracy of these maps as it scans the environment from different viewpoints and stores the maps on the device. Holograms are placed in relation to these maps. The more accurate the map, the more accurate the hologram placement.

    Before [!include[pn-dyn-365-guides](../includes/pn-dyn-365-guides.md)] is used on a [!include[pn-hololens](../includes/pn-hololens.md)] that hasn't been used in a particular environment, have the user put on the [!include[pn-hololens](../includes/pn-hololens.md)], sign in to the device, and walk around the space where hologram instructions have been placed or will be placed. Although the user can perform this step from the [!include[pn-hololens](../includes/pn-hololens.md)] shell, we recommend that the **Start** menu be hidden, so that the user can see the space as he or she walks around. By walking at a leisurely pace while slowly looking up and down, the user will give the device an opportunity to find features and construct accurate maps. This process is called "pre-scanning" because it's done before you run [!include[pn-dyn-365-guides](../includes/pn-dyn-365-guides.md)]. You must complete this process only once for each environment, because [!include[pn-hololens](../includes/pn-hololens.md)] stores the maps that it creates on the device and remembers the spaces that it has scanned.

    Very dark or very bright environments, or environments that include very reflective surfaces (mirrors), dark surfaces, or featureless surfaces, negatively affect the ability of [!include[pn-hololens](../includes/pn-hololens.md)] to recognize the space. This, in turn,  affects hologram position and stability.

- **Impact of device positioning on [!include[pn-hololens](../includes/pn-hololens.md)] 1.** [!include[pn-hololens](../includes/pn-hololens.md)] uses a novel display technology to project images in the user's field of vision, creating holograms. On [!include[pn-hololens](../includes/pn-hololens.md)] 1, the way that users wear a device on their head has a huge impact on the perceived position of the holograms. The best way to understand this point is to adjust the device positioning while you align holograms to their physical counterparts in [!include[pn-dyn-365-guides](../includes/pn-dyn-365-guides.md)]. Notice how the alignment of holograms is affected when you shift the device left and right, and up and down, and when you slide the display forward and backward. Users should wear the device in a consistent way, and they should understand that subtle shifts in device positioning might not feel different but can cause significant changes in perceived hologram locations. On [!include[pn-hololens](../includes/pn-hololens.md)] 2, issues with device positioning are addressed through eye tracking.

## What's next?

[Structure your guide in the Outline page](structure-guide.md)<br>
[Create steps and add 3D content or 2D media](create-steps-assign-media.md)<br>
[Learn about keyboard shortcuts](keyboard-shortcuts-pc-app.md)
