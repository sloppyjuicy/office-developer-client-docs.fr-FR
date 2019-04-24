---
title: Identificateurs de carnet d'adresses
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 40f6c699-86aa-4324-a30d-12c8f1e2de9c
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 822d83c4b77d06c2e000b391c7e229985470ccd3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331093"
---
# <a name="address-book-identifiers"></a>Identificateurs de carnet d'adresses

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Tous les fournisseurs de carnets d'adresses attribuent des identificateurs d'entrée à l'aide de la propriété **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) pour leur utilisateur de messagerie et les objets de liste de distribution. Les applications clientes utilisent ces identificateurs d'entrée pour ouvrir et accéder aux objets auxquels elles sont affectées.
  
Le carnet d'adresses utilise trois autres types d'identificateurs pour représenter les objets:
  
- Identificateurs d’entrée ponctuelle
    
- Identificateurs d'entrée de modèle uniques
    
- Identificateurs de modèle
    
En raison de la diversité des identificateurs d'entrée et de la similarité avec lesquels elles sont nommées, il est facile de se rendre compte de la façon dont chaque type est utilisé et créé. 
  
Un identificateur d'entrée unique est un identificateur d'entrée qui permet d'ouvrir et d'accéder au type de destinataire connu sous le nom de destinataire unique ou personnalisé. Les destinataires unique sont des destinataires qui n'appartiennent à aucun des fournisseurs de carnet d'adresses dans le profil. Les identificateurs d'entrée attribués à des destinataires uniques utilisent un format spécialement réservé pour les destinataires uniques. Les identificateurs d'entrée uniques étant utilisés pour ouvrir et accéder aux objets, ils sont stockés dans la propriété PR_ENTRYID.
  
Des identificateurs d'entrée uniques et uniques sont créés:
  
- Lorsque les utilisateurs d'une application cliente choisissent d'ajouter un destinataire qui ne représente aucune entrée dans le carnet d'adresses à la liste des destinataires d'un message.
    
- Lorsque les utilisateurs d'une application cliente choisissent d'ajouter un destinataire qui ne représente aucune entrée dans le carnet d'adresses à un conteneur de carnet d'adresses modifiable.
    
- Lorsqu'un fournisseur de transport reçoit un message avec une adresse qui ne peut pas être gérée par son fournisseur de carnet d'adresses associé.
    
- Lorsqu'un fournisseur de transport reçoit un message avec une adresse qui appartient à une passerelle.
    
Dans les deux premières situations, le client appelle **IAddrBook:: CreateOneOff** pour associer un identificateur d'entrée unique au destinataire isolé nouvellement créé. Dans les deux cas, le fournisseur de transport appelle **IMAPISupport:: CreateOneOff** pour associer un identificateur d'entrée unique à l'adresse étrangère. Pour plus d'informations, voir [IAddrBook:: CreateOneOff](iaddrbook-createoneoff.md) et [IMAPISupport:: CreateOneOff](imapisupport-createoneoff.md).
  
Un identificateur d'entrée de modèle unique est un identificateur d'entrée à court terme qui est utilisé pour ouvrir un modèle et y accéder pour créer des cas uniques. Les fournisseurs de carnet d'adresses et les modèles de fourniture MAPI pour la saisie des informations requises pour créer un destinataire d'un type particulier. Des informations sur ces modèles, y compris leurs identificateurs d'entrée, sont publiées dans la table ponctuelle. Les tables ponctuelles s'affichent lorsque MAPI appelle la méthode **IABLogon:: GetOneOffTable** ou la méthode **IMAPIProp:: OpenProperty** du carnet d'adresses pour demander le **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)). ou lorsqu'un fournisseur appelle **IMAPISupport:: GetOneOffTable**. Pour plus d'informations, voir [IABLogon:: GetOneOffTable](iablogon-getoneofftable.md), [IMAPIProp:: OpenProperty](imapiprop-openproperty.md)et [IMAPISupport:: GetOneOffTable](imapisupport-getoneofftable.md).
  
Pour créer un nouveau, un utilisateur sélectionne l'un des modèles figurant dans le tableau à l'arrêt. Le client transmet la colonne PR_ENTRYID à partir de la ligne sélectionnée, qui est l'identificateur d'entrée de modèle unique du modèle sélectionné, à **IAddrBook:: NewEntry** dans le paramètre _lpEIDNewEntryTpl_ . Pour plus d'informations, voir [IAddrBook:: NewEntry](iaddrbook-newentry.md). MAPI utilise l'identificateur d'entrée de modèle unique pour afficher le modèle et permettre à l'utilisateur d'entrer les informations nécessaires à la création du destinataire. 
  
Un identificateur de modèle est un identificateur d'entrée que certains fournisseurs de carnet d'adresses affectent à leurs destinataires en plus de l'identificateur d'entrée qui est conservé dans la propriété PR_ENTRYID. Les fournisseurs définissent la propriété **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) d'un destinataire pour stocker son identificateur de modèle. Certains fournisseurs de carnets d'adresses affectent la même valeur pour l'identificateur de modèle et les propriétés de l'identificateur d'entrée d'un destinataire.
  
Les identificateurs de modèle sont utilisés uniquement par les fournisseurs de carnet d'adresses et par MAPI pour lier les données des destinataires d'un fournisseur, connu sous le nom de fournisseur d'hôte, au code du destinataire dans un autre fournisseur, connu sous le nom de fournisseur étranger. Le fournisseur d'hôte fournit le stockage pour le destinataire; le fournisseur étranger fournit la logique. Le processus de liaison permet à un fournisseur d'hôtes de mettre à jour les données d'un destinataire qu'il stocke à l'aide du code d'un fournisseur étranger.
  
Lorsque le fournisseur hôte est prêt à modifier son destinataire, il transmet la propriété PR_TEMPLATEID dans un appel à la méthode **IMAPISupport:: OpenTemplateID** pour lancer le processus de liaison. MAPI continue le processus en transférant l'identificateur de modèle au fournisseur étranger approprié par le biais d'un appel à sa méthode **IABLogon:: OpenTemplateID** . Pour plus d'informations, voir [IMAPISupport:: OpenTemplateID](imapisupport-opentemplateid.md) et [IABLogon:: OpenTemplateID](iablogon-opentemplateid.md). Le fournisseur étranger renvoie un pointeur vers son implémentation **IMAPIProp** pour le destinataire, que le fournisseur hôte peut utiliser à la place de sa propre implémentation. 
  

