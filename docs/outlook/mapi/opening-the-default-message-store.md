---
title: Ouverture de la banque de messages par défaut
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 670fb896-9aaf-4a96-83f7-76237409e956
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 0b9a1fd73701c663d0477a2e2ebe1a445c5eb54e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59555936"
---
# <a name="opening-the-default-message-store"></a>Ouverture de la banque de messages par défaut

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Dans une session particulière, une seule magasin de messages fait office de magasin de messages par défaut. Une magasin de messages par défaut présente les caractéristiques suivantes :
  
- La **PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md)) est définie sur TRUE.
    
- L STATUS_DEFAULT_STORE est définie dans la **propriété PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).
    
- MAPI crée automatiquement la sous-arbre IPM et les dossiers racine pour les résultats de recherche, les affichages communs et les affichages personnels lorsque la magasin de messages est ouverte. Pour plus d’informations sur ces dossiers, voir [Sous-arbre IPM](ipm-subtree.md) et [Dossiers spéciaux MAPI.](mapi-special-folders.md) 
    
Pour récupérer l’identificateur d’entrée de la magasin de messages par défaut, vous devez appeler [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) pour ouvrir la table de la boutique de messages et appliquer une restriction appropriée dans un appel à [HrQueryAllRows](hrqueryallrows.md). **HrQueryAllRows** retourne un ensemble de lignes avec la seule ligne qui représente la magasin de messages par défaut. La restriction que vous passez à **HrQueryAllRows** peut prendre l’une des formes suivantes : 
  
1. Restriction **AND** qui utilise une structure **SAndRestriction** pour combiner : 
    
   - Il existe une restriction qui utilise une structure **SExistRestriction** pour tester l’existence de **la propriété PR_DEFAULT_STORE.** 
    
   - Restriction de propriété qui utilise une structure [SPropertyRestriction](spropertyrestriction.md) pour vérifier la valeur TRUE dans la **propriété PR_DEFAULT_STORE.** 
    
2. Restriction de masque de bits qui utilise une structure [SBitMaskRestriction](sbitmaskrestriction.md) pour appliquer des STATUS_DEFAULT_STORE en tant que masque à la **propriété PR_RESOURCE_FLAGS.** 
    
## <a name="see-also"></a>Voir aussi

- [SExistRestriction](sexistrestriction.md)
- [SAndRestriction](sandrestriction.md)

