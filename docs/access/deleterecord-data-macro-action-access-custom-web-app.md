---
title: DeleteRecord Data, action de macro (application Web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: f6b68a9a-e04a-476e-a407-b1779fea1953
description: Vous pouvez utiliser l'action SupprimerEnregistrement pour supprimer un enregistrement.
ms.openlocfilehash: 0e8a658b944e894e4d4014fb3d3d9a583efbee8d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423152"
---
# <a name="deleterecord-data-macro-action-access-custom-web-app"></a>DeleteRecord Data, action de macro (application Web personnalisée Access)

Vous pouvez utiliser l'action **SupprimerEnregistrement** pour supprimer un enregistrement. 
  
> [!IMPORTANT]
> Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles. 
  
## <a name="setting"></a>Paramètre

L'action **DeleteRecord** possède les arguments suivants. 
  
|**Argument**|**Description**|
|:-----|:-----|
|**Alias d’enregistrement** <br/> |Chaîne qui identifie l’enregistrement à supprimer. Si l'argument *alias* n'est pas spécifié, l'enregistrement actif est supprimé.  <br/> |
   
## <a name="remarks"></a>Remarques

Vous pouvez utiliser la variable locale **IdentitéDernierEnregistrementCréé** pour travailler avec le dernier enregistrement créé dans un bloc de données **CréerEnregistrement**. Par exemple, utilisez la syntaxe suivante pour faire référence au dernier enregistrement créé: 
  
`[LastCreateRecordIdentity]`


