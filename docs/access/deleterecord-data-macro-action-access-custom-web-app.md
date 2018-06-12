---
title: Action de Macro de données SupprimerEnregistrement (accès personnalisé web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: f6b68a9a-e04a-476e-a407-b1779fea1953
description: Vous pouvez utiliser l’action SupprimerEnregistrement pour supprimer un enregistrement.
ms.openlocfilehash: 64742d73ec57b94474c8e27822fd3946c7673336
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19781781"
---
# <a name="deleterecord-data-macro-action-access-custom-web-app"></a>Action de Macro de données SupprimerEnregistrement (accès personnalisé web app)

Vous pouvez utiliser l'action **SupprimerEnregistrement** pour supprimer un enregistrement. 
  
> [!IMPORTANT]
> [!IMPORTANTE] Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles. 
  
## <a name="setting"></a>Valeur

L’action **SupprimerEnregistrement** possède les arguments suivants. 
  
|**Argument**|**Description**|
|:-----|:-----|
|**Alias d’enregistrement** <br/> |Une chaîne qui identifie l’enregistrement à supprimer. Si l’argument *Alias* n’est pas spécifié, l’enregistrement actif est supprimé.  <br/> |
   
## <a name="remarks"></a>Notes

Vous pouvez utiliser la variable locale **IdentitéDernierEnregistrementCréé** pour travailler avec le dernier enregistrement créé dans un bloc de données **CréerEnregistrement**. Par exemple, utilisez la syntaxe suivante pour faire référence à l’enregistrement plus récent : 
  
`[LastCreateRecordIdentity]`


