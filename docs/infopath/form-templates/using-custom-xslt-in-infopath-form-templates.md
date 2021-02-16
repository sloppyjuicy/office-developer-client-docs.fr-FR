---
title: Utilisation de langage XSLT personnalisé dans les modèles de formulaire InfoPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 32c80bcd-a5d6-af32-38ba-9ca9ff148b99
description: Vous pouvez créer la plupart des éléments d'affichage dont vous aurez probablement besoin dans le concepteur de formulaires Microsoft InfoPath. Si vous avez besoin d'un élément d'affichage personnalisé qu'InfoPath ne peut pas créer pour vous, vous pouvez cependant modifier manuellement le fichier XSLT (XSL Transformation) utilisé par InfoPath pour générer l'affichage. Pour cela, extrayez le formulaire et ses fichiers de composants à l'aide de Exporter les fichiers source sur l'onglet Publier de Microsoft Office Backstage, puis modifiez la transformation dans votre éditeur XML favori, tel que Microsoft Visual Studio ou le Bloc-notes.
ms.openlocfilehash: a61980191dbedeec33b06ad8173ce50126fea781
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428269"
---
# <a name="using-custom-xslt-in-infopath-form-templates"></a><span data-ttu-id="f32ce-105">Utilisation de langage XSLT personnalisé dans les modèles de formulaire InfoPath</span><span class="sxs-lookup"><span data-stu-id="f32ce-105">Using Custom XSLT in InfoPath Form Templates</span></span>

<span data-ttu-id="f32ce-p102">Vous pouvez créer la plupart des éléments d'affichage dont vous aurez probablement besoin dans le concepteur de formulaires Microsoft InfoPath. Si vous avez besoin d'un élément d'affichage personnalisé qu'InfoPath ne peut pas créer pour vous, vous pouvez cependant modifier manuellement le fichier XSLT (XSL Transformation) utilisé par InfoPath pour générer l'affichage. Pour cela, extrayez le formulaire et ses fichiers de composants à l'aide de **Exporter les fichiers source** sur l'onglet **Publier** de Microsoft Office Backstage, puis modifiez la transformation dans votre éditeur XML favori, tel que Microsoft Visual Studio ou le Bloc-notes.</span><span class="sxs-lookup"><span data-stu-id="f32ce-p102">You can create most of the view elements you're likely to need in the Microsoft InfoPath form designer. If you need a custom view element that InfoPath can't create for you, however, you can manually modify the XSL Transformation (XSLT) that InfoPath uses to generate the view. To do so, extract the form into its component files by using **Export Source Files** on the **Publish** tab of the Microsoft Office Backstage, and then edit the transform in your preferred XML editor, such as Microsoft Visual Studio or Notepad.</span></span> 
  
<span data-ttu-id="f32ce-p103">Si vous apportez des modifications à une transformation d'affichage en dehors d'InfoPath, puis que vous ouvrez l'affichage en mode conception et que vous effectuez des modifications, InfoPath remplace les modifications que vous avez effectuées manuellement. Pour empêcher InfoPath de remplacer vos modifications, vous devez les placer dans un élément  `<xsl:template>` de la transformation et utiliser le mode  `xd:preserve`, comme indiqué ici :</span><span class="sxs-lookup"><span data-stu-id="f32ce-p103">If you make changes to a view transform outside of InfoPath and then open the view in design mode and make changes, InfoPath will overwrite the changes you made manually. To keep InfoPath from overwriting the changes you make, you must place those changes in an  `<xsl:template>` element in the transform and use the  `xd:preserve` mode, as shown here:</span></span> 
  
```XML
<xsl:template match="my:field1" mode="xd:preserve"> 
   <div> 
      The value of field1 is <xsl:value-of select="."/> 
   </div> 
</xsl:template>
```

<span data-ttu-id="f32ce-111">Pour inclure le modèle dans le fichier transformé, utilisez l'élément  `<xsl:apply-templates>` avec le même mode  `xd:preserve` :</span><span class="sxs-lookup"><span data-stu-id="f32ce-111">To include the template in the transformed file, use the  `<xsl:apply-templates>` element with the same  `xd:preserve` mode:</span></span> 
  
```XML
<xsl:apply-templates select="my:field1" mode="xd:preserve"/>
```

<span data-ttu-id="f32ce-p104">Les éléments et les constructions définies dans des modèles XSL avec le mode  `xd:preserve` ne seront pas affichées dans l'environnement de conception InfoPath. Au lieu de cela, InfoPath marquera la section personnalisée avec un contrôle nommé **Conserver le bloc de code** avec une bordure rouge. Lorsqu'un utilisateur ouvre le formulaire pour le remplir, les transformations XSL personnalisées sont appliquées et les contrôles **Conserver le bloc de code** n'apparaissent pas.</span><span class="sxs-lookup"><span data-stu-id="f32ce-p104">Elements and constructs defined within XSL templates with the  `xd:preserve` mode will not be displayed in the InfoPath design environment. Instead, InfoPath will mark the custom section with a control labeled **Preserve Code Block** with a red border. When a user opens the form to fill it out, the custom XSL transforms are applied and the **Preserve Code Block** controls will not appear.</span></span> 
  

