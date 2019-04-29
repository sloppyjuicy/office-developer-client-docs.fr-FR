---
title: SetProperty, action de macro (application Web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 1e97dd95-23f6-4f49-b3b9-2c7261b3a70d
description: Vous pouvez utiliser l'action DéfinirPropriété pour définir une propriété pour un contrôle sur une vue.
ms.openlocfilehash: 1876be32606d66e0570c9e69206a508b8888b157
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438028"
---
# <a name="setproperty-macro-action-access-custom-web-app"></a>SetProperty, action de macro (application Web personnalisée Access)

Vous pouvez utiliser l'action **DéfinirPropriété** pour définir une propriété pour un contrôle sur une vue. 
  
> [!IMPORTANT]
> Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles. 
  
## <a name="setting"></a>Paramètre

L'action **SetProperty** possède les arguments figurant dans le tableau suivant. 
  
|**Argument de l'action**|**Description**|
|:-----|:-----|
| _Nom du contrôle_ : <br/> |Tapez le nom du champ ou du contrôle pour lequel vous souhaitez définir la valeur d’une propriété. Laissez cet argument vide pour définir la propriété de l'affichage.  <br/> |
| _Property_ <br/> |Sélectionnez la propriété dont la valeur doit être définie. Consultez la section **Remarques** de cet article pour accéder à la liste des propriétés qui peuvent être définies via cette action.<br/> |
| _Valeur_ <br/> |Tapez la valeur que vous souhaitez définir pour la propriété. Pour les propriétés dont la valeur doit être définie sur Oui ou Non, utilisez **-1** pour Oui et **0** pour Non.<br/> |
   
## <a name="remarks"></a>Remarques

Vous pouvez utiliser l'action **SetProperty** pour définir les propriétés suivantes d'un contrôle: 
  
- Légende
    
- Activé
    
- ForeColor
    
- Valeur
    
- Visible
    
Si vous entrez une valeur non admise pour l'argument ** *Valeur* **, aucune erreur ne se produit, mais il se peut que la valeur de la propriété soit modifiée dans Access, selon l'interprétation de l'argument. 
  

