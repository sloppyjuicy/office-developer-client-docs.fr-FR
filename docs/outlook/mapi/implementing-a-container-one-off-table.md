---
title: Mise en œuvre d’une table One-Off conteneur
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: eabbde74-49a1-4eeb-a01d-67e45ae4b343
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 72dc73b6ed8519be2d8010544fdd5dc5b7b0f759
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417419"
---
# <a name="implementing-a-container-one-off-table"></a>Mise en œuvre d’une table One-Off conteneur

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Pour accéder à la table unique appartenant à l’un de vos conteneurs, MAPI appelle la méthode [IMAPIProp::OpenProperty](imapiprop-openproperty.md) du conteneur pour ouvrir la propriété **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) avec l’interface **IMAPITable.** Votre conteneur est invité à retourner sa table one-off lorsqu’une application cliente tente d’ajouter un destinataire au conteneur. Si le conteneur autorise des destinataires, votre fournisseur peut retourner sa propre implémentation de table ou appeler [IMAPISupport::GetOneOffTable](imapisupport-getoneofftable.md) pour renvoyer l’implémentation MAPI. 
  
L’ensemble des modèles de la table unique de conteneur doit refléter le type de destinataires que le conteneur particulier peut contenir. En règle générale, cela inclut un ou deux modèles, des modèles pour la création d’un utilisateur de messagerie individuel ou d’une liste de distribution. Les identificateurs d’entrée pour ces modèles sont détenus dans les propriétés **PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md)) et **PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)). Toutefois, les conteneurs ne sont en aucun cas limités à ces types d’entrées. Elles peuvent contenir d’autres types de destinataires ou d’entrées non destinataires, telles que des répertoires. 
  

