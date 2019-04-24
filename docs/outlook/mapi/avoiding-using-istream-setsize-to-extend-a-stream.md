---
title: Éviter d'utiliser IStreamSetSize pour étendre un flux
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b6de594f-e331-4421-956b-86ee0b5518fe
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 614bb3d142b7aaabe89223b6ce3552469edfce27
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331639"
---
# <a name="avoiding-using-istreamsetsize-to-extend-a-stream"></a>Éviter d'utiliser IStream:: asSetS pour étendre un flux

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Lors de l'écriture dans des flux, il est parfois nécessaire de les agrandir car leur taille initiale n'est plus suffisante. Utilisez la méthode OLE **IStream:: Write** pour effectuer cette opération au lieu de **IStream:: assets**. **IStream:: Write** étend automatiquement le flux, en rendant * * IStream:: * * indésirable. L'appel de **IStream:: Write** sans **IStream:: la méthode sets** peut prendre jusqu'à trois fois plus de temps que l'appel de la **méthode** avant l' **écriture**.
  

