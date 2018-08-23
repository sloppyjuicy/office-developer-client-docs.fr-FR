---
title: Obtention et définition des propriétés avec GetProps et SetProps
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 309d2b3d-dc71-4222-b293-4bfc467b5429
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 6b54be711d8c33648d211e480c6a00ee92755108
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575566"
---
# <a name="getting-and-setting-properties-with-getprops-and-setprops"></a>Obtention et définition des propriétés avec GetProps et SetProps
 
**S’applique à**: Outlook 2013 | Outlook 2016 
  
La mesure du possible, essayez d’extraire ou de modifier une propriété avec les méthodes [IMAPIProp::GetProps](imapiprop-getprops.md) et [IMAPIProp::SetProps](imapiprop-setprops.md) . Sauf si la propriété que vous utilisez est très volumineuse, ces méthodes doivent être adéquates. L’autre solution consiste à lire ou écrire dans un stream à l’interface [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) . Flux peuvent gérer des propriétés très volumineuses avec succès, mais ils sont une charge supérieure pour les ressources car ils ont besoin les bibliothèques COM. Utiliser l’interface **IStream** uniquement après l’appel de **IMAPIProp::GetProps** ou **IMAPIProp::SetProps** échoue. 
  

