---
title: Événements de notification MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ef082d7b-9b2d-4267-beb5-d3ed1d9c7bbf
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 0d05672a0b136520216357cc85a6b7a125415759
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427954"
---
# <a name="mapi-notification-events"></a>Événements de notification MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Lorsque les applications clientes s'inscrivent pour la notification d'événement, elles doivent spécifier un ou plusieurs événements. Les événements qu'ils peuvent spécifier dépendent de l'ensemble d'événements pris en charge par la source de notification prévue. Il existe dix types de notifications que les clients et les fournisseurs de services peuvent inscrire, chacun étant représenté par une constante. La notification d'objet d'État est une exception. La notification d'objet d'État est une notification MAPI interne; les clients ne peuvent pas s'inscrire pour le service informatique et les fournisseurs de services ne peuvent pas le générer. Le tableau suivant décrit les types d'événements et les objets de source de notification qui peuvent les prendre en charge. La constante d'événement est incluse dans le type d'événement.
  
|**Type d’événement**|**Description**|**Informer les objets sources**|
|:-----|:-----|:-----|
|Erreur critique ( _fnevCriticalError_)  <br/> |Une erreur ou un événement global s'est produit, tel qu'un arrêt de session en cours.  <br/> |Session, tous les types d'objets de banque de messages et de carnet d'adresses, table, état  <br/> |
|Objet modifié ( _fnevObjectModified_)  <br/> |Un objet MAPI a été modifié.  <br/> |Dossiers, messages, tous les types d'objets de carnet d'adresses  <br/> |
|Objet créé ( _fnevObjectCreated_)  <br/> |Un objet MAPI a été créé.  <br/> |Dossiers, messages, tous les types d'objets de carnet d'adresses  <br/> |
|Objet déplacé ( _fnevObjectMoved_)  <br/> |Un objet MAPI a été déplacé.  <br/> |Dossiers, messages, tous les types d'objets de carnet d'adresses  <br/> |
|Objet supprimé ( _fnevObjectDeleted_)  <br/> |Un objet MAPI a été supprimé.  <br/> |Dossiers, messages, tous les types d'objets de carnet d'adresses  <br/> |
|Objet copié ( _fnevObjectCopied_)  <br/> |Un objet MAPI a été copié.  <br/> |Dossiers, messages, tous les types d'objets de carnet d'adresses  <br/> |
|Événement étendu ( _fnevExtended_)  <br/> |Un événement interne défini par un fournisseur de services particulier s'est produit.  <br/> |Tout objet de source de notification  <br/> |
|Recherche terminée ( _fnevSearchComplete_)  <br/> |Une opération de recherche est terminée et les résultats de la recherche sont disponibles.  <br/> |Folders  <br/> |
|Table modifiée ( _fnevTableModified_)  <br/> |Les informations contenues dans un objet table MAPI ont été modifiées.  <br/> |Tableaux  <br/> |
|Nouveau message ( _fnevNewMail_)  <br/> |Un message a été remis et est en attente de traitement.  <br/> |Banque de messages, dossiers  <br/> |
   
L'événement étendu est défini par un fournisseur de services pour représenter un événement qui ne peut pas être couvert par les autres événements prédéfinis. Seuls les clients qui connaissent qu'un fournisseur de services prend en charge un événement étendu peuvent s'inscrire à cet événement. Les clients ne peuvent pas déterminer sans savoir si un fournisseur de services prend en charge un événement étendu et, si c'est le cas, comment gérer ce type d'événement lors de sa réception.
  

