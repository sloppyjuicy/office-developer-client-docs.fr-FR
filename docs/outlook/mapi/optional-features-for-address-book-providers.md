---
title: Fonctionnalités facultatives pour les fournisseurs de carnets d’adresses
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f1558259-7f0b-4731-80d2-88e51e203df0
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 378dcc3e1506432de22731a27731c58067647952
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565892"
---
# <a name="optional-features-for-address-book-providers"></a>Fonctionnalités facultatives pour les fournisseurs de carnets d’adresses

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Il existe de nombreuses fonctionnalités facultatives pour les fournisseurs de carnet d’adresses. Certaines des fonctionnalités plus souvent mises en œuvre sont les suivantes :
  
- En autorisant les entrées à partir d’un de vos conteneurs à ajouter au conteneur d’un autre fournisseur, agissant comme un fournisseur étranger.
    
- Agissant comme un fournisseur d’hébergement en ajoutant des entrées à partir d’un autre fournisseur à un de vos conteneurs.
    
- Recherche avancée.
    
- Préfixe de défilement des tables des matières.
    
- Prise en charge des listes de distribution.
    
- Prise en charge de la notification d’événement.
    
Le tableau suivant décrit brièvement ces fonctionnalités facultatives et comment les implémenter :
  
|**Fonctionnalité**|**Comment mettre en œuvre**|
|:-----|:-----|
|Fournir des modèles pour créer des listes de destinataires entrées des messages  <br/> |Implémentez la méthode [IABLogon::GetOneOffTable](iablogon-getoneofftable.md) . Pour plus d’informations, voir [Uniques Tables](one-off-tables.md) et [l’implémentation uniques](implementing-one-off-tables.md).  <br/> |
|Destinataires de groupe dans une unité nommée  <br/> |Prendre en charge les propriétés des listes de distribution en implémentant la [IDistList : IMAPIContainer](idistlistimapicontainer.md) interface.  <br/> |
|Agir comme un fournisseur de carnet d’adresse étrangère en autorisant les entrées à ajouter à un conteneur dans un autre fournisseur  <br/> | Prise en charge du code de liaison à des données dans le fournisseur d’hébergement par :  <br/>  Prise en charge de la propriété **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) sur les listes de distribution et les utilisateurs de messagerie. Pour plus d’informations, voir [Identificateurs de carnet d’adresses](address-book-identifiers.md).  <br/>  L’implémentation de la méthode [IABLogon::OpenTemplateID](iablogon-opentemplateid.md) . Pour plus d’informations, voir [agissant comme un fournisseur de carnet d’adresses étrangère](acting-as-a-foreign-address-book-provider.md).  <br/> |
|Agissant comme un fournisseur de carnet d’adresses hôte en insérant des entrées à partir d’un autre fournisseur  <br/> |Prend en charge en liant des données au code d’un fournisseur externe en appelant la méthode [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) . Pour plus d’informations, voir [agit comme fournisseur de carnet d’adresses hôte](acting-as-a-host-address-book-provider.md).  <br/> |
|Préfixe de défilement  <br/> |Prise en charge des restrictions sur les tables des matières conteneur. Pour plus d’informations, voir [à propos des Restrictions](about-restrictions.md).  <br/> |
|Recherche avancée dans un conteneur  <br/> |Prise en charge de la propriété **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)) sur les conteneurs. Pour plus d’informations, voir [Implémentation de la recherche avancée](implementing-advanced-searching.md).  <br/> |
|Notification d’événement  <br/> |Implémenter les méthodes [IABLogon::Advise](iablogon-advise.md) et [IABLogon::Unadvise](iablogon-unadvise.md) . Pour plus d’informations, voir [Notification d’événement MAPI](event-notification-in-mapi.md) et [Prise en charge de Notification d’événement](supporting-event-notification.md).  <br/> |
   
Notification d’événement, votre méthode **IABLogon::Advise** est appelée par MAPI, lorsqu’un client appelle **IAddrBook::Advise** pour enregistrer les notifications sur l’un de vos conteneurs, de messagerie des utilisateurs ou des listes de distribution. Toutefois, étant donné que la prise en charge de la notification d’événement est facultatif, vous pouvez retourner MAPI_E_NO_SUPPORT à partir de ces méthodes. Toutefois, MAPI ne recommande que vous avez au moins prendre en charge des notifications sur les tables des matières et vous encourage à prendre en charge tous les types de notification de l’objet à l’exception de _fnevSearchComplete_ et l’événement _fnevCriticalError_ pour ajouter la valeur. 
  

