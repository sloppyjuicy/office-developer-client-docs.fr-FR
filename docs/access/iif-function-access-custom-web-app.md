---
title: Fonction IIf (application web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 58a24f46-c61d-432a-a957-d831e960795d
description: Vérifie si une condition est remplie et renvoie une valeur si TRUE d’une autre sur si elle est FALSE.
ms.openlocfilehash: 688c17434d9fb8843740989226f82b8a49ee1358
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59593123"
---
# <a name="iif-function-access-custom-web-app"></a>Fonction IIf (application web personnalisée Access)

Vérifie si une condition est remplie et renvoie une valeur si TRUE d’une autre sur si elle est FALSE.
  
> [!IMPORTANT]
> Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles. 
  
## <a name="syntax"></a>Syntaxe

**IIf** (*Condition*, *TrueValue*, *FalseValue*) 
  
La **fonction IIf** contient les arguments suivants. 
  
|**Nom de l’argument**|**Description**|
|:-----|:-----|
| *Condition*  <br/> |Expression que vous souhaitez évaluer.  <br/> |
| *TrueValue*  <br/> |Valeur ou expression renvoyée si  *la condition*  est True.  <br/> |
| *FalseValue*  <br/> |Valeur ou expression renvoyée si  *la condition est*  False.  <br/> |
   
## <a name="example"></a>Exemple

L’expression suivante peut être utilisée pour afficher le nom complet d’une personne où la table contient les champs FirstName, MiddleInitial et LastName. Si le champ MiddleInitial est vide, seuls les champs FirstName et LastName sont combinés pour afficher le nom complet.
  
`IIf([MiddleInitial] Is Null,Concat([FirstName]," ",[LastName]),Concat([FirstName]," ",[MiddleInitial]," ",[LastName]))`


