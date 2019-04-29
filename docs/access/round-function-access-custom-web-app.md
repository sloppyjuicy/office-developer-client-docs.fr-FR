---
title: Fonction Round (application Web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4af7fbe2-ee34-4a52-b55e-ce3983313b5e
description: Renvoie une valeur numérique, arrondie ou tronquée, à la longueur ou à la précision spécifiée.
ms.openlocfilehash: 0afab8c3434aef58c4bb25aee22eefd95732797b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413744"
---
# <a name="round-function-access-custom-web-app"></a>Fonction Round (application Web personnalisée Access)

Renvoie une valeur numérique, arrondie ou tronquée, à la longueur ou à la précision spécifiée.
  
> [!IMPORTANT]
> Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles. 
  
## <a name="syntax"></a>Syntaxe

 **Arrondi** (*Nombre*, *précision* , [ *TruncateInsteadOfRound* ]) 
  
La fonction **Round** contient les arguments suivants. 
  
|**Nom de l’argument**|**Description**|
|:-----|:-----|
| *Number*  <br/> |Expression numérique.  <br/> |
| *Dell*  <br/> |Précision à laquelle le *nombre* doit être arrondi.  La *précision* doit être une expression numérique. Lorsque la *précision* est un nombre positif, le *nombre* est arrondi au nombre de positions décimales spécifié par la longueur. Lorsque la *précision* est un nombre négatif, le *nombre* est arrondi à gauche du séparateur décimal, comme spécifié par longueur.  <br/> |
| *TruncateInsteadOfRound*  <br/> |Type d'opération à effectuer. Si cet argument est omis ou défini sur 0, le *nombre* est arrondi. Lorsqu'une valeur autre que 0 est spécifiée, le *nombre* est tronqué. La valeur par défaut est 0.  <br/> |
   
## <a name="remarks"></a>Remarques

 **Round** renvoie toujours une valeur. Si le paramètre longueur est négatif et supérieur au nombre de chiffres avant le séparateur décimal, **Round** renvoie 0. 
  

