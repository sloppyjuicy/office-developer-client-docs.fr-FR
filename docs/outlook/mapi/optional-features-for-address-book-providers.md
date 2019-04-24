---
title: Fonctionnalités facultatives pour les fournisseurs de carnets d'adresses
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f1558259-7f0b-4731-80d2-88e51e203df0
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 9f5d8f0cd1b21f58e4e5c7d7ccd6cb19f3626c38
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348565"
---
# <a name="optional-features-for-address-book-providers"></a>Fonctionnalités facultatives pour les fournisseurs de carnets d'adresses

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Il existe de nombreuses fonctionnalités facultatives pour les fournisseurs de carnet d'adresses. Parmi les fonctionnalités les plus couramment implémentées, citons:
  
- Agir en tant que fournisseur étranger en autorisant l'ajout d'entrées de l'un de vos conteneurs au conteneur d'un autre fournisseur.
    
- Agir en tant que fournisseur d'hôte en ajoutant des entrées d'un autre fournisseur à l'un de vos conteneurs.
    
- Recherche avancée.
    
- PréFixe le défilement dans les tables de contenu.
    
- Prise en charge des listes de distribution.
    
- Prise en charge de la notification d'événement.
    
Le tableau suivant décrit brièvement ces fonctionnalités facultatives et leur implémentation:
  
|**Fonctionnalité**|**Comment implémenter**|
|:-----|:-----|
|Fournir des modèles pour la création d'entrées pour les listes de destinataires de message  <br/> |Implémentez la méthode [IABLogon:: GetOneOffTable](iablogon-getoneofftable.md) . Pour plus d'informations, consultez la rubrique [tables One-Off](one-off-tables.md) et [implémentation de tables ponctuelles](implementing-one-off-tables.md).  <br/> |
|ReGrouper les destinataires dans une unité nommée  <br/> |Prendre en charge les propriétés des listes de distribution en implémentant l'interface [IDistList: IMAPIContainer](idistlistimapicontainer.md) .  <br/> |
|Agir en tant que fournisseur de carnets d'adresses étrangers en autorisant l'ajout d'entrées à un conteneur dans un autre fournisseur  <br/> | Prendre en charge la liaison de code aux données du fournisseur hôte en:  <br/>  Prise en charge de la propriété **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) sur les utilisateurs de messagerie et les listes de distribution. Pour plus d'informations, consultez la rubrique identificateurs de [carnet d'adresses](address-book-identifiers.md).  <br/>  Implémentation de la méthode [IABLogon:: OpenTemplateID](iablogon-opentemplateid.md) . Pour plus d'informations, consultez [la rubrique agir en tant que fournisseur de carnet d'adresses étranger](acting-as-a-foreign-address-book-provider.md).  <br/> |
|Agir en tant que fournisseur de carnets d'adresses hôte en insérant des entrées à partir d'un autre fournisseur  <br/> |Prendre en charge la liaison de données à du code à partir d'un fournisseur étranger en appelant la méthode [IMAPISupport:: OpenTemplateID](imapisupport-opentemplateid.md) . Pour plus d'informations, consultez [la rubrique agir en tant que fournisseur de carnet d'adresses hôte](acting-as-a-host-address-book-provider.md).  <br/> |
|Défilement du préFixe  <br/> |Prise en charge des restrictions sur les tables des matières du conteneur. Pour plus d'informations, consultez la rubrique [à propos des restrictions](about-restrictions.md).  <br/> |
|Recherche avancée dans un conteneur  <br/> |Prendre en charge la propriété **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)) sur les conteneurs. Pour plus d'informations, consultez la rubrique implémentation de la [recherche avancée](implementing-advanced-searching.md).  <br/> |
|Notification d'événement  <br/> |Implémentez les méthodes [IABLogon:: Advise](iablogon-advise.md) et [IABLogon::](iablogon-unadvise.md) Unadvise. Pour plus d'informations, consultez la rubrique [notifications d'événements dans MAPI](event-notification-in-mapi.md) et [notification d'événement de prise en charge](supporting-event-notification.md).  <br/> |
   
Pour la notification d'événement, votre méthode **IABLogon:: Advise** est appelée par MAPI lorsqu'un client appelle **IAddrBook:: Advise** pour s'inscrire aux notifications sur l'un de vos conteneurs, utilisateurs de messagerie ou listes de distribution. Toutefois, étant donné que la notification d'événement de prise en charge est facultative, vous pouvez renvoyer MAPI_E_NO_SUPPORT à partir de ces méthodes. Toutefois, MAPI recommande de prendre en charge au moins les notifications sur vos tables de contenu et vous encourage à prendre en charge tous les types de notifications d'objets, à l'exception de _fnevSearchComplete_ et de l'événement _fnevCriticalError_ pour ajouter de la valeur. 
  

