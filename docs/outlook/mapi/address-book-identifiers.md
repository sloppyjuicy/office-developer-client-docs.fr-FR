---
title: Identificateurs de carnet d’adresses
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 40f6c699-86aa-4324-a30d-12c8f1e2de9c
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 0814d76dac97e40940f41c49dbf72efdd26b3cca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782887"
---
# <a name="address-book-identifiers"></a>Identificateurs de carnet d’adresses

  
  
**S’applique à**: Outlook 
  
Tous les fournisseurs de carnet d’adresses attribuer des identificateurs d’entrée à l’aide de la propriété **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) à leur messagerie utilisateur et les objets de liste de distribution. Applications clientes utilisent ces identificateurs d’entrée d’ouvrir et d’accéder aux objets auxquels ils sont affectés.
  
Le carnet d’adresses utilise trois autres types d’identificateurs pour représenter des objets :
  
- Identificateurs d’entrée unique
    
- Identificateurs d’entrée modèle uniques
    
- Identificateurs de modèle
    
Étant donné la multitude d’identificateurs d’entrée et la similarité avec lequel ils sont nommés, il est facile de devenir des doutes quant à la façon dont chaque type est utilisé et créé. 
  
Un identificateur d’entrée unique est un identificateur d’entrée qui sert à ouvrir et accéder au type de destinataire appelé One-Off ou un destinataire personnalisé. Uniques sont des destinataires qui n’appartiennent pas à un des fournisseurs de carnet d’adresses dans le profil. Les identificateurs d’entrée assignés à uniques utilisent un format spécialement réservés pour les destinataires uniques. Étant donné que les identificateurs d’entrée uniques sont utilisés pour ouvrir et accéder aux objets, ils sont stockés dans la propriété PR_ENTRYID.
  
Uniques et les identificateurs d’entrée uniques sont créés :
  
- Lorsque les utilisateurs d’une application cliente choisir Ajouter un destinataire qui ne représente pas une entrée dans le carnet d’adresses à la liste des destinataires d’un message.
    
- Lorsque les utilisateurs d’une application cliente choisir Ajouter un destinataire qui ne représente pas une entrée dans le carnet d’adresses pour un conteneur de carnet d’adresses modifiable.
    
- Lorsqu’un fournisseur de transport reçoit un message à une adresse qui ne peuvent pas être géré par son fournisseur de carnet d’adresses associées.
    
- Lorsqu’un fournisseur de transport reçoit un message à une adresse qui appartient à une passerelle.
    
Dans les deux premiers cas, le client appelle **IAddrBook::CreateOneOff** pour associer un identificateur d’entrée unique le destinataire unique nouvellement créé. Dans les deux cas, le fournisseur de transport appelle **IMAPISupport::CreateOneOff** pour associer un identificateur d’entrée unique à l’adresse étrangère. Pour plus d’informations, voir [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) et [IMAPISupport::CreateOneOff](imapisupport-createoneoff.md).
  
Un identificateur d’entrée unique modèle est un identificateur d’entrée à court terme qui sert à ouvrir et accéder à un modèle pour la création uniques. Fournisseurs de carnet d’adresses et MAPI fournissent des modèles pour saisir les informations nécessaires à la création d’un destinataire d’un type particulier. Plus d’informations sur ces modèles, y compris les identificateurs d’entrée, sont publiés dans le tableau unique. Tables uniques sont affichées lorsque MAPI appelle la méthode **IABLogon::GetOneOffTable** ou méthode de **IMAPIProp::OpenProperty** d’un conteneur carnet d’adresses pour demander le **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) propriété ou lorsqu’un fournisseur appelle **IMAPISupport::GetOneOffTable**. Pour plus d’informations, voir [IABLogon::GetOneOffTable](iablogon-getoneofftable.md), [IMAPIProp::OpenProperty](imapiprop-openproperty.md)et [IMAPISupport::GetOneOffTable](imapisupport-getoneofftable.md).
  
Pour créer un nouveau unique, un utilisateur sélectionne un des modèles répertoriés dans le tableau unique. Le client transmet la colonne PR_ENTRYID à partir de la ligne sélectionnée, qui est l’identificateur d’entrée unique modèle du modèle sélectionné, à **IAddrBook::NewEntry** dans le paramètre _lpEIDNewEntryTpl_ . Pour plus d’informations, voir [IAddrBook::NewEntry](iaddrbook-newentry.md). MAPI utilise l’identificateur d’entrée unique de modèle pour le modèle d’affichage et pour autoriser l’utilisateur à entrer les informations nécessaires pour créer le destinataire. 
  
Un identificateur de modèle est un identificateur d’entrée que certains fournisseurs de carnet d’adresses affecter à leurs destinataires en plus de l’identificateur d’entrée n’est conservé dans la propriété PR_ENTRYID. Fournisseurs **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) propriété d’un destinataire définie pour stocker son identificateur de modèle. Certains fournisseurs de carnet d’adresses affecter la même valeur pour l’identificateur du modèle d’un destinataire et les propriétés d’identificateur d’entrée.
  
Identificateurs de modèle sont utilisés uniquement par les fournisseurs de carnet d’adresses et MAPI pour lier des données des destinataires dans un fournisseur, désignés comme fournisseur d’hébergement, au code pour le destinataire dans un autre fournisseur, désignés comme le fournisseur étranger. Le fournisseur d’hébergement fournit le stockage pour le destinataire ; le fournisseur étranger fournit la logique. Le processus de liaison permet à un fournisseur de l’hôte à mettre à jour les données d’un destinataire qu’il stocke l’aide du code d’un fournisseur externe.
  
Lorsque le fournisseur d’hébergement est prêt à modifier son destinataire, il passe un appel à la méthode **IMAPISupport::OpenTemplateID** pour lancer le processus de liaison de la propriété PR_TEMPLATEID. MAPI continue le processus en transférant l’identificateur de modèle au fournisseur étranger approprié via un appel à la méthode **IABLogon::OpenTemplateID** . Pour plus d’informations, voir [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) et [IABLogon::OpenTemplateID](iablogon-opentemplateid.md). Le fournisseur étranger retourne un pointeur vers son implémentation **IMAPIProp** pour le destinataire, le fournisseur d’hébergement peut utiliser à la place de sa propre implémentation. 
  

