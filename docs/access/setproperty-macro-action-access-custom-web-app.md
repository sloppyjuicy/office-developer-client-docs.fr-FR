---
title: SetProperty Macro Action (Application web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: 1e97dd95-23f6-4f49-b3b9-2c7261b3a70d
description: Vous pouvez utiliser l’action DéfinirProperty pour définir une propriété pour un contrôle sur un affichage.
ms.openlocfilehash: 1c2d19413835f2e920d974d59a789e942659b755
ms.sourcegitcommit: f8dc13ccaadfbd6d3783c3b291d998d5255a5f38
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2022
ms.locfileid: "63402617"
---
# <a name="setproperty-macro-action-access-custom-web-app"></a>SetProperty Macro Action (Application web personnalisée Access)

Vous pouvez utiliser **l’action DéfinirProperty** pour définir une propriété pour un contrôle sur un affichage.
  
> [!IMPORTANT]
> Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles.
  
## <a name="setting"></a>Paramètre

**L’action DéfinirProperty** présente les arguments répertoriés dans le tableau suivant.
  
|**Argument de l'action**|**Description**|
|:-----|:-----|
| _Nom du contrôle_ : <br/> |Tapez le nom du champ ou du contrôle pour lequel vous souhaitez définir la valeur d’une propriété. Laissez cet argument vide pour définir la propriété de l’affichage. |
| _Propriété_ <br/> |Sélectionnez la propriété dont la valeur doit être définie. Consultez la section **Remarques** de cet article pour accéder à la liste des propriétés qui peuvent être définies via cette action. |
| _Valeur_ <br/> |Tapez la valeur que vous souhaitez définir pour la propriété. Pour les propriétés dont la valeur doit être définie sur Oui ou Non, utilisez **-1** pour Oui et **0** pour Non. |

## <a name="remarks"></a>Remarques

Vous pouvez utiliser **l’action DéfinirProperty** pour définir les propriétés suivantes d’un contrôle :
  
- Légende
- Activé
- ForeColor
- Valeur
- Visible

Si vous entrez une valeur non admise pour l’argument ***Valeur***, aucune erreur ne se produit, mais il se peut que la valeur de la propriété soit modifiée dans Access, selon l’interprétation de l’argument.
  