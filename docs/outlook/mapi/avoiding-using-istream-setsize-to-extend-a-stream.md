---
title: Éviter d’utiliser IStreamSetSize pour étendre un flux
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: b6de594f-e331-4421-956b-86ee0b5518fe
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: c4df52e6be76bd7844ed4b16912a4e1d7642edfb
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59584772"
---
# <a name="avoiding-using-istreamsetsize-to-extend-a-stream"></a>Éviter d’utiliser IStream::SetSize pour étendre un flux

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Lors de l’écriture dans des flux, il est parfois nécessaire de les agrandir, car leur taille initiale n’est plus suffisante. Utilisez la méthode OLE **IStream::Write** pour effectuer cette tâche plutôt que **IStream::SetSize**. **IStream::Write** étend automatiquement le flux, ce qui rend ** IStream::SetSize ** inutile. Appeler **IStream::Write** sans **IStream::SetSize** peut être jusqu’à trois fois plus rapide que d’effectuer l’appel **SetSize** avant d’écrire. 
  

