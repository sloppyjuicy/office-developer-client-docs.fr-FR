---
title: Fonction Try_Convert (application Web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ea514f19-4742-4eb4-823d-6f2494668106
description: ConVertit une valeur en un type de données spécifié ou renvoie la valeur null si la conversion n'est pas valide.
ms.openlocfilehash: 473d9063da46652afa88dc974cb4c4036e1c326c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410895"
---
# <a name="tryconvert-function-access-custom-web-app"></a>Fonction Try_Convert (application Web personnalisée Access)

ConVertit une valeur en un type de données spécifié ou renvoie la valeur null si la conversion n'est pas valide.
  
> [!IMPORTANT]
> Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles. 
  
## <a name="syntax"></a>Syntaxe

 **Try_Convert** (*DataType*, *expression*) 
  
La fonction **Try_Convert** contient les arguments suivants. 
  
|**Nom de l’argument**|**Description**|
|:-----|:-----|
| *DataType*  <br/> |Type de données dans lequel convertir l' *expression* .  <br/> |
| *Expression*  <br/> |Valeur à convertir.  <br/> |
   
## <a name="remarks"></a>Remarques

 **Try_Convert** prend la valeur qui lui est passée et tente de la convertir vers le *type de données* spécifié. Si la conversion réussit, **Try_Convert** renvoie la valeur en tant que *type de données* spécifié; Si une erreur se produit, la valeur null est renvoyée. Toutefois, si vous demandez une conversion qui n'est pas autorisée explicitement, **Try_Convert** échoue avec une erreur. 
  

