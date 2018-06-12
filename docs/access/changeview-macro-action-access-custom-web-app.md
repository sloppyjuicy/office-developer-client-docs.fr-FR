---
title: Action de Macro ChangeView (accès personnalisé web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7eb20f21-0218-4a2c-9bbc-90218a1e87bc
description: Vous pouvez utiliser l’action ChangeView pour naviguer entre les vues en place.
ms.openlocfilehash: c420846074ef362d3388d40ed8700db0739b7ce0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19781831"
---
# <a name="changeview-macro-action-access-custom-web-app"></a>Action de Macro ChangeView (accès personnalisé web app)

Vous pouvez utiliser l’action **ChangeView** pour naviguer entre les vues en place. 
  
> [!IMPORTANT]
> [!IMPORTANTE] Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles. 
  
## <a name="setting"></a>Valeur

L’action **ChangeView** possède les arguments suivants. 
  
|**Argument de l'action**|**Obligatoire**|**Description**|
|:-----|:-----|:-----|
|Table  <br/> |Oui  <br/> |Le nom de la table à ouvrir.  <br/> |
|Vue  <br/> |Oui  <br/> |Nom de la vue à ouvrir.  <br/> |
|Où  <br/> |Non  <br/> |Spécifié, remplace la condition Where de la source de l'enregistrement de l'objet.  <br/> |
|Order By  <br/> |Non  <br/> |Une expression de chaîne qui inclut le nom du champ ou des champs à partir desquels trier les enregistrements et les mots clés ASC ou DESC facultatifs. Par défaut, cet argument est vide.  <br/> |
   
## <a name="remarks"></a>Note

Tout tri ou filtrage appliqué par l’utilisateur est effacé lors de l’action **ChangeView** est appelée. 
  
L’argument *OrderBy (TriPar)* est le nom du champ ou des champs sur lesquels vous souhaitez trier les enregistrements. Lorsque vous utilisez plusieurs noms de champs, séparez les noms par une virgule (,). 
  
Lorsque vous définissez l’argument *OrderBy* , les enregistrements sont triés par défaut par ordre croissant. 
  

