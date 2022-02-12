---
title: Événements de notification MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: ef082d7b-9b2d-4267-beb5-d3ed1d9c7bbf
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: e8260fd0db372422d8db86d0d3a618d5f8ed72ae
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62783823"
---
# <a name="mapi-notification-events"></a>Événements de notification MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Lorsque les applications clientes s’inscrivent pour la notification d’événement, elles doivent spécifier un ou plusieurs événements. Les événements qu’ils peuvent spécifier dépendent de l’ensemble d’événements que la source de conseil prévue prend en charge. Les clients et les fournisseurs de services peuvent s’inscrire pour dix types de notifications, chacun représenté par une constante. La notification d’objet d’état est une exception. La notification d’objet d’état est une notification MAPI interne ; les clients ne peuvent pas s’y inscrire et les fournisseurs de services ne peuvent pas le générer. Le tableau suivant décrit les types d’événements et les objets source de conseil qui peuvent les prendre en charge. La constante d’événement est incluse dans le type d’événement.
  
|**Type d’événement**|**Description**|**Conseiller les objets source**|
|:-----|:-----|:-----|
|Erreur critique ( _fnevCriticalError_)  <br/> |Une erreur globale ou un événement s’est produit, tel qu’un arrêt de session en cours. |Session, tous les types d’objets de magasin de messages et de carnet d’adresses, tableau, état  <br/> |
|Objet modifié ( _fnevObjectModified_)  <br/> |Un objet MAPI a changé. |Dossiers, messages, tous types d’objets de carnet d’adresses  <br/> |
|Objet créé ( _fnevObjectCreated_)  <br/> |Un objet MAPI a été créé. |Dossiers, messages, tous types d’objets de carnet d’adresses  <br/> |
|Objet déplacé ( _fnevObjectMoved_)  <br/> |Un objet MAPI a été déplacé. |Dossiers, messages, tous types d’objets de carnet d’adresses  <br/> |
|Objet supprimé ( _fnevObjectDeleted_)  <br/> |Un objet MAPI a été supprimé. |Dossiers, messages, tous types d’objets de carnet d’adresses  <br/> |
|Objet copié ( _fnevObjectCopied_)  <br/> |Un objet MAPI a été copié. |Dossiers, messages, tous types d’objets de carnet d’adresses  <br/> |
|Événement étendu ( _fnevExtended_)  <br/> |Un événement interne défini par un fournisseur de services particulier s’est produit. |Tout objet source de conseil  <br/> |
|Recherche terminée ( _fnevSearchComplete_)  <br/> |Une opération de recherche est terminée et les résultats de la recherche sont disponibles. |Folders  <br/> |
|Table modified ( _fnevTableModified_)  <br/> |Les informations d’un objet table MAPI ont changé. |Tables  <br/> |
|Nouveau courrier ( _fnevNewMail_)  <br/> |Un message a été remis et attend d’être traitée. |Magasin de messages, dossiers  <br/> |
   
L’événement étendu est défini par un fournisseur de services pour représenter un événement qui ne peut être couvert par aucun des autres événements prédéfin définis. Seuls les clients qui savent avant qu’ils s’inscrivent qu’un fournisseur de services prend en charge un événement étendu peuvent s’inscrire à cet événement. Il n’est pas possible pour les clients de déterminer à l’avance si un fournisseur de services prend en charge un événement étendu et, si tel est le cas, comment gérer un tel événement lorsqu’il est reçu.
  

