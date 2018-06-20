---
title: Ouverture de la banque de messages par défaut
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 670fb896-9aaf-4a96-83f7-76237409e956
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 1eb4e150be68ea01060c7afaed489c8759b576db
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784917"
---
# <a name="opening-the-default-message-store"></a>Ouverture de la banque de messages par défaut

**S’applique à**: Outlook 
  
Dans une session particulière, une banque de messages joue de la banque de messages par défaut. Une banque de messages par défaut présente les caractéristiques suivantes :
  
- La propriété **PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md)) est définie sur TRUE.
    
- L’indicateur STATUS_DEFAULT_STORE est défini dans la propriété **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).
    
- MAPI crée automatiquement la sous-arborescence IPM et les dossiers racine pour les résultats de recherche, les vues communes et des affichages personnels lors de la banque de messages est ouvert. Pour plus d’informations sur ces dossiers, voir [La sous-arborescence IPM](ipm-subtree.md) et [Dossiers spéciaux MAPI](mapi-special-folders.md). 
    
Pour récupérer l’identificateur d’entrée de la banque de messages par défaut, vous devez appeler [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) pour ouvrir la table et appliquer une restriction appropriée dans un appel à [HrQueryAllRows](hrqueryallrows.md). **HrQueryAllRows** renvoie un ensemble de la ligne qui représente la banque de messages par défaut de lignes. La restriction que vous passez à **HrQueryAllRows** peut prendre une des formes suivantes : 
  
1. Une restriction **et** qui utilise une structure **SAndRestriction** pour combiner : 
    
   - Une restriction qui utilise une structure **SExistRestriction** pour tester l’existence de la propriété **PR_DEFAULT_STORE** d’existe. 
    
   - Une restriction de propriété qui utilise une structure [SPropertyRestriction](spropertyrestriction.md) pour vérifier la valeur TRUE dans la propriété **PR_DEFAULT_STORE** . 
    
2. Une restriction de masque de bits qui utilise une structure [SBitMaskRestriction](sbitmaskrestriction.md) pour l’application STATUS_DEFAULT_STORE sous forme de masque par rapport à la propriété **PR_RESOURCE_FLAGS** . 
    
## <a name="see-also"></a>Voir aussi

- [SExistRestriction](sexistrestriction.md)
- [SAndRestriction](sandrestriction.md)

