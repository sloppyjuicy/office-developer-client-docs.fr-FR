---
title: Fonctionnalités facultatives pour les fournisseurs de carnets d’adresses
description: Décrit les fonctionnalités facultatives pour les fournisseurs de carnets d’adresses dans Microsoft Outlook et comment les implémenter.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: f1558259-7f0b-4731-80d2-88e51e203df0
ms.openlocfilehash: a37dbbf8f9fddece16d2dae0040be9219e843ae0
ms.sourcegitcommit: 1b44c8f9eac3aedaf7fe7ec70c808fe8ed7d4b99
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65853257"
---
# <a name="optional-features-for-address-book-providers"></a>Fonctionnalités facultatives pour les fournisseurs de carnets d’adresses

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Il existe de nombreuses fonctionnalités facultatives pour les fournisseurs de carnets d’adresses. Voici quelques-unes des fonctionnalités les plus couramment implémentées :
  
- Agissant en tant que fournisseur étranger en autorisant l’ajout d’entrées d’un de vos conteneurs au conteneur d’un autre fournisseur.
    
- Agissant en tant que fournisseur hôte en ajoutant des entrées d’un autre fournisseur à l’un de vos conteneurs.
    
- Recherche avancée.
    
- Préfixe faisant défiler les tables de contenu.
    
- Prise en charge des listes de distribution.
    
- Prise en charge de la notification d’événement.
    
Le tableau suivant décrit brièvement ces fonctionnalités facultatives et la façon dont vous les implémentez :
  
|**Fonctionnalité**|**Modalités de mise en œuvre**|
|:-----|:-----|
|Fournir des modèles pour la création d’entrées pour les listes de destinataires de messages  <br/> |Implémentez la méthode [IABLogon::GetOneOffTable](iablogon-getoneofftable.md) . Pour plus d’informations, consultez [Tables uniques](one-off-tables.md) et [Implémentation de tables One-Off](implementing-one-off-tables.md). |
|Regrouper les destinataires dans une unité nommée  <br/> |Prenez en charge les propriétés des listes de distribution en implémentant l’interface [IDistList : IMAPIContainer](idistlistimapicontainer.md) . |
|Agir en tant que fournisseur de carnet d’adresses étranger en autorisant l’ajout d’entrées à un conteneur dans un autre fournisseur  <br/> | Prenez en charge le code de liaison aux données du fournisseur hôte en :  <br/>  Prise en charge de la propriété **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) sur les utilisateurs de messagerie et les listes de distribution. Pour plus d’informations, consultez [Identificateurs de carnet d’adresses](address-book-identifiers.md).  Implémentation de la méthode [IABLogon::OpenTemplateID](iablogon-opentemplateid.md) . Pour plus d’informations, consultez [Agir en tant que fournisseur de carnets d’adresses étrangers](acting-as-a-foreign-address-book-provider.md). |
|Agir en tant que fournisseur de carnet d’adresses hôte en insérant des entrées à partir d’un autre fournisseur  <br/> |Prenez en charge la liaison de données au code d’un fournisseur étranger en appelant la méthode [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) . Pour plus d’informations, consultez [Agir en tant que fournisseur de carnet d’adresses d’hôte](acting-as-a-host-address-book-provider.md). |
|Défilement de préfixe  <br/> |Prise en charge des restrictions sur les tables de contenu de conteneur. Pour plus d’informations, consultez [À propos des restrictions](about-restrictions.md). |
|Recherche avancée dans un conteneur  <br/> |Prise en charge de la propriété **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)) sur les conteneurs. Pour plus d’informations, consultez [Implémentation de la recherche avancée](implementing-advanced-searching.md). |
|Notification d’événement  <br/> |Implémentez les méthodes [IABLogon::Advise](iablogon-advise.md) et [IABLogon::Unadvise](iablogon-unadvise.md) . Pour plus d’informations, consultez [Notification d’événement dans MAPI](event-notification-in-mapi.md) et [Notification d’événement de prise en charge](supporting-event-notification.md). |
   
Pour la notification d’événement, votre méthode **IABLogon::Advise** est appelée par MAPI lorsqu’un client appelle **IAddrBook::Conseille de** s’inscrire aux notifications sur l’un de vos conteneurs, utilisateurs de messagerie ou listes de distribution. Toutefois, étant donné que la prise en charge de la notification d’événement est facultative, vous pouvez retourner MAPI_E_NO_SUPPORT à partir de ces méthodes. Toutefois, MAPI vous recommande de prendre au moins en charge les notifications sur vos tables de contenu et vous encourage à prendre en charge tous les types de notification d’objet, à l’exception de  _fnevSearchComplete_ et de  _l’événement fnevCriticalError_ pour ajouter de la valeur. 
  

