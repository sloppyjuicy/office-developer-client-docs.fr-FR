---
title: Try_Convert Function (Application web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: ea514f19-4742-4eb4-823d-6f2494668106
description: Convertit une valeur en un type de données spécifié ou renvoie la valeur Null si la conversion n’est pas valide.
ms.openlocfilehash: 0e2aa0d877090812494c2aa53a3325ad2217eaa5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59564679"
---
# <a name="try_convert-function-access-custom-web-app"></a>Try_Convert Function (Application web personnalisée Access)

Convertit une valeur en un type de données spécifié ou renvoie la valeur Null si la conversion n’est pas valide.
  
> [!IMPORTANT]
> Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles. 
  
## <a name="syntax"></a>Syntaxe

 **Try_Convert** (*DataType*, *Expression*) 
  
La **Try_Convert** contient les arguments suivants. 
  
|**Nom de l’argument**|**Description**|
|:-----|:-----|
| *DataType*  <br/> |Type de données dans lequel convertir  *Expression*  .  <br/> |
| *Expression*  <br/> |Valeur à convertir.  <br/> |
   
## <a name="remarks"></a>Remarques

 **Try_Convert** prend la valeur qui lui est passée et tente de la convertir en *DataType spécifié.* Si la conversion réussit, **Try_Convert** renvoie la valeur en tant que  *DataType spécifié ;*  si une erreur se produit, la valeur null est renvoyée. Toutefois, si vous demandez une conversion qui n’est explicitement pas autorisée, **Try_Convert** échoue avec une erreur. 
  

