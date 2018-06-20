---
title: IMAPISession IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession
api_type:
- COM
ms.assetid: 5650fa2a-6e62-451c-964e-363f7bee2344
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: a37d8138547c8c4e9308dbb0ebbc6750b152d795
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783961"
---
# <a name="imapisession--iunknown"></a>IMAPISession : IUnknown

  
  
**S’applique à**: Outlook 
  
Gère les objets associés à une session MAPI.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |MAPIX.h  <br/> |
|Exposés par :  <br/> |Objets de session  <br/> |
|Implémentée par :  <br/> |MAPI  <br/> |
|Appelée par :  <br/> |Les applications clientes et MAPI  <br/> |
|Identificateur de l’interface :  <br/> |IID_IMAPISession  <br/> |
|Type de pointeur :  <br/> |LPMAPISESSION  <br/> |
   
## <a name="vtable-order"></a>Ordre vtable

|||
|:-----|:-----|
|[GetLastError](imapisession-getlasterror.md) <br/> |Retourne une structure [MAPIERROR](mapierror.md) qui contient des informations sur l’erreur de session précédente.  <br/> |
|[GetMsgStoresTable](imapisession-getmsgstorestable.md) <br/> |Permet d’accéder à la table de magasin de message qui contient des informations sur toutes les banques de messages dans le profil de la session.  <br/> |
|[OpenMsgStore](imapisession-openmsgstore.md) <br/> |Ouvre une banque de messages et retourne un pointeur [IMsgStore](imsgstoreimapiprop.md) pour davantage d’accès.  <br/> |
|[OpenAddressBook](imapisession-openaddressbook.md) <br/> |Ouvre le carnet d’adresses intégré MAPI, qui retourne un pointeur [IAddrBook](iaddrbookimapiprop.md) pour davantage d’accès.  <br/> |
|[OpenProfileSection](imapisession-openprofilesection.md) <br/> |Ouvre une section du profil actuel et retourne un pointeur [IProfSect](iprofsectimapiprop.md) pour davantage d’accès.  <br/> |
|[GetStatusTable](imapisession-getstatustable.md) <br/> |Fournit l’accès à la table d’état, une table qui contient des informations sur toutes les ressources MAPI dans la session.  <br/> |
|[OpenEntry](imapisession-openentry.md) <br/> |Ouvre un objet et retourne un pointeur d’interface pour l’accès des autres.  <br/> |
|[CompareEntryIDs](imapisession-compareentryids.md) <br/> |Compare deux identificateurs d’entrée pour déterminer si elles font référence au même objet.  <br/> |
|[Conseiller](imapisession-advise.md) <br/> |Inscrit pour recevoir des notifications d’événements spécifiques qui affectent la session.  <br/> |
|[L’avertissement](imapisession-unadvise.md) <br/> |Annule l’envoi de notifications précédemment configurées avec un appel à la méthode **Advise** .  <br/> |
|**Options des messages** <br/> | *Non pris en charge ou documentés.*  <br/> |
|**QueryDefaultMessageOpt** <br/> | *Non pris en charge ou documentés.*  <br/> |
|[EnumAdrTypes](imapisession-enumadrtypes.md) <br/> |Déconseillé. Renvoie les types d’adresses qui peuvent être gérés par tous les fournisseurs de transport dans la session.  <br/> |
|[QueryIdentity](imapisession-queryidentity.md) <br/> |Renvoie l’identificateur d’entrée de l’objet qui fournit l’identité du principale pour la session.  <br/> |
|[Logoff](imapisession-logoff.md) <br/> |Met fin à une session MAPI.  <br/> |
|[SetDefaultStore](imapisession-setdefaultstore.md) <br/> |Établissement d’une banque de messages comme banque de messages par défaut pour la session.  <br/> |
|[AdminServices](imapisession-adminservices.md) <br/> |Retourne un pointeur [IMsgServiceAdmin](imsgserviceadminiunknown.md) pour apporter des modifications à des services de messagerie.  <br/> |
|[ShowForm](imapisession-showform.md) <br/> |Affiche un formulaire.  <br/> |
|[PrepareForm](imapisession-prepareform.md) <br/> |Crée un jeton numérique que la méthode **ShowForm** utilise pour accéder à un message.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

