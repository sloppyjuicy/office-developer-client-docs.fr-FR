---
title: L’implémentation d’une Table unique du conteneur
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: eabbde74-49a1-4eeb-a01d-67e45ae4b343
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 83351e18750ccbffbe60c4e19f9b04a9c94a42e2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784155"
---
# <a name="implementing-a-container-one-off-table"></a>L’implémentation d’une Table unique du conteneur

  
  
**S’applique à**: Outlook 
  
Pour accéder à la table unique appartenant à l’une de vos conteneurs, MAPI appelle la méthode de [IMAPIProp::OpenProperty](imapiprop-openproperty.md) du conteneur pour ouvrir la propriété **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) avec **IMAPITable** interface. Le conteneur est demandé à retourner sa table unique lors d’une application cliente ajouter un destinataire vers le conteneur. Si le conteneur autorise tous les destinataires, votre fournisseur peut retourner son propre implémentation tableau soit appeler [IMAPISupport::GetOneOffTable](imapisupport-getoneofftable.md) pour retourner l’implémentation MAPI. 
  
L’ensemble des modèles dans la table uniques conteneur doit refléter le type de destinataires conteneur peut contenir. En règle générale, cela inclut un ou deux modèles, les modèles pour la création d’un utilisateur de messagerie spécifique ou une liste de distribution. Les identificateurs d’entrée de ces modèles sont stockés dans le **PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md)) et les propriétés **PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)). Toutefois, les conteneurs ne sont en aucun cas limités à ces types d’entrées. Ils peuvent contenir d’autres types de destinataires ou entrées non-recipient comme des répertoires. 
  

