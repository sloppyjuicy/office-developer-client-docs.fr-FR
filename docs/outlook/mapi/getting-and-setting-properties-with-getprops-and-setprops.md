---
title: Obtention et définition de propriétés avec GetProps et SetProps
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 309d2b3d-dc71-4222-b293-4bfc467b5429
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 7d11f69c6da8560f5879ebc38498d852486bed8b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299397"
---
# <a name="getting-and-setting-properties-with-getprops-and-setprops"></a>Obtention et définition de propriétés avec GetProps et SetProps
 
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Dans la mesure du possible, essayez de récupérer ou de modifier une propriété avec les méthodes [IMAPIProp::GetProps](imapiprop-getprops.md) et [IMAPIProp::SetProps.](imapiprop-setprops.md) À moins que la propriété que vous travaillez avec soit très grande, ces méthodes doivent être adéquates. L’autre solution consiste à lire ou à écrire dans un flux avec l’interface [IStream.](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) Flux gérer des propriétés très importantes avec succès, mais elles drainent davantage les ressources, car elles nécessitent les bibliothèques COM. Utilisez l’interface **IStream** uniquement après l’échec de votre appel à **IMAPIProp::GetProps** ou **IMAPIProp::SetProps.** 
  

