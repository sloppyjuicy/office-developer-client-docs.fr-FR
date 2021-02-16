---
title: RequeryRecords Macro Action (Access custom web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 1dab102f-24af-4984-8020-a9fb06355639
description: Vous pouvez utiliser l’action ActualiserEnregistrements pour actualiser, trier et filtrer les données dans l’affichage actif en actualisant la source de l’affichage.
ms.openlocfilehash: 69d88401abc0de417f7dc58e275c66f2037212aa
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439246"
---
# <a name="requeryrecords-macro-action-access-custom-web-app"></a>RequeryRecords Macro Action (Access custom web app)

Vous pouvez utiliser l’action **ActualiserEnregistrements** pour actualiser, trier et filtrer les données dans l’affichage actif en actualisant la source de l’affichage. 
  
> [!IMPORTANT]
> Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles. 
  
## <a name="setting"></a>Paramètre

**L’action RequeryRecords** a les arguments suivants. 
  
|**Paramètre**|**Obligatoire**|**Description**|
|:-----|:-----|:-----|
|**Where=** <br/> |Non  <br/> |A SQL WHERE clause that restricts the records in the view. Par défaut, cet argument est vide.  <br/> |
|**OrderBy** <br/> |Non  <br/> |Une expression de chaîne qui inclut le nom du champ ou des champs à partir desquels trier les enregistrements et les mots clés ASC ou DESC facultatifs. Par défaut, cet argument est vide.  <br/> |
   
## <a name="remarks"></a>Remarques

Tout tri ou filtrage appliqué par l’utilisateur est effacé lorsque l’action **RequeryRecords** est appelée. 
  
*L’argument OrderBy* est le nom du ou des champs sur lesquels vous souhaitez trier les enregistrements. Lorsque vous utilisez plusieurs noms de champs, séparez-les par une virgule (,). 
  
Lorsque vous définissez  *l’argument OrderBy,*  les enregistrements sont triés par défaut dans l’ordre croissant. 
  
Pour trier les enregistrements dans l’ordre décroit, entrez DESC à la fin de l’expression d’argument *OrderBy.* Par exemple, pour trier les enregistrements client par ordre décroit par nom de contact, définissez l’argument  *OrderBy*  sur « ContactName DESC ». 
  
Pour trier les noms par nom décroit et Prénom croissant, définissez l’argument  *OrderBy*  sur « LastName DESC, FirstName ASC ». 
  

