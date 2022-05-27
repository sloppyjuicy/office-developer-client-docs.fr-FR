---
title: Plages d’identificateurs de propriétés
description: Récapitule les différentes plages des identificateurs de propriétés, en décrivant le propriétaire des propriétés de chaque plage.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: c01e95bb-be25-490d-880b-60674f890258
ms.openlocfilehash: 140ba9d1b74156eccb66de2b00cf04b74c2ef9fc
ms.sourcegitcommit: b568a00c3da704273896b6941b65cee91fd1bd22
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2022
ms.locfileid: "65752406"
---
# <a name="property-identifier-ranges"></a>Plages d’identificateurs de propriétés

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Le tableau suivant récapitule les différentes plages pour les identificateurs de propriétés, en décrivant le propriétaire des propriétés de chaque plage.
  
|**Plage d’identificateurs**|**Description**|
|:-----|:-----|
|0000  <br/> |Réservé par MAPI pour la valeur spéciale **PR_NULL**. |
|0001 - 0BFF  <br/> |Propriétés d’enveloppe de message définies par MAPI. |
|0C00 - 0DFF  <br/> |Propriétés du destinataire définies par MAPI. |
|0E00 - 0FFF  <br/> |Propriétés de message non transmissibles définies par MAPI. |
|1000 - 2FFF  <br/> |Propriétés de contenu de message définies par MAPI. |
|3000 - 3FFF  <br/> |Propriétés des objets autres que les messages et les destinataires définis par MAPI. |
|4000 - 57FF  <br/> |Propriétés d’enveloppe de message définies par les fournisseurs de transport. |
|5800 - 5FFF  <br/> |Propriétés du destinataire définies par les fournisseurs de transport et de carnet d’adresses. |
|6000 - 65FF  <br/> |Propriétés de message non transmissibles définies par les clients. |
|6600 - 67FF  <br/> |Propriétés non transmissibles définies par un fournisseur de services. Ces propriétés peuvent être visibles ou invisibles pour les utilisateurs. |
|6800 - 7BFF  <br/> |Propriétés de contenu de message pour les classes de message personnalisées définies par les créateurs de ces classes. |
|7C00 - 7FFF  <br/> |Propriétés non transmissibles pour les classes de message personnalisées définies par les créateurs de ces classes. |
|8000 - FFFE  <br/> |Propriétés définies par les clients et parfois les fournisseurs de services identifiés par leur nom via les méthodes [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) et [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) . |
|FFFF  <br/> |Réservé par MAPI pour la valeur d’erreur spéciale PROP_ID_INVALID. |
   
La plage comprise entre 3000 et 3FFF est réservée aux propriétés qui ne sont pas liées aux messages ou aux destinataires. MAPI divise cette plage en sous-plages par types d’objets ; le tableau suivant montre cette répartition supplémentaire. 
  
|**Plage d’identificateurs**|**Type de propriété**|
|:-----|:-----|
|3000 - 33FF  <br/> |Propriétés courantes qui apparaissent sur plusieurs objets, tels que **PR_DISPLAY_NAME** et **PR_ENTRYID**. |
|3400 - 35FF  <br/> |Propriétés du magasin de messages  <br/> |
|3600 - 36FF  <br/> |Propriétés du conteneur de dossiers et de carnets d’adresses  <br/> |
|3700 - 38FF  <br/> |Propriétés des pièces jointes  <br/> |
|3900 - 39FF  <br/> |Propriétés du carnet d’adresses  <br/> |
|3A00 - 3BFF  <br/> |Propriétés de l’utilisateur de messagerie  <br/> |
|3C00 - 3CFF  <br/> |Propriétés de la liste de distribution  <br/> |
|3D00 - 3DFF  <br/> |Propriétés du profil  <br/> |
|3E00 - 3FFF  <br/> |Propriétés de l’objet Status  <br/> |
   

