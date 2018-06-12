---
title: Bloc de données CréerEnregistrement (accès personnalisé web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9dd73bae-a8d5-4d8b-b356-01ac72f7e5d9
description: Vous pouvez utiliser le bloc de données CréerEnregistrement pour créer un nouvel enregistrement dans la table spécifiée.
ms.openlocfilehash: dc4be7653081c7c02426d84c74b7b56e597706fa
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19781856"
---
# <a name="createrecord-data-block-access-custom-web-app"></a>Bloc de données CréerEnregistrement (accès personnalisé web app)

Vous pouvez utiliser le bloc de données **CréerEnregistrement** pour créer un nouvel enregistrement dans la table spécifiée. 
  
> [!IMPORTANT]
> [!IMPORTANTE] Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles. 
  
> [!NOTE]
> [!REMARQUE] Le bloc de données **CréerEnregistrement** est disponible uniquement dans les macros de données. 
  
## <a name="setting"></a>Paramètre

Le bloc de données **SupprimerEnregistrement** utilise les arguments suivants. 
  
Le bloc de données **SupprimerEnregistrement** utilise les arguments suivants. 
  
|**Nom de l’argument**|**Obligatoire**|**Description**|
|:-----|:-----|:-----|
|**Créer un enregistrement dans** <br/> |Oui  <br/> |Nom de la table dans laquelle créer le nouvel enregistrement.  <br/> |
|**Alias** <br/> |Non  <br/> |Une chaîne qui identifie l’enregistrement. Vous pouvez utiliser l’alias de l’enregistrement pour l’identifier.  <br/> |
   
## <a name="remarks"></a>Notes

L'enregistrement créé par **CréerEnregistrement** devient automatiquement l'enregistrement actif. 
  
Après l’instruction **CréerEnregistrement** , vous pouvez insérer un bloc de commandes qui sera exécuté avant que le nouvel enregistrement est validé. Les actions suivantes sont disponibles dans un bloc de données **CréerEnregistrement**. 
  
||
|:-----|
|[Action de Macro AnnulerModificationEnregistrement](cancelrecordchange-macro-action-access-custom-web-app.md) <br/> |
|[Instruction de Macro commentaire](comment-macro-block-access-custom-web-app.md) <br/> |
|[Group, instruction de Macro](group-macro-block-access-custom-web-app.md) <br/> |
|[If... Procédez comme suit... Else, instruction de Macro](ifthenelse-macro-block-access-custom-web-app.md) <br/> |
|[Action de Macro SetField](setfield-macro-action-access-custom-web-app.md) <br/> |
|[Action de Macro DéfinirVarLocale](setlocalvar-macro-action-access-custom-web-app.md) <br/> |
   
Après que l'action **CréerEnregistrement** a créé un enregistrement, utilisez l'action **DéfinirChamp** pour spécifier une valeur d'un champ dans le nouvel enregistrement. 
  
Vous pouvez utiliser un **Si... Procédez comme suit... Autre** instruction pour effectuer des opérations en fonction d’une condition. 
  
Pour annuler la création d'un enregistrement, utilisez l'action **AnnulerModificationEnregistrement**. Cela empêche la validation des modifications et quitte le bloc de données **CréerEnregistrement**. 
  
Une fois le nouvel enregistrement validé, vous pouvez utiliser la variable locale **IdentitéDernierEnregistrementCréé** pour travailler avec l'enregistrement. Par exemple, utilisez la syntaxe suivante pour faire référence au champ AssignedTo du dernier enregistrement. 
  
`[LastCreateRecordIdentity].[AssignedTo]`


