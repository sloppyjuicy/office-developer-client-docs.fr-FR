---
title: Utilisation de langage XSLT personnalisé dans les modèles de formulaire InfoPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 32c80bcd-a5d6-af32-38ba-9ca9ff148b99
description: Vous pouvez créer la plupart des éléments d'affichage dont vous aurez probablement besoin dans le concepteur de formulaires Microsoft InfoPath. Si vous avez besoin d'un élément d'affichage personnalisé qu'InfoPath ne peut pas créer pour vous, vous pouvez cependant modifier manuellement le fichier XSLT (XSL Transformation) utilisé par InfoPath pour générer l'affichage. Pour cela, extrayez le formulaire et ses fichiers de composants à l'aide de Exporter les fichiers source sur l'onglet Publier de Microsoft Office Backstage, puis modifiez la transformation dans votre éditeur XML favori, tel que Microsoft Visual Studio ou le Bloc-notes.
ms.openlocfilehash: 1eda97ccb9035eb9dbc68fff56b74c205b0ec4c6
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63380291"
---
# <a name="using-custom-xslt-in-infopath-form-templates"></a>Utilisation de langage XSLT personnalisé dans les modèles de formulaire InfoPath

Vous pouvez créer la plupart des éléments d'affichage dont vous aurez probablement besoin dans le concepteur de formulaires Microsoft InfoPath. Si vous avez besoin d'un élément d'affichage personnalisé qu'InfoPath ne peut pas créer pour vous, vous pouvez cependant modifier manuellement le fichier XSLT (XSL Transformation) utilisé par InfoPath pour générer l'affichage. Pour cela, extrayez le formulaire et ses fichiers de composants à l'aide de **Exporter les fichiers source** sur l'onglet **Publier** de Microsoft Office Backstage, puis modifiez la transformation dans votre éditeur XML favori, tel que Microsoft Visual Studio ou le Bloc-notes.
  
Si vous apportez des modifications à une transformation d'affichage en dehors d'InfoPath, puis que vous ouvrez l'affichage en mode conception et que vous effectuez des modifications, InfoPath remplace les modifications que vous avez effectuées manuellement. Pour empêcher InfoPath de modifier les modifications apportées, `<xsl:template>` `xd:preserve` vous devez placer ces modifications dans un élément de la transformation et utiliser le mode, comme illustré ici :
  
```XML
<xsl:template match="my:field1" mode="xd:preserve"> 
   <div> 
      The value of field1 is <xsl:value-of select="."/> 
   </div> 
</xsl:template>
```

Pour inclure le modèle dans le fichier transformé, utilisez l’élément `<xsl:apply-templates>` avec le même `xd:preserve` mode :
  
```XML
<xsl:apply-templates select="my:field1" mode="xd:preserve"/>
```

Les éléments et les constructions définis dans les modèles `xd:preserve` XSL avec le mode ne seront pas affichés dans l’environnement de conception InfoPath. Au lieu de cela, InfoPath marquera la section personnalisée avec un contrôle nommé **Conserver le bloc de code** avec une bordure rouge. Lorsqu'un utilisateur ouvre le formulaire pour le remplir, les transformations XSL personnalisées sont appliquées et les contrôles **Conserver le bloc de code** n'apparaissent pas.
  