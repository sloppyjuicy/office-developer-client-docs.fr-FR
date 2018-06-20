---
title: Bloc de données RechercherEnregistrement (accès personnalisé web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 001899f7-5b1a-4c0b-a0e4-e01985eea818
description: Un bloc de données RechercherEnregistrement effectue un ensemble d’actions sur un enregistrement spécifique.
ms.openlocfilehash: 7012fecdf0e73647b2b8177473dd8b5540b5fcca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19781860"
---
# <a name="lookuprecord-data-block-access-custom-web-app"></a>Bloc de données RechercherEnregistrement (accès personnalisé web app)

Un bloc de données **RechercherEnregistrement** effectue un ensemble d'actions sur un enregistrement spécifique. 
  
> [!IMPORTANT]
> [!IMPORTANTE] Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles. 
  
> [!NOTE]
> [!REMARQUE] Le bloc de données **RechercherEnregistrement** est disponible uniquement dans les macros de données. 
  
## <a name="setting"></a>Paramètre

L'action **DéfinirChamp** utilise les arguments suivants. 
  
|**Argument**|**Obligatoire**|**Description**|
|:-----|:-----|:-----|
| _Dans_ <br/> |Oui  <br/> |Une chaîne qui identifie l’enregistrement à utiliser. L’argument *dans* peut contenir le nom de la table, une requête sélection ou une instruction SQL.  <br/> |
| _Where Condition_ <br/> |Non  <br/> |Une expression de chaîne utilisée pour limiter la plage de données sur lequel le bloc de données **RechercherEnregistrement** est effectuée. Par exemple, critères est souvent équivalent à la clause WHERE d’une expression SQL sans le mot où. Si l’argument critères est omis, le bloc de données **RechercherEnregistrement** opère sur l’intégralité du domaine spécifié par l’argument *dans* . Un champ qui est inclus dans les critères doit également être un champ *dans* .  <br/> |
| _Alias_ <br/> |Non  <br/> |Chaîne qui fournit un autre nom pour l’enregistrement spécifié par l’argument *dans* . Souvent utilisés pour raccourcir le nom de table de références ultérieures éviter d’éventuelles références ambigus. Si *Alias* n’est pas spécifié, le nom de la table ou requête sera utilisé comme alias.  <br/> |
   
## <a name="remarks"></a>Notes

Si les critères spécifiés par les arguments  *In*  et  *Condition WHERE*  spécifient plusieurs enregistrements, le bloc de données **RechercherEnregistrement** n'opère que sur le premier enregistrement. 
  
Si aucun enregistrement ne satisfait à *Condition Where* ou si *In* ne contient aucun enregistrement, **RechercherEnregistrement** crée un enregistrement vide dans lequel tous les champs contiennent une valeur **Null** . 
  

