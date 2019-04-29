---
title: Ouverture de la banque de messages par défaut
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 670fb896-9aaf-4a96-83f7-76237409e956
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: d8e620516e2b3e61cd07f3a08af989cc4ed5b61e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436026"
---
# <a name="opening-the-default-message-store"></a>Ouverture de la banque de messages par défaut

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Dans une session particulière, un magasin de messages agit comme la Banque de messages par défaut. Une banque de messages par défaut présente les caractéristiques suivantes:
  
- La propriété **PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md)) est définie sur true.
    
- L'indicateur STATUS_DEFAULT_STORE est défini dans la propriété **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).
    
- MAPI crée automatiquement la sous-arborescence IPM et les dossiers racine pour les résultats de recherche, les affichages courants et les vues personnelles lors de l'ouverture de la Banque de messages. Pour plus d'informations sur ces dossiers, consultez la rubrique [IPM subtree](ipm-subtree.md) and [MAPI Special Folders](mapi-special-folders.md). 
    
Pour récupérer l'identificateur d'entrée pour la Banque de messages par défaut, vous devez appeler [IMAPISession:: GetMsgStoresTable](imapisession-getmsgstorestable.md) pour ouvrir la table de banque de messages et appliquer une restriction appropriée dans un appel à [HrQueryAllRows](hrqueryallrows.md). **HrQueryAllRows** renverra un jeu de lignes avec la ligne qui représente la Banque de messages par défaut. La restriction que vous transmettez à **HrQueryAllRows** peut prendre l'une des formes suivantes: 
  
1. Une restriction **et** qui utilise une structure **SAndRestriction** pour combiner: 
    
   - Une restriction Exists qui utilise une structure **SExistRestriction** pour tester l'existence de la propriété **PR_DEFAULT_STORE** . 
    
   - Une restriction de propriété qui utilise une structure [SPropertyRestriction](spropertyrestriction.md) pour vérifier la valeur true dans la propriété **PR_DEFAULT_STORE** . 
    
2. Une restriction de masque de masque qui utilise une structure [SBitMaskRestriction](sbitmaskrestriction.md) pour l'application de STATUS_DEFAULT_STORE en tant que masque à la propriété **PR_RESOURCE_FLAGS** . 
    
## <a name="see-also"></a>Voir aussi

- [SExistRestriction](sexistrestriction.md)
- [SAndRestriction](sandrestriction.md)

