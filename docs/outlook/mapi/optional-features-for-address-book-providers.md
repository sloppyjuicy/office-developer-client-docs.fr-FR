---
title: Fonctionnalités facultatives pour les fournisseurs de carnets d’adresses
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: f1558259-7f0b-4731-80d2-88e51e203df0
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 41343755f058b7e210f59bd1cd2781d8996d89cd
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62771936"
---
# <a name="optional-features-for-address-book-providers"></a>Fonctionnalités facultatives pour les fournisseurs de carnets d’adresses

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Il existe de nombreuses fonctionnalités facultatives pour les fournisseurs de carnets d’adresses. Voici quelques-unes des fonctionnalités les plus couramment implémentées :
  
- Agir en tant que fournisseur étranger en permettant l’ajout d’entrées de l’un de vos conteneurs au conteneur d’un autre fournisseur.
    
- Agir en tant que fournisseur d’hôtes en ajoutant des entrées d’un autre fournisseur à l’un de vos conteneurs.
    
- Recherche avancée.
    
- Préfixe faisant défiler les tables des matières.
    
- Prise en charge des listes de distribution.
    
- Prise en charge de la notification d’événement.
    
Le tableau suivant décrit brièvement ces fonctionnalités facultatives et la façon dont vous les implémentez :
  
|**Fonctionnalité**|**Modalités de mise en œuvre**|
|:-----|:-----|
|Modèles de fourniture pour la création d’entrées pour les listes de destinataires des messages  <br/> |[Implémentez la méthode IABLogon::GetOneOffTable](iablogon-getoneofftable.md). Pour plus d’informations, [voir Tableaux one-off](one-off-tables.md) et [Implémentation One-Off Tables](implementing-one-off-tables.md). |
|Grouper les destinataires dans une unité nommée  <br/> |Prise en charge des propriétés des listes de distribution en [implémentant l’interface IDistList : IMAPIContainer](idistlistimapicontainer.md) . |
|Agir en tant que fournisseur de carnet d’adresses étranger en permettant l’ajout d’entrées à un conteneur dans un autre fournisseur  <br/> | Prendre en charge le code de liaison aux données dans le fournisseur hôte en :  <br/>  Prise en **charge PR_TEMPLATEID** propriété ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) sur les utilisateurs de messagerie et les listes de distribution. Pour plus d’informations, [voir Identificateurs de carnet d’adresses](address-book-identifiers.md).  Mise en œuvre [de la méthode IABLogon::OpenTemplateID](iablogon-opentemplateid.md) . Pour plus d’informations, [voir Agir en tant que fournisseur de carnet d’adresses étranger](acting-as-a-foreign-address-book-provider.md). |
|Agir en tant que fournisseur de carnet d’adresses hôte en insérant des entrées d’un autre fournisseur  <br/> |Prendre en charge la liaison de données au code à partir d’un fournisseur étranger en appelant [la méthode IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) . Pour plus d’informations, [voir Acting as a Host Address Book Provider](acting-as-a-host-address-book-provider.md). |
|Défilement de préfixe  <br/> |Prise en charge des restrictions sur les tables de contenu de conteneur. Pour plus d’informations, voir [À propos des restrictions](about-restrictions.md). |
|Recherche avancée dans un conteneur  <br/> |Prise en **charge PR_SEARCH** propriété ([PidTagSearch](pidtagsearch-canonical-property.md)) sur les conteneurs. Pour plus d’informations, voir [Implementing Advanced Searching](implementing-advanced-searching.md). |
|Notification d’événement  <br/> |[Implémentez les méthodes IABLogon::Advise](iablogon-advise.md) et [IABLogon::Unadvise](iablogon-unadvise.md). Pour plus d’informations, [voir Notification d’événement dans MAPI](event-notification-in-mapi.md) et [notification d’événement de prise en charge](supporting-event-notification.md). |
   
Pour la notification d’événement, votre méthode **IABLogon::Advise** sera appelée par MAPI lorsqu’un client appelle **IAddrBook::Advise** pour s’inscrire pour les notifications sur l’un de vos conteneurs, utilisateurs de messagerie ou listes de distribution. Toutefois, étant donné que la prise en charge de la notification d’événement est facultative, vous pouvez MAPI_E_NO_SUPPORT à partir de ces méthodes. Toutefois, MAPI vous recommande de prendre au moins en charge les notifications sur vos tables de contenu et vous encourage à prendre en charge tous les types de notification d’objet à l’exception de  _fnevSearchComplete_ et de l’événement  _fnevCriticalError_ pour ajouter de la valeur. 
  

