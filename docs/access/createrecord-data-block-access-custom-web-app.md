---
title: CreateRecord Data Block (Access custom web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 9dd73bae-a8d5-4d8b-b356-01ac72f7e5d9
description: Vous pouvez utiliser le bloc de données CréerEnregistrement pour créer un nouvel enregistrement dans la table spécifiée.
ms.openlocfilehash: a45aa10c38cd659780cd70cad07a75adccf2d750
ms.sourcegitcommit: b2c5a02b2d0abd2da2542089fc3f83ff07e121e0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2022
ms.locfileid: "63506692"
---
# <a name="createrecord-data-block-access-custom-web-app"></a>CreateRecord Data Block (Access custom web app)

Vous pouvez utiliser le bloc de données **CréerEnregistrement** pour créer un nouvel enregistrement dans la table spécifiée. 
  
> [!IMPORTANT]
> Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles. 
  
> [!NOTE]
> Le bloc de données **CréerEnregistrement** est disponible uniquement dans les macros de données. 
  
## <a name="setting"></a>Setting

Le bloc de données **CréerEnregistrement** utilise les arguments suivants. 
  
Le bloc de données **CréerEnregistrement** utilise les arguments suivants. 
  
|**Nom de l’argument**|**Obligatoire**|**Description**|
|:-----|:-----|:-----|
|**Créer un enregistrement dans** <br/> |Oui  <br/> |Nom de la table dans laquelle créer le nouvel enregistrement. |
|**Alias** <br/> |Non  <br/> |Chaîne qui identifie l’enregistrement. Vous pouvez utiliser l’alias de l’enregistrement pour l’identifier.  <br/> |
   
## <a name="remarks"></a>Remarques

L’enregistrement créé par **CréerEnregistrement** devient automatiquement l’enregistrement actif. 
  
Après **l’instruction CreateRecord** , vous pouvez insérer un bloc de commandes qui s’exécute avant que le nouvel enregistrement ne soit engagé. Les actions suivantes sont disponibles dans un bloc de données **CréerEnregistrement**. 
  
|Opération |
|:-----|
|[Action de macro AnnulerModificationEnregistrement](cancelrecordchange-macro-action-access-custom-web-app.md) <br/> |
|[Instruction de macro Comment](comment-macro-block-access-custom-web-app.md) <br/> |
|[Instruction de macro Group](group-macro-block-access-custom-web-app.md) <br/> |
|[Instruction de macro If... Then... Else](ifthenelse-macro-block-access-custom-web-app.md) <br/> |
|[Action de macro DéfinirChamp](setfield-macro-action-access-custom-web-app.md) <br/> |
|[Action de macro DéfinirVarLocale](setlocalvar-macro-action-access-custom-web-app.md) <br/> |
   
Après que l’action **CréerEnregistrement** a créé un enregistrement, utilisez l’action **DéfinirChamp** pour spécifier une valeur d’un champ dans le nouvel enregistrement. 
  
Vous pouvez utiliser un **if... Ensuite... Instruction Else** pour effectuer des opérations basées sur une condition. 
  
Pour annuler la création d'un enregistrement, utilisez l'action **AnnulerModificationEnregistrement**. Cela empêche la validation des modifications et quitte le bloc de données **CréerEnregistrement**. 
  
Une fois le nouvel enregistrement validé, vous pouvez utiliser la variable locale **IdentitéDernierEnregistrementCréé** pour travailler avec l’enregistrement. Par exemple, utilisez la syntaxe suivante pour faire référence au champ AssignedTo du dernier enregistrement créé. 
  
`[LastCreateRecordIdentity].[AssignedTo]`


