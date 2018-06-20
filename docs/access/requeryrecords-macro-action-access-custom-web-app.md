---
title: Action de Macro RequeryRecords (accès personnalisé web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 1dab102f-24af-4984-8020-a9fb06355639
description: Vous pouvez utiliser l’action RequeryRecords pour actualiser, trier et filtrer les données dans l’affichage actif en actualisant la source de l’affichage.
ms.openlocfilehash: 27c6a4f62f62f6d903de7a23d2aca6db8d316a84
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19781970"
---
# <a name="requeryrecords-macro-action-access-custom-web-app"></a>Action de Macro RequeryRecords (accès personnalisé web app)

Vous pouvez utiliser l’action **RequeryRecords** pour actualiser, trier et filtrer les données dans l’affichage actif en actualisant la source de l’affichage. 
  
> [!IMPORTANT]
> [!IMPORTANTE] Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles. 
  
## <a name="setting"></a>Valeur

L’action **RequeryRecords** possède les arguments suivants. 
  
|**Paramètre**|**Obligatoire**|**Description**|
|:-----|:-----|:-----|
|**Où =** <br/> |Non  <br/> |Une clause WHERE SQL qui limite les enregistrements dans l’affichage. Par défaut, cet argument est vide.  <br/> |
|**OrderBy** <br/> |Non  <br/> |Une expression de chaîne qui inclut le nom du champ ou des champs à partir desquels trier les enregistrements et les mots clés ASC ou DESC facultatifs. Par défaut, cet argument est vide.  <br/> |
   
## <a name="remarks"></a>Remarques

Tout tri ou filtrage appliqué par l’utilisateur est effacé lors de l’action **RequeryRecords** est appelée. 
  
L’argument *OrderBy (TriPar)* est le nom du champ ou des champs sur lesquels vous souhaitez trier les enregistrements. Lorsque vous utilisez plusieurs noms de champs, séparez les noms par une virgule (,). 
  
Lorsque vous définissez l’argument *OrderBy* , les enregistrements sont triés par défaut par ordre croissant. 
  
Pour trier les enregistrements dans l’ordre décroissant, saisissez DESC à la fin de l’expression d’argument *OrderBy (TriPar)* . Par exemple, pour trier les enregistrements clients dans l’ordre décroissant par contact, définissez l’argument *OrderBy* sur « ContactName DESC ». 
  
Pour trier les noms par ordre décroissant de LastName et FirstName croissant, définissez l’argument *OrderBy* sur « LastName DESC, FirstName ASC ». 
  

