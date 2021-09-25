---
title: OpenPopup Macro Action (Application web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: 850de802-e417-4884-8d14-571de52aa391
description: Ouvre l’affichage spécifié dans une fenêtre popup.
ms.openlocfilehash: f381389dad13e2a31fa73009118804ed5588c048
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59576813"
---
# <a name="openpopup-macro-action-access-custom-web-app"></a>OpenPopup Macro Action (Application web personnalisée Access)

Ouvre l’affichage spécifié dans une fenêtre popup.
  
> [!IMPORTANT]
> Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles. 
  
## <a name="syntax"></a>Syntaxe

 **OpenPopup** (*View*, *Where=*, *Order By*) 
  
**L’action OuvrirPopup** contient les arguments suivants. 
  
|**Nom de l’argument**|**Description**|
|:-----|:-----|
| *View*  <br/> |Nom de la vue à ouvrir.  <br/> |
| *Where=*  <br/> |Une clause SQL valide (sans le mot WHERE) qui limite les enregistrements dans l’affichage.  <br/> |
| *Trier par*  <br/> |Une expression de chaîne qui inclut le nom du champ ou des champs à partir desquels trier les enregistrements et les mots clés ASC ou DESC facultatifs. Par défaut, cet argument est vide.  <br/> |
   
## <a name="remarks"></a>Remarques

La macro actuelle se termine une fois que **l’action OpenPopup** est traitée. 
  
Tout tri ou filtrage appliqué par l’utilisateur est effacé lorsque l’action **OpenPopup** est appelée. 
  
*L’argument OrderBy* est le nom du ou des champs sur lesquels vous souhaitez trier les enregistrements. Lorsque vous utilisez plusieurs noms de champs, séparez-les par une virgule (,). 
  
Lorsque vous définissez  *l’argument OrderBy,*  les enregistrements sont triés par défaut dans l’ordre croissant. 
  

