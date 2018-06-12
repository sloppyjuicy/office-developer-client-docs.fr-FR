---
title: Bloc de données ModifierEnregistrement (accès personnalisé web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 54975434-78b2-4010-b2f9-f277831fa92e
description: Vous pouvez utiliser le bloc de données ModifierEnregistrement pour modifier les valeurs contenues dans un enregistrement existant.
ms.openlocfilehash: 6c214e48326a93cff220b5436d7e7802cd6e3431
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19781811"
---
# <a name="editrecord-data-block-access-custom-web-app"></a>Bloc de données ModifierEnregistrement (accès personnalisé web app)

Vous pouvez utiliser le bloc de données **ModifierEnregistrement** pour modifier les valeurs contenues dans un enregistrement existant. 
  
> [!IMPORTANT]
> [!IMPORTANTE] Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles. 
  
> [!NOTE]
> [!REMARQUE] Le bloc de données **ModifierEnregistrement** est disponible uniquement dans les macros de données. 
  
## <a name="setting"></a>Paramètre

Le bloc de données **ModifierEnregistrement** utilise les arguments suivants. 
  
|**Argument**|**Description**|
|:-----|:-----|
|**Alias** <br/> |Une chaîne qui identifie l’enregistrement à modifier. Si l’argument *Alias* n’est pas spécifié, l’enregistrement actif est modifié.  <br/> |
   
## <a name="remarks"></a>Note

Après l’instruction **EditRecord** , vous pouvez insérer un bloc de commandes qui sera exécuté avant que les modifications apportées à l’enregistrement sont validées. Les actions suivantes sont disponibles dans un bloc de données **ModifierEnregistrement** . 
  
||
|:-----|
|[Action de Macro AnnulerModificationEnregistrement](cancelrecordchange-macro-action-access-custom-web-app.md) <br/> |
|[Instruction de Macro commentaire](comment-macro-block-access-custom-web-app.md) <br/> |
|[Group, instruction de Macro](group-macro-block-access-custom-web-app.md) <br/> |
|[If... Procédez comme suit... Else, instruction de Macro](ifthenelse-macro-block-access-custom-web-app.md) <br/> |
|[Action de Macro SetField](setfield-macro-action-access-custom-web-app.md) <br/> |
|[Action de Macro DéfinirVarLocale](setlocalvar-macro-action-access-custom-web-app.md) <br/> |
   
Utilisez l'action **DéfinirChamp** pour spécifier les nouvelles valeurs d'un champ dans l'enregistrement modifié. 
  
Vous pouvez utiliser un **Si... Procédez comme suit... Autre** instruction pour effectuer des opérations en fonction d’une condition. 
  
Pour annuler la modification d'un enregistrement, utilisez l'action **AnnulerModificationEnregistrement**. Cela empêche la validation des modifications et quitte le bloc de données **ModifierEnregistrement**. 
  
Vous pouvez utiliser la variable locale **IdentitéDernierEnregistrementCréé** pour travailler avec le dernier enregistrement créé dans un bloc de données **CréerEnregistrement**. Par exemple, utilisez la syntaxe suivante pour faire référence au champ AssignedTo du dernier enregistrement : 
  
`[LastCreateRecordIdentity].[AssignedTo]`


