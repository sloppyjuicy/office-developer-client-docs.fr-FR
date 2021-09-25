---
title: Utilisation de langage XSLT personnalisé dans les modèles de formulaire InfoPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 32c80bcd-a5d6-af32-38ba-9ca9ff148b99
description: Vous pouvez créer la plupart des éléments d'affichage dont vous aurez probablement besoin dans le concepteur de formulaires Microsoft InfoPath. Si vous avez besoin d'un élément d'affichage personnalisé qu'InfoPath ne peut pas créer pour vous, vous pouvez cependant modifier manuellement le fichier XSLT (XSL Transformation) utilisé par InfoPath pour générer l'affichage. Pour cela, extrayez le formulaire et ses fichiers de composants à l'aide de Exporter les fichiers source sur l'onglet Publier de Microsoft Office Backstage, puis modifiez la transformation dans votre éditeur XML favori, tel que Microsoft Visual Studio ou le Bloc-notes.
ms.openlocfilehash: 6f25005eb69ce298f79082273eb9d21e3acf34f8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59621240"
---
# <a name="using-custom-xslt-in-infopath-form-templates"></a>Utilisation de langage XSLT personnalisé dans les modèles de formulaire InfoPath

Vous pouvez créer la plupart des éléments d'affichage dont vous aurez probablement besoin dans le concepteur de formulaires Microsoft InfoPath. Si vous avez besoin d'un élément d'affichage personnalisé qu'InfoPath ne peut pas créer pour vous, vous pouvez cependant modifier manuellement le fichier XSLT (XSL Transformation) utilisé par InfoPath pour générer l'affichage. Pour cela, extrayez le formulaire et ses fichiers de composants à l'aide de **Exporter les fichiers source** sur l'onglet **Publier** de Microsoft Office Backstage, puis modifiez la transformation dans votre éditeur XML favori, tel que Microsoft Visual Studio ou le Bloc-notes. 
  
Si vous apportez des modifications à une transformation d'affichage en dehors d'InfoPath, puis que vous ouvrez l'affichage en mode conception et que vous effectuez des modifications, InfoPath remplace les modifications que vous avez effectuées manuellement. Pour empêcher InfoPath de remplacer vos modifications, vous devez les placer dans un élément  `<xsl:template>` de la transformation et utiliser le mode  `xd:preserve`, comme indiqué ici : 
  
```XML
<xsl:template match="my:field1" mode="xd:preserve"> 
   <div> 
      The value of field1 is <xsl:value-of select="."/> 
   </div> 
</xsl:template>
```

Pour inclure le modèle dans le fichier transformé, utilisez l'élément  `<xsl:apply-templates>` avec le même mode  `xd:preserve` : 
  
```XML
<xsl:apply-templates select="my:field1" mode="xd:preserve"/>
```

Les éléments et les constructions définies dans des modèles XSL avec le mode  `xd:preserve` ne seront pas affichées dans l'environnement de conception InfoPath. Au lieu de cela, InfoPath marquera la section personnalisée avec un contrôle nommé **Conserver le bloc de code** avec une bordure rouge. Lorsqu'un utilisateur ouvre le formulaire pour le remplir, les transformations XSL personnalisées sont appliquées et les contrôles **Conserver le bloc de code** n'apparaissent pas. 
  

