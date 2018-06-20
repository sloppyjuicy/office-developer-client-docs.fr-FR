---
title: Fonction IIf (accès personnalisé web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 58a24f46-c61d-432a-a957-d831e960795d
description: Vérifie que si une condition est remplie et renvoie une valeur True d’une autre session si elle a la valeur FALSE.
ms.openlocfilehash: 26240735341a316a3aed08a12c42e8b6e7af805f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19781802"
---
# <a name="iif-function-access-custom-web-app"></a>Fonction IIf (accès personnalisé web app)

Vérifie que si une condition est remplie et renvoie une valeur True d’une autre session si elle a la valeur FALSE.
  
> [!IMPORTANT]
> [!IMPORTANTE] Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles. 
  
## <a name="syntax"></a>Syntaxe

**IIf** (*Condition*, *TrueValue*, *FalseValue*) 
  
La fonction **IIf** contient les arguments suivants. 
  
|**Nom de l’argument**|**Description**|
|:-----|:-----|
| *Condition*  <br/> |L’expression que vous souhaitez évaluer.  <br/> |
| *TrueValue*  <br/> |Valeur ou expression renvoyée si *Condition* est True.  <br/> |
| *FalseValue*  <br/> |Valeur ou expression renvoyée si *Condition* a la valeur False.  <br/> |
   
## <a name="example"></a>Exemple

L’expression suivante peut être utilisée pour afficher le nom complet d’une personne où la table contient les champs FirstName, MiddleInitial et LastName. Si le champ « MiddleInitial » est vide, seuls les champs FirstName et LastName sont combinés pour afficher le nom complet.
  
`IIf([MiddleInitial] Is Null,Concat([FirstName]," ",[LastName]),Concat([FirstName]," ",[MiddleInitial]," ",[LastName]))`


