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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401691"
---
# <a name="error-handling-in-mapi"></a>Gestion des erreurs dans MAPI

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les valeurs de réussite, avertissement et d’erreur sont renvoyés en utilisant un nombre 32 bits connu ainsi poignée ou HRESULT. Une valeur HRESULT n’est vraiment pas un handle vers rien ; Il est simplement une valeur 32 bits avec plusieurs champs codé dans la valeur. Un résultat de zéro indique la réussite et un résultat différent de zéro indique l’échec.
  
MAPI sur les plateformes 32 bits fonctionne uniquement avec les valeurs HRESULT.
  
L’illustration suivante montre le format HRESULT pour les plateformes 32 bits.
  
**Format HRESULT**
  
![Format HRESULT] (media/amapi_49.gif "Format HRESULT")
  
Le bit poids fort HRESULT indique si la valeur renvoyée représente a réussi ou échoué. Si la valeur zéro, la valeur indique la réussite. Si la valeur 1, elle indique échec.
  
R, C, N, les bits r sont réservés dans HRESULT.
  
Le champ facility dans les deux versions indique le domaine de responsabilité de l’erreur. Il existe plusieurs fonctions, mais la plupart des erreurs MAPI utiliser FACILITY_ITF pour représenter les erreurs de l’interface. Les fonctionnalités les plus courants qui sont actuellement utilisées sont : FACILITY_NULL, FACILITY_ITF, FACILITY_DISPATCH, FACILITY_RPC et FACILITY_STORAGE. Si les nouvelles installations sont nécessaires, Microsoft les alloue, car ils doivent être uniques. Le tableau suivant décrit les divers champs des immobilisations.
  
|Immobilisations|Description|
|:-----|:-----|
|FACILITY_NULL  <br/> |Pour les codes d’état courant applicables comme S_OK ou E_OUTOF_MEMORY ; la valeur est égale à zéro.  <br/> |
|FACILITY_ITF  <br/> |Pour la plupart des codes d’état renvoyés par les méthodes d’interface ; la valeur est définie par l’interface. Autrement dit, deux valeurs HRESULT avec exactement la même valeur 32 bits renvoyé à partir de deux interfaces différentes peuvent avoir des significations différentes.  <br/> |
|FACILITY_DISPATCH  <br/> |Erreurs d’interface de la liaison tardive [IDispatch](https://msdn.microsoft.com/library/ms221608.aspx) .  <br/> |
|FACILITY_RPC  <br/> |Pour les codes d’état renvoyés par les appels de procédure distante.  <br/> |
|FACILITY_STORAGE  <br/> |Pour les codes d’état renvoyés à partir d’appels de méthode [IStorage](https://msdn.microsoft.com/library/aa380015%28VS.85%29.aspx) ou [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) relatifs au stockage structuré. Codes d’état avec des valeurs de code (16 bits inférieurs) dans les codes d’erreur de plage de Windows (c'est-à-dire, moins de 256) ont la même signification que les erreurs Windows correspondants.  <br/> |
   
Le champ code est un numéro unique assigné pour représenter l’erreur ou avertissement.
  

