---
title: EditRecord Data Block (Access custom web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 54975434-78b2-4010-b2f9-f277831fa92e
description: Vous pouvez utiliser le bloc de données ModifierEnregistrement pour modifier les valeurs contenues dans un enregistrement existant.
ms.openlocfilehash: 8e179eb08d5624adb58a72576ac816126e0a8edc
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59621492"
---
# <a name="editrecord-data-block-access-custom-web-app"></a>EditRecord Data Block (Access custom web app)

Vous pouvez utiliser le bloc de données **ModifierEnregistrement** pour modifier les valeurs contenues dans un enregistrement existant. 
  
> [!IMPORTANT]
> Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles. 
  
> [!NOTE]
> Le bloc de données **ModifierEnregistrement** est disponible uniquement dans les macros de données. 
  
## <a name="setting"></a>Paramètre

Le bloc de données **ModifierEnregistrement** utilise les arguments suivants. 
  
|**Argument**|**Description**|
|:-----|:-----|
|**Alias** <br/> |Chaîne qui identifie l’enregistrement à modifier. Si  *l’argument Alias*  n’est pas spécifié, l’enregistrement actuel est modifié.  <br/> |
   
## <a name="remarks"></a>Remarques

Après **l’instruction EditRecord,** vous pouvez insérer un bloc de commandes qui s’exécute avant que les modifications apportées à l’enregistrement soient enregistrées. Les actions suivantes sont disponibles dans un bloc **de données EditRecord.** 
  
||
|:-----|
|[Action de macro AnnulerModificationEnregistrement](cancelrecordchange-macro-action-access-custom-web-app.md) <br/> |
|[Instruction de macro Comment](comment-macro-block-access-custom-web-app.md) <br/> |
|[Instruction de macro Group](group-macro-block-access-custom-web-app.md) <br/> |
|[Instruction de macro If... Then... Else](ifthenelse-macro-block-access-custom-web-app.md) <br/> |
|[Action de macro DéfinirChamp](setfield-macro-action-access-custom-web-app.md) <br/> |
|[Action de macro DéfinirVarLocale](setlocalvar-macro-action-access-custom-web-app.md) <br/> |
   
Utilisez l'action **DéfinirChamp** pour spécifier les nouvelles valeurs d'un champ dans l'enregistrement modifié. 
  
Vous pouvez utiliser un **if... Ensuite... Instruction Else** pour effectuer des opérations basées sur une condition. 
  
Pour annuler la modification d'un enregistrement, utilisez l'action **AnnulerModificationEnregistrement**. Cela empêche la validation des modifications et quitte le bloc de données **ModifierEnregistrement**. 
  
Vous pouvez utiliser la variable locale **IdentitéDernierEnregistrementCréé** pour travailler avec le dernier enregistrement créé dans un bloc de données **CréerEnregistrement**. Par exemple, utilisez la syntaxe suivante pour faire référence au champ AssignedTo du dernier enregistrement créé : 
  
`[LastCreateRecordIdentity].[AssignedTo]`


