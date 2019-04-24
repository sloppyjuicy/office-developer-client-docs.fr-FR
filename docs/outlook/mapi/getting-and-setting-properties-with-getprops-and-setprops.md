---
title: Obtention et définition de propriétés avec GetProps et SetProps
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 309d2b3d-dc71-4222-b293-4bfc467b5429
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 7d11f69c6da8560f5879ebc38498d852486bed8b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299397"
---
# <a name="getting-and-setting-properties-with-getprops-and-setprops"></a>Obtention et définition de propriétés avec GetProps et SetProps
 
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Dans la mesure du possible, essayez de récupérer ou de modifier une propriété avec les méthodes [IMAPIProp:: GetProps](imapiprop-getprops.md) et [IMAPIProp:: SetProps](imapiprop-setprops.md) . À moins que la propriété avec laquelle vous travaillez ne soit très volumineuse, ces méthodes doivent être appropriées. L'autre solution consiste à lire ou écrire dans un flux à l'aide de l'interface [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) . Les flux peuvent gérer correctement les propriétés très volumineuses, mais ils sont plus déchargés des ressources, car ils nécessitent les bibliothèques COM. Utilisez l'interface **IStream** uniquement après l'échec de votre appel à **IMAPIProp:: GetProps** ou **IMAPIProp:: SetProps** . 
  

