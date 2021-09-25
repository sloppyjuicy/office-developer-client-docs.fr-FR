---
title: ForEachRecord Data Block (Access custom web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: 8ffa0de2-5abb-4375-9fb5-042ce3c21506
description: Un bloc de données ForEachRecord répète un ensemble d’instructions pour chaque enregistrement d’un domaine.
ms.openlocfilehash: 65c87cfd44796d16310c38da303dfcd3c7c81384
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59601540"
---
# <a name="foreachrecord-data-block-access-custom-web-app"></a>ForEachRecord Data Block (Access custom web app)

Un **bloc de données ForEachRecord** répète un ensemble d’instructions pour chaque enregistrement d’un domaine. 
  
> [!IMPORTANT]
> Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles. 
  
> [!NOTE]
> Le bloc de données **PourChaqueEnregistrement** est disponible uniquement dans les macros de données. 
  
## <a name="setting"></a>Paramètre

L’action **PourChaqueEnregistrement** utilise les arguments suivants. 
  
|**Nom de l’argument**|**Obligatoire**|**Description**|
|:-----|:-----|:-----|
|**In** <br/> |Oui  <br/> |Chaîne qui identifie le domaine d’enregistrements sur lequel opérer. *L’argument In* peut contenir le nom de la table, une requête Select ou une SQL instruction.  <br/> **REMARQUE**: le domaine spécifié ne peut pas inclure les données stockées dans une table liée ou une source de données ODBC.           |
|**Condition Where** <br/> |Non  <br/> |Expression de chaîne utilisée pour limiter la plage de données sur laquelle le bloc de données **ForEachRecord** est effectué. Par exemple, les critères sont souvent équivalents à la clause WHERE dans une expression SQL, sans le mot WHERE. Si des critères sont omis, le bloc de données **ForEachRecord** fonctionne sur l’intégralité du domaine spécifié par l’argument *In.* Tout champ inclus dans les critères doit également être un champ *dans .*  <br/> |
|**Alias** <br/> |Non  <br/> |Chaîne qui fournit un autre nom pour le domaine spécifié par l’argument *In.* On l’utilise souvent pour raccourcir le nom de la table pour les références ultérieures, afin d’éviter d’éventuelles références ambiguës. Si  *l’alias*  n’est pas spécifié, le nom de la table ou de la requête sera utilisé comme alias.  <br/> |
   
## <a name="remarks"></a>Remarques

Utilisez l'action **[QuitterPourChaqueEnregistrement](exitforeachrecord-macro-action-access-custom-web-app.md)** pour quitter immédiatement un bloc de données **PourChaqueEnregistrement**. 
  

