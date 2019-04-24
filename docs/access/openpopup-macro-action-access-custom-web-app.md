---
title: OpenPopup, action de macro (application Web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 850de802-e417-4884-8d14-571de52aa391
description: Ouvre l'affichage spécifié dans une fenêtre contextuelle.
ms.openlocfilehash: 2a8b67fcbf31c42f13b36f06d14d9d046be68c68
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308112"
---
# <a name="openpopup-macro-action-access-custom-web-app"></a>OpenPopup, action de macro (application Web personnalisée Access)

Ouvre l'affichage spécifié dans une fenêtre contextuelle.
  
> [!IMPORTANT]
> Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles. 
  
## <a name="syntax"></a>Syntaxe

 **OpenPopup** (*View*, *Where =*, *order by*) 
  
L'action **OpenPopup** contient les arguments suivants. 
  
|**Nom de l’argument**|**Description**|
|:-----|:-----|
| *View*  <br/> |Nom de la vue à ouvrir.  <br/> |
| *Où =*  <br/> |Une clause SQL WHERE valide (sans le mot WHERE) qui limite les enregistrements dans l'affichage.  <br/> |
| *Trier par*  <br/> |Une expression de chaîne qui inclut le nom du champ ou des champs à partir desquels trier les enregistrements et les mots clés ASC ou DESC facultatifs. Par défaut, cet argument est vide.  <br/> |
   
## <a name="remarks"></a>Remarques

La macro active se termine une fois l'action **OpenPopup** traitée. 
  
Tout tri ou filtrage appliqué par l'utilisateur est effacé lors de l'appel de l'action **OpenPopup** . 
  
L'argument *orderby* est le nom du ou des champs sur lesquels vous souhaitez trier les enregistrements. Lorsque vous utilisez plusieurs noms de champs, séparez-les par une virgule (,). 
  
Lorsque vous définissez l'argument *orderby* , les enregistrements sont triés par défaut dans l'ordre croissant. 
  

