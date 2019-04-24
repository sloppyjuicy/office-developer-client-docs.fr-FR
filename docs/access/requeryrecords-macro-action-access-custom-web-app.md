---
title: RequeryRecords, action de macro (application Web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 1dab102f-24af-4984-8020-a9fb06355639
description: Vous pouvez utiliser l'action RequeryRecords pour actualiser, trier et filtrer les données dans l'affichage actif en actualisant la source de la vue.
ms.openlocfilehash: 69d88401abc0de417f7dc58e275c66f2037212aa
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32311010"
---
# <a name="requeryrecords-macro-action-access-custom-web-app"></a>RequeryRecords, action de macro (application Web personnalisée Access)

Vous pouvez utiliser l'action **RequeryRecords** pour actualiser, trier et filtrer les données dans l'affichage actif en actualisant la source de la vue. 
  
> [!IMPORTANT]
> Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles. 
  
## <a name="setting"></a>Paramètre

L'action **RequeryRecords** utilise les arguments suivants. 
  
|**Paramètre**|**Obligatoire**|**Description**|
|:-----|:-----|:-----|
|**Où =** <br/> |Non  <br/> |Une clause SQL WHERE qui limite les enregistrements dans l'affichage. Par défaut, cet argument est vide.  <br/> |
|**OrderBy** <br/> |Non  <br/> |Une expression de chaîne qui inclut le nom du champ ou des champs à partir desquels trier les enregistrements et les mots clés ASC ou DESC facultatifs. Par défaut, cet argument est vide.  <br/> |
   
## <a name="remarks"></a>Remarques

Tout tri ou filtrage appliqué par l'utilisateur est effacé lors de l'appel de l'action **RequeryRecords** . 
  
L'argument *orderby* est le nom du ou des champs sur lesquels vous souhaitez trier les enregistrements. Lorsque vous utilisez plusieurs noms de champs, séparez-les par une virgule (,). 
  
Lorsque vous définissez l'argument *orderby* , les enregistrements sont triés par défaut dans l'ordre croissant. 
  
Pour trier les enregistrements par ordre décroissant, entrez DESC à la fin de l'expression de l'argument *orderby* . Par exemple, pour trier les enregistrements clients par nom de contact dans l'ordre décroissant, définissez l'argument *orderby* sur «ContactName DESC». 
  
Pour trier les noms par nom décroissant et par ordre croissant, définissez l'argument *orderby* sur «LastName DESC, FirstName ASC». 
  

