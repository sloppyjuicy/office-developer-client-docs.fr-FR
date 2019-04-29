---
title: PourChaqueEnregistrement, bloc de données (application Web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 8ffa0de2-5abb-4375-9fb5-042ce3c21506
description: Un bloc de données PourChaqueEnregistrement répète un ensemble d'instructions pour chaque enregistrement dans un domaine.
ms.openlocfilehash: 9715824bff7d478fa2880ada5e8770f7a0c88883
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428234"
---
# <a name="foreachrecord-data-block-access-custom-web-app"></a>PourChaqueEnregistrement, bloc de données (application Web personnalisée Access)

Un bloc de données **PourChaqueEnregistrement** répète un ensemble d'instructions pour chaque enregistrement dans un domaine. 
  
> [!IMPORTANT]
> Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles. 
  
> [!NOTE]
> Le bloc de données **PourChaqueEnregistrement** est disponible uniquement dans les macros de données. 
  
## <a name="setting"></a>Setting

L’action **PourChaqueEnregistrement** utilise les arguments suivants. 
  
|**Nom de l’argument**|**Obligatoire**|**Description**|
|:-----|:-----|:-----|
|**Dans** <br/> |Oui  <br/> |Chaîne qui identifie le domaine d’enregistrements sur lequel opérer. L'argument *dans* peut contenir le nom de la table, une requête sélection ou une instruction SQL.  <br/> **Remarque**: le domaine spécifié ne peut pas inclure de données stockées dans une table liée ou une source de données ODBC.           |
|**Condition Where** <br/> |Non  <br/> |Expression de chaîne servant à limiter la plage de données sur laquelle le bloc de données **PourChaqueEnregistrement** est exécuté. Par exemple, les critères sont souvent équivalents à la clause WHERE dans une expression SQL, sans le mot WHERE. Si les critères sont omis, le bloc de données **PourChaqueEnregistrement** s'applique à l'ensemble du domaine spécifié par l'argument *in* . Tout champ inclus dans le critère doit également être un champ dans. **  <br/> |
|**Alias** <br/> |Non  <br/> |Chaîne qui fournit un autre nom pour le domaine spécifié par l'argument *dans* . On l’utilise souvent pour raccourcir le nom de la table pour les références ultérieures, afin d’éviter d’éventuelles références ambiguës. Si *alias* n'est pas spécifié, le nom de la table ou de la requête sera utilisé comme alias.  <br/> |
   
## <a name="remarks"></a>Remarques

Utilisez l'action **[QuitterPourChaqueEnregistrement](exitforeachrecord-macro-action-access-custom-web-app.md)** pour quitter immédiatement un bloc de données **PourChaqueEnregistrement**. 
  

