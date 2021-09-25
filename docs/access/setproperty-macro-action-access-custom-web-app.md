---
title: SetProperty Macro Action (Application web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: 1e97dd95-23f6-4f49-b3b9-2c7261b3a70d
description: Vous pouvez utiliser l’action DéfinirProperty pour définir une propriété pour un contrôle sur un affichage.
ms.openlocfilehash: 1f72d038d522b9ed6e1b1c6d27dd948d8ee7352a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59601491"
---
# <a name="setproperty-macro-action-access-custom-web-app"></a>SetProperty Macro Action (Application web personnalisée Access)

Vous pouvez utiliser **l’action DéfinirProperty** pour définir une propriété pour un contrôle sur un affichage. 
  
> [!IMPORTANT]
> Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles. 
  
## <a name="setting"></a>Paramètre

**L’action DéfinirProperty** présente les arguments répertoriés dans le tableau suivant. 
  
|**Argument de l'action**|**Description**|
|:-----|:-----|
| _Nom du contrôle_ : <br/> |Tapez le nom du champ ou du contrôle pour lequel vous souhaitez définir la valeur d’une propriété. Laissez cet argument vide pour définir la propriété de l’affichage.  <br/> |
| _Propriété_ <br/> |Sélectionnez la propriété dont la valeur doit être définie. Consultez la section **Remarques** de cet article pour accéder à la liste des propriétés qui peuvent être définies via cette action.<br/> |
| _Valeur_ <br/> |Tapez la valeur que vous souhaitez définir pour la propriété. Pour les propriétés dont la valeur doit être définie sur Oui ou Non, utilisez **-1** pour Oui et **0** pour Non.<br/> |
   
## <a name="remarks"></a>Remarques

Vous pouvez utiliser **l’action DéfinirProperty** pour définir les propriétés suivantes d’un contrôle : 
  
- Légende
    
- Activé
    
- ForeColor
    
- Valeur
    
- Visible
    
Si vous entrez une valeur non admise pour l'argument ** *Valeur* **, aucune erreur ne se produit, mais il se peut que la valeur de la propriété soit modifiée dans Access, selon l'interprétation de l'argument. 
  

