---
title: Événements de Notification MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ef082d7b-9b2d-4267-beb5-d3ed1d9c7bbf
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 8acf197f305373c082ef411732d631535201d488
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567250"
---
# <a name="mapi-notification-events"></a>Événements de Notification MAPI

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Lorsque les applications clientes s’inscrire pour la notification d’événement, ils doivent spécifier un ou plusieurs événements. Les événements qui ils peuvent spécifier dépendent de l’ensemble d’événements qui prend en charge de la source advise concerné. Il existe dix types de notifications clients et fournisseurs de services peuvent s’inscrire pour chacune représentée par une constante. Notification d’état d’objet est une exception. Notification d’état d’objet est une notification MAPI interne ; Impossible d’enregistrer les clients pour qu’il et il ne peut pas générer des fournisseurs de services. Le tableau suivant décrit les types d’événements et les objets source advise pouvant prendre en charge les. La constante de l’événement est incluse dans le type d’événement.
  
|**Type d’événement**|**Description**|**Objets de la source de notification**|
|:-----|:-----|:-----|
|Erreur critique ( _fnevCriticalError_)  <br/> |Une erreur globale ou un événement s’est produite, par exemple un arrêt de la session en cours.  <br/> |Tous les types de banque de messages et objets de carnet d’adresses, table, l’état de session  <br/> |
|Objet modifié ( _fnevObjectModified_)  <br/> |Un objet MAPI a changé.  <br/> |Dossiers, des messages, tous les types d’objets de carnet d’adresses  <br/> |
|Objet créé ( _fnevObjectCreated_)  <br/> |Un objet MAPI a été créé.  <br/> |Dossiers, des messages, tous les types d’objets de carnet d’adresses  <br/> |
|L’objet déplacé ( _fnevObjectMoved_)  <br/> |Un objet MAPI a été déplacé.  <br/> |Dossiers, des messages, tous les types d’objets de carnet d’adresses  <br/> |
|Objet supprimé ( _fnevObjectDeleted_)  <br/> |Un objet MAPI a été supprimé.  <br/> |Dossiers, des messages, tous les types d’objets de carnet d’adresses  <br/> |
|Objet copié ( _fnevObjectCopied_)  <br/> |Un objet MAPI a été copié.  <br/> |Dossiers, des messages, tous les types d’objets de carnet d’adresses  <br/> |
|Événements étendus ( _fnevExtended_)  <br/> |Un événement interne définie par un fournisseur de services particulier s’est produite.  <br/> |N’importe quel objet source de notification  <br/> |
|Recherche terminée ( _fnevSearchComplete_)  <br/> |Une opération de recherche est terminée et les résultats de la recherche sont disponibles.  <br/> |Dossiers  <br/> |
|Table modifiée ( _fnevTableModified_)  <br/> |Informations d’un objet de table MAPI a changé.  <br/> |Tableaux  <br/> |
|Nouveaux messages ( _fnevNewMail_)  <br/> |Un message a été remis et est en attente de traitement.  <br/> |Banque de messages, les dossiers  <br/> |
   
L’événement étendue est définie par un fournisseur de services pour représenter un événement qui ne peuvent pas être couvertes par les autres événements prédéfinis. Seuls les clients qui savoir avant qu’ils inscrivent qu’un fournisseur de services prend en charge un événement étendu peuvent s’inscrire pour cet événement. Il n’est pas possible pour les clients déterminer insu avance si un fournisseur de services prend en charge un événement étendu et, si c’est le cas, comment gérer un événement lorsqu’il est reçu.
  

