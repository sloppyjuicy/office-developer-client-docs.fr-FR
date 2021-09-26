---
title: Mise en œuvre d’une table One-Off conteneur
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: eabbde74-49a1-4eeb-a01d-67e45ae4b343
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 62951a7c4330fb8e909e0b6b978c210a5f5c1938
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59610495"
---
# <a name="implementing-a-container-one-off-table"></a>Mise en œuvre d’une table One-Off conteneur

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Pour accéder à la table unique appartenant à l’un de vos conteneurs, MAPI appelle la méthode [IMAPIProp::OpenProperty](imapiprop-openproperty.md) du conteneur pour ouvrir la propriété **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) avec l’interface **IMAPITable.** Votre conteneur est invité à retourner sa table one-off lorsqu’une application cliente tente d’ajouter un destinataire au conteneur. Si le conteneur autorise des destinataires, votre fournisseur peut retourner sa propre implémentation de table ou appeler [IMAPISupport::GetOneOffTable](imapisupport-getoneofftable.md) pour renvoyer l’implémentation MAPI. 
  
L’ensemble de modèles dans la table unique de conteneur doit refléter le type de destinataires que le conteneur particulier peut contenir. En règle générale, cela inclut un ou deux modèles, des modèles pour la création d’un utilisateur de messagerie individuel ou d’une liste de distribution. Les identificateurs d’entrée pour ces modèles sont détenus dans les propriétés **PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md)) et **PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)). Toutefois, les conteneurs ne sont en aucun cas limités à ces types d’entrées. Elles peuvent contenir d’autres types de destinataires ou d’entrées non destinataires, telles que des répertoires. 
  

