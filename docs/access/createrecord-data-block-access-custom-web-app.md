---
title: Bloc de données CréerEnregistrement (application Web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9dd73bae-a8d5-4d8b-b356-01ac72f7e5d9
description: Vous pouvez utiliser le bloc de données CréerEnregistrement pour créer un nouvel enregistrement dans la table spécifiée.
ms.openlocfilehash: d89b62180dbe50a0c7dab862b70062a47558c25a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421374"
---
# <a name="createrecord-data-block-access-custom-web-app"></a>Bloc de données CréerEnregistrement (application Web personnalisée Access)

Vous pouvez utiliser le bloc de données **CréerEnregistrement** pour créer un nouvel enregistrement dans la table spécifiée. 
  
> [!IMPORTANT]
> Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles. 
  
> [!NOTE]
> Le bloc de données **CréerEnregistrement** est disponible uniquement dans les macros de données. 
  
## <a name="setting"></a>Setting

Le bloc de données **CréerEnregistrement** utilise les arguments suivants. 
  
Le bloc de données **CréerEnregistrement** utilise les arguments suivants. 
  
|**Nom de l’argument**|**Obligatoire**|**Description**|
|:-----|:-----|:-----|
|**Créer un enregistrement dans** <br/> |Oui  <br/> |Nom de la table dans laquelle créer le nouvel enregistrement.  <br/> |
|**Alias** <br/> |Non  <br/> |Chaîne qui identifie l'enregistrement. Vous pouvez utiliser l’alias de l’enregistrement pour l’identifier.  <br/> |
   
## <a name="remarks"></a>Remarques

L’enregistrement créé par **CréerEnregistrement ** devient automatiquement l’enregistrement actif. 
  
Après l'instruction **CréerEnregistrement** , vous pouvez insérer un bloc de commandes qui s'exécutera avant la validation du nouvel enregistrement. Les actions suivantes sont disponibles dans un bloc de données **CréerEnregistrement**. 
  
||
|:-----|
|[Action de macro AnnulerModificationEnregistrement](cancelrecordchange-macro-action-access-custom-web-app.md) <br/> |
|[Instruction de macro Comment](comment-macro-block-access-custom-web-app.md) <br/> |
|[Instruction de macro Group](group-macro-block-access-custom-web-app.md) <br/> |
|[Instruction de macro If... Then... Else](ifthenelse-macro-block-access-custom-web-app.md) <br/> |
|[Action de macro DéfinirChamp](setfield-macro-action-access-custom-web-app.md) <br/> |
|[Action de macro DéfinirVarLocale](setlocalvar-macro-action-access-custom-web-app.md) <br/> |
   
Après que l’action **CréerEnregistrement** a créé un enregistrement, utilisez l’action **DéfinirChamp** pour spécifier une valeur d’un champ dans le nouvel enregistrement. 
  
Vous pouvez utiliser une **If... Then... Else** pour effectuer des opérations en fonction d'une condition. 
  
Pour annuler la création d'un enregistrement, utilisez l'action **AnnulerModificationEnregistrement**. Cela empêche la validation des modifications et quitte le bloc de données **CréerEnregistrement**. 
  
Une fois le nouvel enregistrement validé, vous pouvez utiliser la variable locale **IdentitéDernierEnregistrementCréé** pour travailler avec l’enregistrement. Par exemple, utilisez la syntaxe suivante pour faire référence au champ AffectéÀ du dernier enregistrement créé. 
  
`[LastCreateRecordIdentity].[AssignedTo]`


