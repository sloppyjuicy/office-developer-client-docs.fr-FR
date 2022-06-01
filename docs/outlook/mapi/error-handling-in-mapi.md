---
title: Gestion des erreurs dans MAPI
description: Décrit la gestion des erreurs dans MAPI, qui, sur les plateformes 32 bits, fonctionne uniquement avec des valeurs HRESULT. Des descriptions des champs encodés dans ces valeurs sont fournies.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 99e2c485-af84-46f4-84b4-fca2117b5a21
ms.openlocfilehash: 1585075d447d73bd5eb132f4378c64c3cbbcbcf7
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65817311"
---
# <a name="error-handling-in-mapi"></a>Gestion des erreurs dans MAPI

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les valeurs de réussite, d’avertissement et d’erreur sont retournées à l’aide d’un nombre 32 bits appelé handle de résultats ou HRESULT. Un HRESULT n’est vraiment pas une poignée à quoi que ce soit; il s’agit simplement d’une valeur 32 bits avec plusieurs champs encodés dans la valeur. Un résultat zéro indique la réussite et un résultat différent de zéro indique l’échec.
  
MAPI sur les plateformes 32 bits fonctionne uniquement avec des valeurs HRESULT.
  
L’illustration suivante montre le format HRESULT pour les plateformes 32 bits.
  
**Format HRESULT**
  
![Format HRESULT](media/amapi_49.gif "Format HRESULT")
  
Le bit d’ordre élevé dans HRESULT indique si la valeur de retour représente la réussite ou l’échec. Si la valeur est égale à zéro, la valeur indique la réussite. Si la valeur est 1, elle indique l’échec.
  
Les bits R, C, N et r sont réservés dans HRESULT.
  
Le champ d’installation dans les deux versions indique la zone de responsabilité de l’erreur. Il existe plusieurs fonctionnalités, mais la grande majorité des erreurs MAPI utilisent FACILITY_ITF pour représenter les erreurs d’interface. Les installations les plus courantes sont les suivantes : FACILITY_NULL, FACILITY_ITF, FACILITY_DISPATCH, FACILITY_RPC et FACILITY_STORAGE. Si de nouvelles installations sont nécessaires, Microsoft les alloue, car elles doivent être uniques. Le tableau suivant décrit les différents champs d’installation.
  
|Facility|Description|
|:-----|:-----|
|FACILITY_NULL  <br/> |Pour les codes d’état courants applicables globalement, tels que S_OK ou E_OUTOF_MEMORY ; la valeur est zéro. |
|FACILITY_ITF  <br/> |Pour la plupart des codes d’état retournés par les méthodes d’interface ; la valeur est définie par l’interface. Autrement dit, deux valeurs HRESULT avec exactement la même valeur 32 bits retournée à partir de deux interfaces différentes peuvent avoir des significations différentes. |
|FACILITY_DISPATCH  <br/> |Pour les erreurs [d’interface IDispatch](https://msdn.microsoft.com/library/ms221608.aspx) de liaison tardive. |
|FACILITY_RPC  <br/> |Pour les codes d’état retournés à partir d’appels de procédure distante. |
|FACILITY_STORAGE  <br/> |Pour les codes d’état retournés à partir d’appels de méthode [IStorage](https://msdn.microsoft.com/library/aa380015%28VS.85%29.aspx) ou [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) relatifs au stockage structuré. Les codes d’état avec des valeurs de code (16 bits inférieurs) dans la plage de codes d’erreur Windows (c’est-à-dire moins de 256) ont la même signification que les erreurs de Windows correspondantes. |
   
Le champ de code est un nombre unique qui est affecté pour représenter l’erreur ou l’avertissement.
  

