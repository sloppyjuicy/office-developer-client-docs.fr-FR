---
title: Bloc de données PourChaqueEnregistrement (accès personnalisé web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 8ffa0de2-5abb-4375-9fb5-042ce3c21506
description: Un bloc de données PourChaqueEnregistrement répète un ensemble d’instructions pour chaque enregistrement dans un domaine.
ms.openlocfilehash: 8ad14a01be05de9fb34299e49a9737f2009ef5ef
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19781836"
---
# <a name="foreachrecord-data-block-access-custom-web-app"></a>Bloc de données PourChaqueEnregistrement (accès personnalisé web app)

Un bloc de données **PourChaqueEnregistrement** répète un ensemble d’instructions pour chaque enregistrement dans un domaine. 
  
> [!IMPORTANT]
> [!IMPORTANTE] Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles. 
  
> [!NOTE]
> [!REMARQUE] Le bloc de données **PourChaqueEnregistrement** est disponible uniquement dans les macros de données. 
  
## <a name="setting"></a>Paramètre

L'action **PourChaqueEnregistrement** utilise les arguments suivants. 
  
|**Nom de l’argument**|**Obligatoire**|**Description**|
|:-----|:-----|:-----|
|**Dans** <br/> |Oui  <br/> |Une chaîne qui identifie le domaine d’enregistrements de fonctionner sur. L’argument *dans* peut contenir le nom de la table, une requête sélection ou une instruction SQL.  <br/> **Remarque**: le domaine spécifié ne peut pas inclure les données stockées dans une table liée ou d’une source de données ODBC.           |
|**Where Condition** <br/> |Non  <br/> |Une expression de chaîne utilisée pour limiter la plage de données sur lequel le bloc de données **PourChaqueEnregistrement** est effectuée. Par exemple, critères est souvent équivalent à la clause WHERE d’une expression SQL sans le mot où. Si les critères sont tous deux omis, le bloc de données **PourChaqueEnregistrement** opère sur l’intégralité du domaine spécifié par l’argument *dans* . Un champ qui est inclus dans les critères doit également être un champ *dans* .  <br/> |
|**Alias** <br/> |Non  <br/> |Chaîne qui fournit un autre nom pour le domaine spécifié par l’argument *dans* . Souvent utilisés pour raccourcir le nom de table de références ultérieures éviter d’éventuelles références ambigus. Si *Alias* n’est pas spécifié, le nom de la table ou requête sera utilisé comme alias.  <br/> |
   
## <a name="remarks"></a>Notes

Utilisez l'action **[QuitterPourChaqueEnregistrement](exitforeachrecord-macro-action-access-custom-web-app.md)** pour quitter immédiatement un bloc de données **PourChaqueEnregistrement**. 
  

