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
# <a name="use-relative-time-to-access-freebusy-data"></a><span data-ttu-id="1e0f3-103">Utiliser l'heure relative pour accéder aux données de disponibilité</span><span class="sxs-lookup"><span data-stu-id="1e0f3-103">Use relative time to access free/busy data</span></span>

<span data-ttu-id="1e0f3-104">L'interface [IFreeBusyData](ifreebusydata.md) de l'API de disponibilité utilise un concept de temps relatif, qui correspond au nombre de minutes écoulées depuis le 1er janvier 1601, exprimé en temps universel (UTC), et est une valeur de type **long**.</span><span class="sxs-lookup"><span data-stu-id="1e0f3-104">The [IFreeBusyData](ifreebusydata.md) interface in the Free/Busy API uses a concept of relative time, which is the number of minutes since January 1, 1601, expressed in Universal Time (UTC), and is a value of type **LONG**.</span></span> 
  
<span data-ttu-id="1e0f3-105">Voici quelques valeurs d'heure relatives couramment utilisées:</span><span class="sxs-lookup"><span data-stu-id="1e0f3-105">The following are some commonly used relative time values:</span></span>
  
- `ULONG ulrtmMax = 1525252319L`
    
- `ULONG ulrtmMin = 0L`
    
<span data-ttu-id="1e0f3-106">Utilisez les valeurs de temps relatives maximale et minimale pour vérifier que les valeurs d'heure relatives sont valides.</span><span class="sxs-lookup"><span data-stu-id="1e0f3-106">Use the preceding maximum and minimum relative time values to help verify that your relative time values are valid.</span></span>
  
<span data-ttu-id="1e0f3-107">Étant donné que NTFS enregistre les temps de fichier en mode natif au format [fileTime](https://msdn.microsoft.com/library/9baf8a0e-59e3-4fbd-9616-2ec9161520d1%28Office.15%29.aspx) , il peut s'avérer pratique d'utiliser l'exemple de code suivant \*\*\*\* pour convertir l'heure relative en données.</span><span class="sxs-lookup"><span data-stu-id="1e0f3-107">Because NTFS records file times natively in [FILETIME](https://msdn.microsoft.com/library/9baf8a0e-59e3-4fbd-9616-2ec9161520d1%28Office.15%29.aspx) format, it might be handy to use the following code example to convert relative time to and from **FILETIME**.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="1e0f3-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1e0f3-108">See also</span></span>

- [<span data-ttu-id="1e0f3-109">À propos de l'API de type disponible/occupé</span><span class="sxs-lookup"><span data-stu-id="1e0f3-109">About the Free/Busy API</span></span>](about-the-free-busy-api.md)
- [<span data-ttu-id="1e0f3-110">IFreeBusyData</span><span class="sxs-lookup"><span data-stu-id="1e0f3-110">IFreeBusyData</span></span>](ifreebusydata.md)

