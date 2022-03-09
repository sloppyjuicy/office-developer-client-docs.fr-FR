---
title: Mise en œuvre d’une table de One-Off conteneur
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: eabbde74-49a1-4eeb-a01d-67e45ae4b343
ms.openlocfilehash: a9b277a00f0f45fc0f6987e5a0f6db359a562a2a
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63374354"
---
# <a name="implementing-a-container-one-off-table"></a>Mise en œuvre d’une table de One-Off conteneur

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Pour accéder à la table unique appartenant à l’un de vos conteneurs, MAPI appelle la méthode [IMAPIProp::OpenProperty](imapiprop-openproperty.md) du conteneur pour ouvrir la propriété **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) avec l’interface **IMAPITable** . Votre conteneur est invité à retourner sa table one-off lorsqu’une application cliente tente d’ajouter un destinataire au conteneur. Si le conteneur autorise des destinataires, votre fournisseur peut retourner sa propre implémentation de table ou appeler [IMAPISupport::GetOneOffTable](imapisupport-getoneofftable.md) pour renvoyer l’implémentation MAPI. 
  
L’ensemble des modèles de la table unique de conteneur doit refléter le type de destinataires que le conteneur particulier peut contenir. En règle générale, cela inclut un ou deux modèles, des modèles pour la création d’un utilisateur de messagerie individuel ou d’une liste de distribution. Les identificateurs d’entrée pour ces modèles sont détenus dans les propriétés **PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md)) et **PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)). Toutefois, les conteneurs ne sont en aucun cas limités à ces types d’entrées. Ils peuvent contenir d’autres types de destinataires ou d’entrées non-destinataires, telles que des répertoires. 
  

