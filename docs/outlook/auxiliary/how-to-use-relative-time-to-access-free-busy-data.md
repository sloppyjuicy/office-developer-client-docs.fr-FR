---
title: Utiliser l'heure relative pour accéder aux données de disponibilité
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 13aa6ae2-47b9-2cf4-a6ef-651f1338dd49
description: L'interface IFreeBusyData de l'API de disponibilité utilise un concept de temps relatif, qui correspond au nombre de minutes écoulées depuis le 1er janvier 1601, exprimé en temps universel (UTC), et est une valeur de type LONG.
ms.openlocfilehash: 1b977fc3aebd1f2b20e51f24caa36d6bbf2862ba
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317632"
---
# <a name="use-relative-time-to-access-freebusy-data"></a>Utiliser l'heure relative pour accéder aux données de disponibilité

L'interface [IFreeBusyData](ifreebusydata.md) de l'API de disponibilité utilise un concept de temps relatif, qui correspond au nombre de minutes écoulées depuis le 1er janvier 1601, exprimé en temps universel (UTC), et est une valeur de type **long**. 
  
Voici quelques valeurs d'heure relatives couramment utilisées:
  
- `ULONG ulrtmMax = 1525252319L`
    
- `ULONG ulrtmMin = 0L`
    
Utilisez les valeurs de temps relatives maximale et minimale pour vérifier que les valeurs d'heure relatives sont valides.
  
Étant donné que NTFS enregistre les temps de fichier en mode natif au format [fileTime](https://msdn.microsoft.com/library/9baf8a0e-59e3-4fbd-9616-2ec9161520d1%28Office.15%29.aspx) , il peut s'avérer pratique d'utiliser l'exemple de code suivant **** pour convertir l'heure relative en données. 
  
```cpp
static const LONGLONG UnitsPerMinute = 600000000; 
static const LONGLONG UnitsPerHalfMinute = 300000000; 
void RTimeToFileTime(LONG rtime, FILETIME *pft) 
{ 
    Assert(pft != NULL); 
    ULARGE_INTEGER *puli = (ULARGE_INTEGER *)pft; 
    puli->QuadPart = rtime * UnitsPerMinute; 
} 
  
void FileTimeToRTime(FILETIME *pft, LONG* prtime) 
{ 
    Assert(pft != NULL); 
    Assert(prtime != NULL); 
 
    ULARGE_INTEGER uli = *(ULARGE_INTEGER *)pft; 
  
    uli.QuadPart += UnitsPerHalfMinute; 
    uli.QuadPart /= UnitsPerMinute; 
    *prtime = uli.LowPart; 
} 

```

## <a name="see-also"></a>Voir aussi

- [À propos de l'API de type disponible/occupé](about-the-free-busy-api.md)
- [IFreeBusyData](ifreebusydata.md)

