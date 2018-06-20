---
title: Action de Macro OpenPopup (accès personnalisé web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 850de802-e417-4884-8d14-571de52aa391
description: Ouvre le mode spécifié dans une fenêtre contextuelle.
ms.openlocfilehash: 01e0086dc0b54837cf5f095ec6ac5701b5b0b219
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19781952"
---
# <a name="openpopup-macro-action-access-custom-web-app"></a>Action de Macro OpenPopup (accès personnalisé web app)

Ouvre le mode spécifié dans une fenêtre contextuelle.
  
> [!IMPORTANT]
> [!IMPORTANTE] Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles. 
  
## <a name="syntax"></a>Syntaxe

 **OpenPopup** (*Afficher*, *où =*, *Order By*) 
  
L’action **OpenPopup** contient les arguments suivants. 
  
|**Nom de l’argument**|**Description**|
|:-----|:-----|
| *View*  <br/> |Nom de la vue à ouvrir.  <br/> |
| *Où =*  <br/> |Clause SQL WHERE (sans le mot où) qui limite les enregistrements dans l’affichage.  <br/> |
| *Order By*  <br/> |Une expression de chaîne qui inclut le nom du champ ou des champs à partir desquels trier les enregistrements et les mots clés ASC ou DESC facultatifs. Par défaut, cet argument est vide.  <br/> |
   
## <a name="remarks"></a>Remarques

La macro en cours se termine une fois que l’action **OpenPopup** est traitée. 
  
Tout tri ou filtrage appliqué par l’utilisateur est effacé lors de l’action **OpenPopup** est appelée. 
  
L’argument *OrderBy (TriPar)* est le nom du champ ou des champs sur lesquels vous souhaitez trier les enregistrements. Lorsque vous utilisez plusieurs noms de champs, séparez les noms par une virgule (,). 
  
Lorsque vous définissez l’argument *OrderBy* , les enregistrements sont triés par défaut par ordre croissant. 
  

