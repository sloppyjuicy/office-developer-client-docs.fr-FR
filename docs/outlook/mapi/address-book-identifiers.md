---
title: Identificateurs de carnet d’adresses
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 40f6c699-86aa-4324-a30d-12c8f1e2de9c
ms.openlocfilehash: 1c0461c2de8fa0f149f7a51b99da5602a2c61d3b
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63370966"
---
# <a name="address-book-identifiers"></a>Identificateurs de carnet d’adresses

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Tous les fournisseurs de carnet d’adresses attribuent des identificateurs d’entrée à l’aide de la **propriété PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) à leurs objets utilisateur de messagerie et liste de distribution. Les applications clientes utilisent ces identificateurs d’entrée pour ouvrir et accéder aux objets auquel elles sont affectées.
  
Le carnet d’adresses utilise trois autres types d’identificateurs pour représenter des objets :
  
- Identificateurs d’entrée ponctuelle
    
- Identificateurs d’entrée de modèle uniques
    
- Identificateurs de modèles
    
En raison de la variété des identificateurs d’entrée et de la similarité avec laquelle ils sont nommés, il est facile de confondre la façon dont chaque type est utilisé et créé. 
  
Un identificateur d’entrée unique est un identificateur d’entrée utilisé pour ouvrir et accéder au type de destinataire appelé destinataire unique ou personnalisé. Les destinataires sont des destinataires qui n’appartiennent à aucun des fournisseurs de carnet d’adresses dans le profil. Les identificateurs d’entrée affectés à des identificateurs uniques utilisent un format spécifiquement réservé aux destinataires uniques. Étant donné que les identificateurs d’entrée uniques sont utilisés pour ouvrir et accéder aux objets, ils sont stockés dans PR_ENTRYID propriété.
  
Des identificateurs d’entrée uniques et uniques sont créés :
  
- Lorsque les utilisateurs d’une application cliente choisit d’ajouter un destinataire qui ne représente aucune entrée dans le carnet d’adresses à la liste des destinataires d’un message.
    
- Lorsque les utilisateurs d’une application cliente choisit d’ajouter un destinataire qui ne représente aucune entrée dans le carnet d’adresses à un conteneur de carnet d’adresses modifiable.
    
- Lorsqu’un fournisseur de transport reçoit un message avec une adresse qui ne peut pas être gérée par son fournisseur de carnet d’adresses associé.
    
- Lorsqu’un fournisseur de transport reçoit un message avec une adresse qui appartient à une passerelle.
    
Dans les deux premières situations, le client appelle **IAddrBook::CreateOneOff** pour associer un identificateur d’entrée unique au destinataire unique nouvellement créé. Dans les deux secondes situations, le fournisseur de transport appelle **IMAPISupport::CreateOneOff** pour associer un identificateur d’entrée unique à l’adresse étrangère. Pour plus d’informations, voir [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) and [IMAPISupport::CreateOneOff](imapisupport-createoneoff.md).
  
Un identificateur d’entrée de modèle unique est un identificateur d’entrée à court terme utilisé pour ouvrir et accéder à un modèle pour la création de modèles uniques. Les fournisseurs de carnets d’adresses et les modèles de fourniture MAPI pour entrer les informations requises pour créer un destinataire d’un type particulier. Les informations sur ces modèles, y compris leurs identificateurs d’entrée, sont publiées dans le tableau unique. Les tables one-off sont affichées lorsque MAPI appelle la méthode **IABLogon::GetOneOffTable** ou la méthode **IMAPIProp::OpenProperty** d’un conteneur de carnet d’adresses pour demander la propriété **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) ou lorsqu’un fournisseur appelle **IMAPISupport::GetOneOffTable**. Pour plus d’informations, voir [IABLogon::GetOneOffTable](iablogon-getoneofftable.md), [IMAPIProp::OpenProperty](imapiprop-openproperty.md) et [IMAPISupport::GetOneOffTable](imapisupport-getoneofftable.md).
  
Pour créer un modèle unique, un utilisateur sélectionne l’un des modèles répertoriés dans le tableau unique. Le client transmet la colonne PR_ENTRYID de la ligne sélectionnée, qui est l’identificateur d’entrée de modèle unique du modèle sélectionné, à **IAddrBook::NewEntry** dans le paramètre _lpEIDNewEntryTpl_ . Pour plus d’informations, [voir IAddrBook::NewEntry](iaddrbook-newentry.md). MAPI utilise l’identificateur d’entrée de modèle unique pour afficher le modèle et permettre à l’utilisateur d’entrer les informations nécessaires pour créer le destinataire. 
  
Un identificateur de modèle est un identificateur d’entrée que certains fournisseurs de carnet d’adresses affectent à leurs destinataires en plus de l’identificateur d’entrée conservé dans la propriété PR_ENTRYID. Les fournisseurs définissent la propriété **PR_TEMPLATEID (**[PidTagTemplateid](pidtagtemplateid-canonical-property.md)) d’un destinataire pour stocker son identificateur de modèle. Certains fournisseurs de carnet d’adresses affectent la même valeur pour les propriétés d’identificateur de modèle et d’identificateur d’entrée d’un destinataire.
  
Les identificateurs de modèle sont utilisés uniquement par les fournisseurs de carnets d’adresses et par MAPI pour lier les données des destinataires d’un fournisseur, appelé fournisseur hôte, au code du destinataire dans un autre fournisseur, appelé fournisseur étranger. Le fournisseur d’hôte fournit le stockage pour le destinataire ; le fournisseur étranger fournit la logique. Le processus de liaison permet à un fournisseur hôte de mettre à jour les données d’un destinataire qu’il stocke à l’aide du code d’un fournisseur étranger.
  
Lorsque le fournisseur d’hôte est prêt à modifier son destinataire, il transmet la propriété PR_TEMPLATEID dans un appel à la méthode **IMAPISupport::OpenTemplateID** pour lancer le processus de liaison. MAPI poursuit le processus en transférant l’identificateur de modèle au fournisseur étranger approprié via un appel à sa méthode **IABLogon::OpenTemplateID** . Pour plus d’informations, voir [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) and [IABLogon::OpenTemplateID](iablogon-opentemplateid.md). Le fournisseur étranger renvoie un pointeur vers son implémentation **IMAPIProp** pour le destinataire, que le fournisseur d’hôte peut utiliser à la place de sa propre implémentation. 
  

