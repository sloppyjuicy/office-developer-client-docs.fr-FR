---
title: Action de Macro DéfinirPropriété (accès personnalisé web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 1e97dd95-23f6-4f49-b3b9-2c7261b3a70d
description: Vous pouvez utiliser l’action DéfinirPropriété pour définir une propriété d’un contrôle sur un affichage.
ms.openlocfilehash: 89ac2b10715d707d3b6ee09ee8ab915384c5acf5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19781975"
---
# <a name="setproperty-macro-action-access-custom-web-app"></a>Action de Macro DéfinirPropriété (accès personnalisé web app)

Vous pouvez utiliser l’action **DéfinirPropriété** pour définir une propriété d’un contrôle sur un affichage. 
  
> [!IMPORTANT]
> [!IMPORTANTE] Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles. 
  
## <a name="setting"></a>Valeur

L’action **DéfinirPropriété** utilise les arguments répertoriés dans le tableau suivant. 
  
|**Argument de l'action**|**Description**|
|:-----|:-----|
| _Nom du contrôle_ <br/> |Tapez le nom du champ ou du contrôle pour lequel vous voulez définir la valeur de propriété. Laissez cet argument vide pour définir la propriété pour l’affichage.  <br/> |
| _Propriété_ <br/> |Sélectionnez la propriété que vous souhaitez définir. Voir la section **Remarques** dans cet article pour obtenir la liste des propriétés qui peuvent être définies à l’aide de cette action.  <br/> |
| _Valeur_ <br/> |Tapez la valeur de la propriété doit être définie sur. Pour les propriétés dont les valeurs sont Oui ou non, utilisent **-1** pour Oui et **0** pour non.  <br/> |
   
## <a name="remarks"></a>Remarques

Vous pouvez utiliser l’action **DéfinirPropriété** pour définir les propriétés d’un contrôle suivantes : 
  
- Caption
    
- Activé
    
- Propriété ForeColor
    
- Valeur
    
- Visible
    
Si vous entrez une valeur non admise pour l'argument ** *Valeur* **, aucune erreur ne se produit, mais il se peut que la valeur de la propriété soit modifiée dans Access, selon l'interprétation de l'argument. 
  

