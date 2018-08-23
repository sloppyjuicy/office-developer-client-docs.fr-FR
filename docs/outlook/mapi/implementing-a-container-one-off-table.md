---
title: Implémentation d’une table ponctuelle de conteneur
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: eabbde74-49a1-4eeb-a01d-67e45ae4b343
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: d468943f84f1d23f1b4b84881e69cee0041a5bae
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576595"
---
# <a name="implementing-a-container-one-off-table"></a>Implémentation d’une table ponctuelle de conteneur

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Pour accéder à la table unique appartenant à l’une de vos conteneurs, MAPI appelle la méthode de [IMAPIProp::OpenProperty](imapiprop-openproperty.md) du conteneur pour ouvrir la propriété **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) avec **IMAPITable** interface. Le conteneur est demandé à retourner sa table unique lors d’une application cliente ajouter un destinataire vers le conteneur. Si le conteneur autorise tous les destinataires, votre fournisseur peut retourner son propre implémentation tableau soit appeler [IMAPISupport::GetOneOffTable](imapisupport-getoneofftable.md) pour retourner l’implémentation MAPI. 
  
L’ensemble des modèles dans la table uniques conteneur doit refléter le type de destinataires conteneur peut contenir. En règle générale, cela inclut un ou deux modèles, les modèles pour la création d’un utilisateur de messagerie spécifique ou une liste de distribution. Les identificateurs d’entrée de ces modèles sont stockés dans le **PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md)) et les propriétés **PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)). Toutefois, les conteneurs ne sont en aucun cas limités à ces types d’entrées. Ils peuvent contenir d’autres types de destinataires ou entrées non-recipient comme des répertoires. 
  

