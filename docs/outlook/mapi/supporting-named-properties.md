---
title: Prise en charge des propriétés nommées
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 2e742ecd-2dcd-46a8-9d4e-2cec2c6f795e
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: b989517b38f939796db40291c7a0211c8d3f37fe
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59578542"
---
# <a name="supporting-named-properties"></a>Prise en charge des propriétés nommées

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Any object that implements the [IMAPIProp : IUnknown](imapipropiunknown.md) interface can support named properties. La prise en charge des propriétés nommées est requise pour : 
  
- Fournisseurs de carnets d’adresses qui permettent la copie d’entrées d’autres fournisseurs dans leurs conteneurs.
    
- Fournisseurs de magasins de messages qui peuvent être utilisés pour créer des types de messages arbitraires.
    
La prise en charge des propriétés nommées est facultative pour tous les autres fournisseurs de services. Les fournisseurs de services qui ne supportent pas les propriétés nommées doivent implémenter le mappage nom à identificateur dans les méthodes [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) et [IMAPIProp::GetIDsFromNames.](imapiprop-getidsfromnames.md) Les clients appellent **GetNamesFromIDs** pour récupérer les noms correspondants pour un ou plusieurs identificateurs de propriété dans la plage de 0x8000 et **GetIDsFromNames** pour créer ou récupérer les identificateurs d’un ou plusieurs noms. 
  
Les fournisseurs de services qui ne peuvent pas prendre en charge les propriétés nommées doivent :
  
- Échouez les appels [à IMAPIProp::SetProps](imapiprop-setprops.md) pour définir des propriétés avec des identificateurs de 0x8000 ou supérieur en renvoyant les MAPI_E_UNEXPECTED_ID dans le tableau [SPropProblem.](spropproblem.md) 
    
- Renvoyer MAPI_E_NO_SUPPORT à partir des méthodes [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) et [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) . 
    

