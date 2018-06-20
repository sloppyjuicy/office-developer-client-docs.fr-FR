---
title: Propriété identificateur de plages
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c01e95bb-be25-490d-880b-60674f890258
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: aee199cbbd05606d20378023f103fa122f1457f2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786943"
---
# <a name="property-identifier-ranges"></a>Propriété identificateur de plages

  
  
**S’applique à**: Outlook 
  
Le tableau suivant récapitule les différentes plages pour les identificateurs de propriété, description du propriétaire pour les propriétés de chaque plage.
  
|**Plage d’identificateurs**|**Description**|
|:-----|:-----|
|0000  <br/> |Réservé à la valeur spéciale **PR_NULL**par MAPI.  <br/> |
|0001 - 0BFF  <br/> |Propriétés d’enveloppe de message définies par MAPI.  <br/> |
|0C 00 - 0DFF  <br/> |Propriétés de destinataire définies par MAPI.  <br/> |
|0E00 - 0FFF  <br/> |Propriétés de message non-transmissible définies par MAPI.  <br/> |
|1000 - 2FFF  <br/> |Propriétés du contenu du message définies par MAPI.  <br/> |
|3000 - 3FFF  <br/> |Propriétés d’objets autres que les messages et de destinataires définis par MAPI.  <br/> |
|4000 - 57FF  <br/> |Propriétés d’enveloppe de message définies par les fournisseurs de transport.  <br/> |
|5800 - 5FFF  <br/> |Propriétés de destinataire définies par les fournisseurs de carnet d’adresses et de transport.  <br/> |
|6000 - 65FF  <br/> |Propriétés de message non-transmissible définies par les clients.  <br/> |
|6600 - 67FF  <br/> |Propriétés non-transmissible définies par un fournisseur de services. Ces propriétés peuvent être visible ou invisible aux utilisateurs.  <br/> |
|6800 - 7BFF  <br/> |Propriétés de contenu de message pour les classes de message personnalisées définies par les créateurs de ces classes.  <br/> |
|7C 00 - 7FFF  <br/> |Propriétés non-transmissible de classes de message personnalisées définies par les créateurs de ces classes.  <br/> |
|8000 - FFFE  <br/> |Propriétés définies par les clients et occasionnellement service fournisseurs sont identifiés par un nom à travers les méthodes [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) et [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) .  <br/> |
|FFFF  <br/> |Réservé à la valeur d’erreur spéciaux PROP_ID_INVALID par MAPI.  <br/> |
   
La plage entre 3000 et 3FFF est réservé pour les propriétés qui ne sont pas liées aux messages ou destinataires. MAPI divise cette plage en sous-plages par les types d’objet. le tableau suivant illustre cette répartition plue. 
  
|**Plage d’identificateurs**|**Type de propriété**|
|:-----|:-----|
|3000 - 33FF  <br/> |Propriétés communes qui apparaissent sur plusieurs objets, tels que **PR_DISPLAY_NAME** et **PR_ENTRYID**.  <br/> |
|3400 - 35FF  <br/> |Stocker les propriétés des messages  <br/> |
|3600 - 36FF  <br/> |Propriétés de conteneur du carnet d’adresses et de dossier  <br/> |
|3700 - 38FF  <br/> |Propriétés des pièces jointes  <br/> |
|3900 - 39FF  <br/> |Propriétés de carnet d’adresses  <br/> |
|3A00 - 3BFF  <br/> |Propriétés de l’utilisateur de messagerie  <br/> |
|3C 00 - ET 3CFF  <br/> |Propriétés de liste de distribution  <br/> |
|3D 00 - 3DFF  <br/> |Propriétés de profil  <br/> |
|3E00 - 3FFF  <br/> |Propriétés de l’objet état  <br/> |
   

