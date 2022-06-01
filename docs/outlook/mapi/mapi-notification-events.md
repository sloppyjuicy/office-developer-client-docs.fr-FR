---
title: Événements de notification MAPI
description: Décrit les dix types de notifications pour lesquelles les clients et les fournisseurs de services peuvent s’inscrire, chacune représentée par une constante.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: ef082d7b-9b2d-4267-beb5-d3ed1d9c7bbf
ms.openlocfilehash: 46fa709373968c870b81f8aeedd02f7793b32076
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65812046"
---
# <a name="mapi-notification-events"></a>Événements de notification MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Lorsque les applications clientes s’inscrivent pour la notification d’événement, elles doivent spécifier un ou plusieurs événements. Les événements qu’ils peuvent spécifier dépendent de l’ensemble des événements pris en charge par la source de conseils prévue. Il existe dix types de notifications pour lesquelles les clients et les fournisseurs de services peuvent s’inscrire, chacune représentée par une constante. La notification d’objet Status est une exception. La notification d’objet Status est une notification MAPI interne ; les clients ne peuvent pas s’inscrire et les fournisseurs de services ne peuvent pas le générer. Le tableau suivant décrit les types d’événements et les objets sources de conseils qui peuvent les soutenir. La constante d’événement est incluse avec le type d’événement.
  
|**Type d’événement**|**Description**|**Conseiller les objets sources**|
|:-----|:-----|:-----|
|Erreur critique ( _fnevCriticalError_)  <br/> |Une erreur globale ou un événement s’est produit, tel qu’un arrêt de session en cours. |Session, tous les types d’objets de magasin de messages et de carnet d’adresses, table, état  <br/> |
|Objet modifié ( _fnevObjectModified_)  <br/> |Un objet MAPI a changé. |Dossiers, messages, tous les types d’objets de carnet d’adresses  <br/> |
|Objet créé ( _fnevObjectCreated_)  <br/> |Un objet MAPI a été créé. |Dossiers, messages, tous les types d’objets de carnet d’adresses  <br/> |
|Objet déplacé ( _fnevObjectMoved_)  <br/> |Un objet MAPI a été déplacé. |Dossiers, messages, tous les types d’objets de carnet d’adresses  <br/> |
|Objet supprimé ( _fnevObjectDeleted_)  <br/> |Un objet MAPI a été supprimé. |Dossiers, messages, tous les types d’objets de carnet d’adresses  <br/> |
|Objet copié ( _fnevObjectCopied_)  <br/> |Un objet MAPI a été copié. |Dossiers, messages, tous les types d’objets de carnet d’adresses  <br/> |
|Événement étendu ( _fnevExtended_)  <br/> |Un événement interne défini par un fournisseur de services particulier s’est produit. |Tout objet source conseiller  <br/> |
|Recherche terminée ( _fnevSearchComplete_)  <br/> |Une opération de recherche est terminée et les résultats de la recherche sont disponibles. |Folders  <br/> |
|Table modified ( _fnevTableModified_)  <br/> |Les informations d’un objet de table MAPI ont changé. |Tables  <br/> |
|Nouveau courrier ( _fnevNewMail_)  <br/> |Un message a été remis et attend d’être traité. |Magasin de messages, dossiers  <br/> |
   
L’événement étendu est défini par un fournisseur de services pour représenter un événement qui ne peut être couvert par aucun des autres événements prédéfinis. Seuls les clients qui savent avant d’inscrire qu’un fournisseur de services prend en charge un événement étendu peuvent s’inscrire à cet événement. Il n’est pas possible pour les clients de déterminer à l’avance si un fournisseur de services prend en charge un événement étendu et, si c’est le cas, comment gérer un tel événement lorsqu’il est reçu.
  

