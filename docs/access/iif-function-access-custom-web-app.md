---
title: Fonction IIf (application Web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 58a24f46-c61d-432a-a957-d831e960795d
description: Vérifie si une condition est remplie et renvoie une valeur si la valeur est TRUE si elle a la valeur FALSe.
ms.openlocfilehash: 274a923a96b58421f365b03c566a3a1c16b7c48c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439078"
---
# <a name="iif-function-access-custom-web-app"></a>Fonction IIf (application Web personnalisée Access)

Vérifie si une condition est remplie et renvoie une valeur si la valeur est TRUE si elle a la valeur FALSe.
  
> [!IMPORTANT]
> Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles. 
  
## <a name="syntax"></a>Syntaxe

**VraiFaux (IIF** ) (*Condition*, *TrueValue*, *FalseValue*) 
  
La fonction **IIf** contient les arguments suivants. 
  
|**Nom de l’argument**|**Description**|
|:-----|:-----|
| *Condition*  <br/> |Expression à évaluer.  <br/> |
| *TrueValue*  <br/> |Valeur ou expression renvoyée si la *condition* est vraie.  <br/> |
| *FalseValue*  <br/> |Valeur ou expression renvoyée si la *condition* a la valeur false.  <br/> |
   
## <a name="example"></a>Exemple

L'expression suivante peut être utilisée pour afficher le nom complet d'une personne dans laquelle le tableau contient les champs FirstName, MiddleInitial et LastName. Si le champ MiddleInitial est vide, seuls les champs FirstName et LastName sont combinés pour afficher le nom complet.
  
`IIf([MiddleInitial] Is Null,Concat([FirstName]," ",[LastName]),Concat([FirstName]," ",[MiddleInitial]," ",[LastName]))`


