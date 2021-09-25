---
title: SupprimerEnregistrement, action de macro de données (application web personnalisée Access)
manager: lindalu
ms.date: 09/05/2021
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: f6b68a9a-e04a-476e-a407-b1779fea1953
ms.openlocfilehash: 01d0cdeecd7c1401c274822736a3cd40a865db52
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59586431"
---
# <a name="deleterecord-data-macro-action-access-custom-web-app"></a>SupprimerEnregistrement, action de macro de données (application web personnalisée Access)

Vous pouvez utiliser l'action **SupprimerEnregistrement** pour supprimer un enregistrement. 
  
> [!IMPORTANT]
> Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles. 
  
## <a name="setting"></a>Paramètre

**L’action SupprimerEnregistrement** a les arguments suivants. 
  
|**Argument**|**Description**|
|:-----|:-----|
|**Alias d’enregistrement** <br/> |Chaîne qui identifie l’enregistrement à supprimer. Si  *l’argument Alias*  n’est pas spécifié, l’enregistrement actuel est supprimé.  <br/> |
   
## <a name="remarks"></a>Remarques

Vous pouvez utiliser la variable locale **IdentitéDernierEnregistrementCréé** pour travailler avec le dernier enregistrement créé dans un bloc de données **CréerEnregistrement**. Par exemple, utilisez la syntaxe suivante pour faire référence au dernier enregistrement créé : 
  
`[LastCreateRecordIdentity]`
