---
title: Fonction Try_Convert (accès personnalisé web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ea514f19-4742-4eb4-823d-6f2494668106
description: Convertit une valeur en un type de données spécifiée ou renvoie la valeur Null si la conversion n’est pas valide.
ms.openlocfilehash: ce942c1f444da7bfcbff76077a5a9d75dd611336
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782018"
---
# <a name="tryconvert-function-access-custom-web-app"></a>Fonction Try_Convert (accès personnalisé web app)

Convertit une valeur en un type de données spécifiée ou renvoie la valeur Null si la conversion n’est pas valide.
  
> [!IMPORTANT]
> [!IMPORTANTE] Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles. 
  
## <a name="syntax"></a>Syntaxe

 **Try_Convert** (*Type de données*, *Expression*) 
  
La fonction **Try_Convert** contient les arguments suivants. 
  
|**Nom de l’argument**|**Description**|
|:-----|:-----|
| *DataType*  <br/> |Le type de données dans lequel convertir *l’Expression* .  <br/> |
| *Expression*  <br/> |La valeur à convertir.  <br/> |
   
## <a name="remarks"></a>Remarques

 **Try_Convert** prend la valeur qui lui sont transmise et tente de convertir le *type de données* de spécifié. Si la conversion réussit, **Try_Convert** renvoie la valeur en tant que le *type de données* d' spécifié ; Si une erreur se produit, la valeur null est renvoyée. Toutefois si vous avez demandé une conversion qui n’est pas explicitement autorisée, **Try_Convert** échoue avec une erreur. 
  

