---
title: Gestion des erreurs dans MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 99e2c485-af84-46f4-84b4-fca2117b5a21
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 98ee0856411cce3a3e9012185be6c30503de7779
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287278"
---
# <a name="error-handling-in-mapi"></a>Gestion des erreurs dans MAPI

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les valeurs de réussite, d'avertissement et d'erreur sont renvoyées à l'aide d'un nombre 32 bits appelé handle de résultat, ou HRESULT. Un HRESULT n'est pas un descripteur de rien; Il s'agit simplement d'une valeur de 32 bits avec plusieurs champs codés dans la valeur. Un résultat nul indique la réussite et un résultat différent de zéro indique un échec.
  
MAPI sur les plateformes 32 bits fonctionne uniquement avec les valeurs HRESULT.
  
L'illustration suivante montre le format HRESULT pour les plateformes 32 bits.
  
**Format HRESULT**
  
![Format HRESULT] (media/amapi_49.gif "Format HRESULT")
  
Le bit de poids fort dans le HRESULT indique si la valeur de retour représente la réussite ou l'échec. Si la valeur est égale à zéro, la valeur indique Success. Si ce paramètre est défini sur 1, il indique un échec.
  
Les bits R, C, N et r sont réservés dans le HRESULT.
  
Le champ Facility dans les deux versions indique le domaine de responsabilité de l'erreur. Il existe plusieurs fonctionnalités, mais la plupart des erreurs MAPI utilisent FACILITY_ITF pour représenter les erreurs d'interface. Les installations les plus courantes actuellement utilisées sont les suivantes: FACILITY_NULL, FACILITY_ITF, FACILITY_DISPATCH, FACILITY_RPC et FACILITY_STORAGE. Si de nouvelles installations sont nécessaires, Microsoft les alloue car elles doivent être uniques. Le tableau suivant décrit les différents champs de l'utilitaire.
  
|Facility|Description|
|:-----|:-----|
|FACILITY_NULL  <br/> |Pour les codes d'État communs largement applicables, tels que S_OK ou E_OUTOF_MEMORY; la valeur est zéro.  <br/> |
|FACILITY_ITF  <br/> |Pour la plupart des codes d'État renvoyés par les méthodes d'interface; la valeur est définie par l'interface. En d'autres termes, deux valeurs HRESULT avec exactement la même valeur 32 bits renvoyée à partir de deux interfaces différentes peuvent avoir des significations différentes.  <br/> |
|FACILITY_DISPATCH  <br/> |Pour les erreurs d'interface [IDispatch](https://msdn.microsoft.com/library/ms221608.aspx) de liaison tardive.  <br/> |
|FACILITY_RPC  <br/> |Pour les codes d'État renvoyés par les appels de procédure distante.  <br/> |
|FACILITY_STORAGE  <br/> |Pour les codes d'État renvoyés par les appels de méthode [IStorage](https://msdn.microsoft.com/library/aa380015%28VS.85%29.aspx) ou [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) liés au stockage structuré. Les codes d'État avec des valeurs code (16 bits inférieurs) comprises dans la plage des codes d'erreur Windows (autrement dit, inférieurs à 256) ont la même signification que les erreurs Windows correspondantes.  <br/> |
   
Le champ Code est un numéro unique qui est affecté pour représenter l'erreur ou l'avertissement.
  

