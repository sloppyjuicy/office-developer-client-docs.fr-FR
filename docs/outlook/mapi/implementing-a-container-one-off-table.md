---
title: Implémentation d'une table ponctuelle de conteneur
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: eabbde74-49a1-4eeb-a01d-67e45ae4b343
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 72dc73b6ed8519be2d8010544fdd5dc5b7b0f759
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332885"
---
# <a name="implementing-a-container-one-off-table"></a>Implémentation d'une table ponctuelle de conteneur

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Pour accéder à la table ponctuelle appartenant à l'un de vos conteneurs, MAPI appelle la méthode [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) du conteneur pour ouvrir la **propriété PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) avec la méthode **IMAPITable** . Lip. Votre conteneur est invité à retourner sa table One-Off lorsqu'une application cliente tente d'ajouter un destinataire au conteneur. Si le conteneur autorise des destinataires, votre fournisseur peut renvoyer sa propre implémentation de table ou appeler [IMAPISupport:: GetOneOffTable](imapisupport-getoneofftable.md) pour retourner l'implémentation MAPI. 
  
L'ensemble des modèles de la table ponctuelle conteneur doit refléter le type de destinataire que le conteneur particulier peut conserver. En règle générale, cela inclut un ou deux modèles, des modèles pour la création d'un utilisateur de messagerie individuel ou d'une liste de distribution. Les identificateurs d'entrée de ces modèles sont conservés dans les propriétés **PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md)) et **PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)). Toutefois, les conteneurs ne sont pas limités à ces types d'entrées. Ils peuvent contenir d'autres types de destinataires ou d'entrées autres que des destinataires, tels que des annuaires. 
  

