---
title: Obtention et définition de propriétés avec GetProps et SetProps
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 309d2b3d-dc71-4222-b293-4bfc467b5429
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 8bc60dd8241062abb45523393aaf2025ddac03b1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59614114"
---
# <a name="getting-and-setting-properties-with-getprops-and-setprops"></a>Obtention et définition de propriétés avec GetProps et SetProps
 
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Dans la mesure du possible, essayez de récupérer ou de modifier une propriété avec les méthodes [IMAPIProp::GetProps](imapiprop-getprops.md) et [IMAPIProp::SetProps.](imapiprop-setprops.md) À moins que la propriété que vous travaillez avec soit très grande, ces méthodes doivent être adéquates. L’autre solution consiste à lire ou à écrire dans un flux avec l’interface [IStream.](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) Flux gérer des propriétés très importantes avec succès, mais elles drainent davantage les ressources, car elles nécessitent les bibliothèques COM. Utilisez l’interface **IStream** uniquement après l’échec de votre appel à **IMAPIProp::GetProps** ou **IMAPIProp::SetProps.** 
  

