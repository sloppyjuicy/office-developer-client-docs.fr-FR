---
title: Gestion des erreurs dans MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 99e2c485-af84-46f4-84b4-fca2117b5a21
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 98ee0856411cce3a3e9012185be6c30503de7779
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287278"
---
# <a name="error-handling-in-mapi"></a>Gestion des erreurs dans MAPI

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les valeurs de réussite, d’avertissement et d’erreur sont renvoyées à l’aide d’un nombre 32 bits appelé handle de résultats, ou HRESULT. Un HRESULT n’est vraiment pas un handle vers quoi que ce soit ; Il s’agit simplement d’une valeur 32 bits avec plusieurs champs codés dans la valeur. Un résultat zéro indique un succès et un résultat non nul indique un échec.
  
MAPI sur les plateformes 32 bits fonctionne uniquement avec les valeurs HRESULT.
  
L’illustration suivante montre le format HRESULT pour les plateformes 32 bits.
  
**Format HRESULT**
  
![Format HRESULT au](media/amapi_49.gif "format HRESULT")
  
Le bit d’ordre élevé dans hrESULT indique si la valeur de retour représente la réussite ou l’échec. Si la valeur est définie sur zéro, la valeur indique la réussite. S’il est définie sur 1, elle indique un échec.
  
Les bits R, C, N et r sont réservés dans hrESULT.
  
Le champ de la facilité dans les deux versions indique la zone de responsabilité de l’erreur. Il existe plusieurs installations, mais la grande majorité des erreurs MAPI utilisent FACILITY_ITF pour représenter des erreurs d’interface. Les installations les plus courantes actuellement utilisées sont les FACILITY_NULL, FACILITY_ITF, FACILITY_DISPATCH, FACILITY_RPC et FACILITY_STORAGE. Si de nouvelles installations sont nécessaires, Microsoft les alloue, car elles doivent être uniques. Le tableau suivant décrit les différents champs d’installation.
  
|Facility|Description|
|:-----|:-----|
|FACILITY_NULL  <br/> |Pour les codes d’état courants applicables à grande S_OK ou E_OUTOF_MEMORY ; la valeur est zéro.  <br/> |
|FACILITY_ITF  <br/> |Pour la plupart des codes d’état renvoyés par les méthodes d’interface ; la valeur est définie par l’interface. Autrement dit, deux valeurs HRESULT avec exactement la même valeur 32 bits renvoyées à partir de deux interfaces différentes peuvent avoir des significations différentes.  <br/> |
|FACILITY_DISPATCH  <br/> |Pour les erreurs d’interface [IDispatch de](https://msdn.microsoft.com/library/ms221608.aspx) liaison tardive.  <br/> |
|FACILITY_RPC  <br/> |Pour les codes d’état renvoyés par les appels de procédure distante.  <br/> |
|FACILITY_STORAGE  <br/> |Pour les codes d’état renvoyés par les appels de méthode [IStorage](https://msdn.microsoft.com/library/aa380015%28VS.85%29.aspx) ou [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) relatifs au stockage structuré. Les codes d’état avec des valeurs de code (moins de 16 bits) dans la plage de codes d’erreur Windows (c’est-à-dire, inférieur à 256) ont la même signification que les erreurs de Windows correspondantes.  <br/> |
   
Le champ de code est un numéro unique affecté pour représenter l’erreur ou l’avertissement.
  

