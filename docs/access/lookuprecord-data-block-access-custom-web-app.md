---
title: LookupRecord Data Block (Access custom web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: 001899f7-5b1a-4c0b-a0e4-e01985eea818
description: Un bloc de données RechercherEnregistrement effectue un ensemble d'actions sur un enregistrement spécifique.
ms.openlocfilehash: 44146de688b0c45b1f1e8beea3fa7082345e043e
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62780322"
---
# <a name="lookuprecord-data-block-access-custom-web-app"></a>LookupRecord Data Block (Access custom web app)

Un bloc de données **RechercherEnregistrement** effectue un ensemble d'actions sur un enregistrement spécifique.
  
> [!IMPORTANT]
> Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles.
  
> [!NOTE]
> Le bloc de données **RechercherEnregistrement** est disponible uniquement dans les macros de données.
  
## <a name="setting"></a>Setting

L’action **DéfinirChamp** utilise les arguments suivants.
  
|**Argument**|**Obligatoire**|**Description**|
|:-----|:-----|:-----|
| _In_ <br/> |Oui  <br/> |Chaîne qui identifie l’enregistrement sur lequel opérer. *L’argument In* peut contenir le nom de la table, une requête Select ou une SQL instruction. |
| _Condition Where_ <br/> |Non  <br/> |Expression de type Chaîne qui permet de restreindre la plage de données sur laquelle opère le bloc de données **RechercherEnregistrement**. Par exemple, les critères sont souvent équivalents à la clause WHERE dans une expression SQL, sans le mot WHERE. Si des critères sont omis, le bloc de données **LookupRecord** fonctionne sur l’intégralité du domaine spécifié par l’argument *In* . Tout champ inclus dans les critères doit également être un champ dans *In*. |
| _Alias_ <br/> |Non  <br/> |Chaîne qui fournit un autre nom pour l’enregistrement spécifié par l’argument *In* . On l’utilise souvent pour raccourcir le nom de la table pour les références ultérieures, afin d’éviter d’éventuelles références ambiguës. Si *l’alias*  n’est pas spécifié, le nom de la table ou de la requête sera utilisé comme alias. |
   
## <a name="remarks"></a>Remarques

Si les critères spécifiés par les arguments *In* et *Condition WHERE* spécifient plusieurs enregistrements, le bloc de données **RechercherEnregistrement** n’opère que sur le premier enregistrement.
  
Si aucun enregistrement ne satisfait à la *condition Where* ou si *In* ne contient aucun enregistrement, **LookupRecord** crée un enregistrement vide dans lequel tous les champs contiennent une **valeur Null** .
  