---
title: IABLogon IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IABLogon
api_type:
- COM
ms.assetid: fe340182-f41e-42e7-b8e8-cc005b1e9a5f
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: d2f7bfd8c1bcc15cc12e4ab6efd26b0591f11b27
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59614023"
---
# <a name="iablogon--iunknown"></a>IABLogon : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Accède aux ressources dans un fournisseur de carnet d’adresses.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapispi.h  <br/> |
|Exposé par :  <br/> |Objets d’logo de carnet d’adresses  <br/> |
|Implémenté par :  <br/> |Fournisseurs de carnets d’adresses  <br/> |
|Appelé par :  <br/> |MAPI  <br/> |
|Identificateur d’interface :  <br/> |IID_IABLogon  <br/> |
|Type de pointeur :  <br/> |LPABLOGON  <br/> |
   
## <a name="vtable-order"></a>Ordre des vtables

|||
|:-----|:-----|
|[GetLastError](iablogon-getlasterror.md) <br/> |Renvoie une structure [MAPIERROR](mapierror.md) qui contient des informations sur l’erreur de fournisseur de carnet d’adresses précédente.  <br/> |
|[Logoff](iablogon-logoff.md) <br/> |Lance le processus de ffage de logo.  <br/> |
|[OpenEntry](iablogon-openentry.md) <br/> |Ouvre un conteneur, un utilisateur de messagerie ou une liste de distribution et renvoie un pointeur vers une implémentation d’interface pour fournir un accès supplémentaire.  <br/> |
|[CompareEntryIDs](iablogon-compareentryids.md) <br/> |Compare deux identificateurs d’entrée pour déterminer s’ils font référence au même objet.  <br/> |
|[Conseiller](iablogon-advise.md) <br/> |Inscrit l’appelant pour recevoir une notification des événements spécifiés qui affectent un conteneur, un utilisateur de messagerie ou une liste de distribution.  <br/> |
|[Unadvise](iablogon-unadvise.md) <br/> |Annule les notifications précédemment définies avec un appel à la **méthode Advise.**  <br/> |
|[OpenStatusEntry](iablogon-openstatusentry.md) <br/> |Ouvre l’objet d’état du fournisseur.  <br/> |
|[OpenTemplateID](iablogon-opentemplateid.md) <br/> |Ouvre une entrée de destinataire dont les données résident dans un fournisseur de carnet d’adresses hôte.  <br/> |
|[GetOneOffTable](iablogon-getoneofftable.md) <br/> |Renvoie une table de modèles unique pour la création de destinataires à ajouter à la liste des destinataires d’un message sortant.  <br/> |
|[PrepareRecips](iablogon-preparerecips.md) <br/> |Prépare une liste de destinataires pour une utilisation ultérieure par le système de messagerie.  <br/> |
   
## <a name="remarks"></a>Remarques

Pour obtenir des informations générales sur les méthodes de l’interface **IABLogon,** voir [Implementing Service Provider Logon](implementing-service-provider-logon.md).
  
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

