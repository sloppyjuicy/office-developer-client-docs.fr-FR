---
title: Bloc de données RechercherEnregistrement (application Web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 001899f7-5b1a-4c0b-a0e4-e01985eea818
description: Un bloc de données RechercherEnregistrement effectue un ensemble d'actions sur un enregistrement spécifique.
ms.openlocfilehash: a6d89b1700a47f88086fd8c4e7b594b90425912c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32304269"
---
# <a name="lookuprecord-data-block-access-custom-web-app"></a>Bloc de données RechercherEnregistrement (application Web personnalisée Access)

Un bloc de données **RechercherEnregistrement** effectue un ensemble d'actions sur un enregistrement spécifique. 
  
> [!IMPORTANT]
> Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles. 
  
> [!NOTE]
> Le bloc de données **RechercherEnregistrement** est disponible uniquement dans les macros de données. 
  
## <a name="setting"></a>Setting

L’action **DéfinirChamp** utilise les arguments suivants. 
  
|**Argument**|**Obligatoire**|**Description**|
|:-----|:-----|:-----|
| _Dans_ <br/> |Oui  <br/> |Chaîne qui identifie l’enregistrement sur lequel opérer. L'argument *dans* peut contenir le nom de la table, une requête sélection ou une instruction SQL.  <br/> |
| _Condition Where_ <br/> |Non  <br/> |Expression de type Chaîne qui permet de restreindre la plage de données sur laquelle opère le bloc de données **RechercherEnregistrement**. Par exemple, les critères sont souvent équivalents à la clause WHERE dans une expression SQL, sans le mot WHERE. En cas d'omission de critère, le bloc de données **RechercherEnregistrement** opère sur tout le domaine spécifié par l'argument *dans* . Tout champ inclus dans le critère doit également être un champ dans. **  <br/> |
| _Alias_ <br/> |Non  <br/> |Chaîne qui fournit un autre nom pour l'enregistrement spécifié par l'argument *dans* . On l’utilise souvent pour raccourcir le nom de la table pour les références ultérieures, afin d’éviter d’éventuelles références ambiguës. Si *alias* n'est pas spécifié, le nom de la table ou de la requête sera utilisé comme alias.  <br/> |
   
## <a name="remarks"></a>Remarques

Si les critères spécifiés par les arguments  *In*  et  *Condition WHERE*  spécifient plusieurs enregistrements, le bloc de données **RechercherEnregistrement** n'opère que sur le premier enregistrement. 
  
Si aucun enregistrement ne satisfait à la *condition WHERE* ou si *in* ne contient aucun enregistrement, **RechercherEnregistrement** crée un enregistrement vide dans lequel tous les champs contiennent une valeur **null** . 
  

