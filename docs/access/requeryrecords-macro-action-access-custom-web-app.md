---
title: RequeryRecords Macro Action (Access custom web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: 1dab102f-24af-4984-8020-a9fb06355639
description: Vous pouvez utiliser l’action ActualiserEnregistrements pour actualiser, trier et filtrer les données dans l’affichage actif en actualisant la source de l’affichage.
ms.openlocfilehash: 5d6e41b3f2ffbf4a429e3744937bf2fbeae4918b
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62780343"
---
# <a name="requeryrecords-macro-action-access-custom-web-app"></a>RequeryRecords Macro Action (Access custom web app)

Vous pouvez utiliser l’action **ActualiserEnregistrements** pour actualiser, trier et filtrer les données dans l’affichage actif en actualisant la source de l’affichage.
  
> [!IMPORTANT]
> Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles.
  
## <a name="setting"></a>Paramètre

**L’action RequeryRecords** a les arguments suivants.
  
|**Paramètre**|**Obligatoire**|**Description**|
|:-----|:-----|:-----|
|**Where=** <br/> |Non  <br/> |Une SQL where qui restreint les enregistrements dans l’affichage. Par défaut, cet argument est vide. |
|**OrderBy** <br/> |Non  <br/> |Une expression de chaîne qui inclut le nom du champ ou des champs à partir desquels trier les enregistrements et les mots clés ASC ou DESC facultatifs. Par défaut, cet argument est vide. |

## <a name="remarks"></a>Remarques

Tout tri ou filtrage appliqué par l’utilisateur est effacé lorsque l’action **RequeryRecords** est appelée.
  
*L’argument OrderBy* est le nom du ou des champs sur lesquels vous souhaitez trier les enregistrements. Lorsque vous utilisez plusieurs noms de champs, séparez-les par une virgule (,).
  
Lorsque vous définissez *l’argument OrderBy* , les enregistrements sont triés par défaut dans l’ordre croissant.
  
Pour trier les enregistrements dans l’ordre décroit, entrez DESC à la fin de l’expression d’argument *OrderBy* . Par exemple, pour trier les enregistrements client par ordre décroit par nom de contact, définissez l’argument *OrderBy* sur « ContactName DESC ».
  
Pour trier les noms par nom décroit et Prénom croissant, définissez l’argument *OrderBy* sur « LastName DESC, FirstName ASC ».
  