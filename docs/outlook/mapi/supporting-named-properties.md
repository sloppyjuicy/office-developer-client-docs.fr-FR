---
title: Prise en charge des propriétés nommées
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2e742ecd-2dcd-46a8-9d4e-2cec2c6f795e
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 983cbaf4d3523bf1e5370e5ad3119ab8c1490f8e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787294"
---
# <a name="supporting-named-properties"></a>Prise en charge des propriétés nommées

  
  
**S’applique à**: Outlook 
  
Any object that implements the [IMAPIProp : IUnknown](imapipropiunknown.md) interface can support named properties. Prise en charge des propriétés nommées est requis pour : 
  
- Fournisseurs de carnet d’adresses qui autorisent les entrées à partir d’autres fournisseurs doivent être copiés dans leurs conteneurs.
    
- Fournisseurs qui peuvent servir à créer des types de message arbitraire de banque de messages.
    
Prise en charge de la propriété nommée est facultatif pour tous les autres fournisseurs de services. Fournisseurs de services qui prennent en charge des propriétés nommées doivent implémenter les méthodes [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) et [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) mappage à-identificateur de nom. Clients appeler **GetNamesFromIDs** pour récupérer les noms correspondants pour un ou plusieurs identificateurs de propriété dans la plage 0 x 8000 plus et **GetIDsFromNames** pour créer ou extraire les identificateurs pour un ou plusieurs noms. 
  
Fournisseurs de services ne prenant pas en charge les propriétés nommées doivent :
  
- Échec des appels [IMAPIProp::SetProps](imapiprop-setprops.md) pour définir des propriétés avec des identificateurs supérieure ou égale à 0 x 8000 à retourner MAPI_E_UNEXPECTED_ID dans le tableau de [SPropProblem](spropproblem.md) . 
    
- Retourner MAPI_E_NO_SUPPORT des méthodes [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) et [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) . 
    

